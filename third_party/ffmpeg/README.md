# Rebuilding the bundled FFmpeg executables

齐放Post v0.2.103 uses separate FFmpeg 9.0.1 command-line executables. They are
built from the unmodified upstream source archive attached to the same GitHub
Release.

Before building, verify both the SHA-256 and the detached signature:

```bash
shasum -a 256 ffmpeg-9.0.1.tar.xz
gpg --verify ffmpeg-9.0.1.tar.xz.asc ffmpeg-9.0.1.tar.xz
```

Expected source SHA-256:

```text
cf38e0e28c7e5605942c4a77755349b0145804a397af37eb1fb4c77cb237f635
```

Expected FFmpeg release-signing fingerprint:

```text
FCF986EA15E6E293A5644F10B4322F04D67658D8
```

The recorded configure lines are in each installer's `resources/ffmpeg` folder.
The commands below reproduce those configurations from a clean source tree.

## macOS arm64

```bash
./configure \
  --prefix=/opt/qifang-ffmpeg \
  --arch=arm64 \
  --target-os=darwin \
  --cc=clang \
  --extra-version=qifang-lgpl \
  --disable-gpl --disable-nonfree --disable-version3 \
  --disable-doc --disable-debug --disable-ffplay --disable-network \
  --disable-autodetect --disable-shared --enable-static --enable-pthreads \
  --enable-videotoolbox \
  --extra-cflags='-mmacosx-version-min=12.0' \
  --extra-ldflags='-mmacosx-version-min=12.0'
make -j8
make DESTDIR="$PWD/stage" install
```

## Windows x64 cross-build on macOS

Install a MinGW-w64 x64 cross-compiler, then run:

```bash
./configure \
  --prefix=/opt/qifang-ffmpeg \
  --arch=x86_64 \
  --target-os=mingw32 \
  --cross-prefix=x86_64-w64-mingw32- \
  --extra-version=qifang-lgpl \
  --disable-x86asm \
  --disable-gpl --disable-nonfree --disable-version3 \
  --disable-doc --disable-debug --disable-ffplay --disable-network \
  --disable-autodetect --disable-shared --enable-static --enable-w32threads \
  --extra-ldflags=-static
make -j8
make DESTDIR="$PWD/stage" install
```

No FFmpeg source patches are applied. `--disable-autodetect` prevents accidental
linkage to locally installed optional libraries. The app uses BMP for lossless
frame extraction and PCM WAV for speech audio, so the build does not require
zlib, x264, x265, LAME, or another external codec library. The macOS build uses
Apple's system VideoToolbox framework only for its local autoplay regression fixture.
