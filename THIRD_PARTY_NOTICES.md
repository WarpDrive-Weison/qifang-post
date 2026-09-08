# Third-party notices

齐放Post includes or invokes the components listed below. Each component is
licensed by its respective copyright holders under its own terms. Those terms
apply independently of the 齐放Post Limited Public Evaluation License.

## FFmpeg 9.0.1

齐放Post invokes separate FFmpeg and FFprobe executables for local media
inspection, frame extraction, and speech-audio conversion. The application is
not linked against FFmpeg libraries.

The release executables are built from FFmpeg 9.0.1 without `--enable-gpl`,
`--enable-nonfree`, or `--enable-version3`, and are distributed under the GNU
Lesser General Public License, version 2.1 or later.

- Project: https://ffmpeg.org/
- Exact upstream source: https://ffmpeg.org/releases/ffmpeg-9.0.1.tar.xz
- Upstream license information: https://ffmpeg.org/legal.html
- LGPL 2.1 text: https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html
- Corresponding source supplied with the Release: `ffmpeg-9.0.1.tar.xz`
- Exact build configuration and binary hashes: `FFMPEG_BUILDINFO.txt` beside
  the executables in each application package
- Reproduction instructions: [`third_party/ffmpeg/README.md`](third_party/ffmpeg/README.md)

## sharp 0.35.3

齐放Post uses sharp for local image decoding, resizing, cropping, and cover
generation. sharp is licensed under the Apache License 2.0.

- Project: https://sharp.pixelplumbing.com/
- Source for 0.35.3: https://github.com/lovell/sharp/tree/v0.35.3
- License: https://github.com/lovell/sharp/blob/v0.35.3/LICENSE
- Apache License 2.0: https://www.apache.org/licenses/LICENSE-2.0

## libvips and sharp-libvips

The platform-specific sharp packages include libvips and supporting libraries
produced by `sharp-libvips`. The bundled `sharp-libvips` package is version
1.3.2 and contains libvips 8.18.3. Its package metadata and licensing inventory
declare LGPL-covered libraries under the GNU Lesser General Public License,
version 3.0 or later. The `sharp-libvips` inventory also identifies the licenses
of its other bundled supporting libraries.

- sharp-libvips 1.3.2 source and licensing inventory:
  https://github.com/lovell/sharp-libvips/tree/v1.3.2
- libvips 8.18.3 source: https://github.com/libvips/libvips/tree/v8.18.3
- libvips license file: https://github.com/libvips/libvips/blob/v8.18.3/COPYING
- LGPL 3.0 text: https://www.gnu.org/licenses/lgpl-3.0.html

The applicable package metadata, version inventory, and license materials are
preserved in the packaged dependency tree where provided upstream.

## Electron 43.2.0 and Chromium

齐放Post is built with Electron 43.2.0, licensed under the MIT License.
Electron embeds Chromium and other third-party software. Chromium is distributed
under the BSD 3-Clause License together with separately licensed third-party
components.

- Electron source for 43.2.0:
  https://github.com/electron/electron/tree/v43.2.0
- Electron MIT license:
  https://github.com/electron/electron/blob/v43.2.0/LICENSE
- Chromium source: https://chromium.googlesource.com/chromium/src/
- Chromium license:
  https://chromium.googlesource.com/chromium/src/+/refs/heads/main/LICENSE

Electron's `resources/legal/ELECTRON_LICENSE.txt` and Chromium's generated
`resources/legal/CHROMIUM_LICENSES.html` are retained in every application distribution.

## No change to upstream terms

This notice is informational. It does not replace, narrow, or expand the license
terms supplied by any third-party copyright holder. If this summary conflicts
with an upstream license, the upstream license controls for that component.
