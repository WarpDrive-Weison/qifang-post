# 安装与校验

## 下载什么

当前版本为 0.2.109。Mac APP 支持 macOS 12 或更高版本的 Apple 芯片 Mac；Windows 使用同版本 AI 技能模式，见[Windows 技能指南](WINDOWS_SKILL.md)。以下 APP 安装步骤仅适用于 Mac。

从同一个 [v0.2.109 Release](https://github.com/WarpDrive-Weison/qifang-post/releases/tag/v0.2.109) 下载：

- `QifangPost-0.2.109-macOS-QA-arm64.dmg`：推荐安装方式。
- `QifangPost-0.2.109-macOS-QA-arm64.zip`：备用，与 DMG 二选一。
- `SHA256SUMS-0.2.109.txt`：完整性校验。

Codex 技能是可选的，不安装也能运行 APP。FFmpeg 源码与上游签名属于第三方合规、重建及核验材料，不需要安装；GitHub 自动提供的 Source code 压缩包是本仓库的说明与技能，不是 APP 安装包。

## 校验

在下载目录运行：

```bash
shasum -a 256 "QifangPost-0.2.109-macOS-QA-arm64.dmg"
```

结果必须与 `SHA256SUMS-0.2.109.txt` 中同名条目完全一致。使用 ZIP 时相应替换文件名。

## 安装

1. 退出正在运行的齐放Post；先妥善处理进行中的任务。
2. 打开 DMG，把齐放Post.app 拖入 Applications；或解压 ZIP 后移动 APP。
3. 从 Applications 打开齐放Post，确认版本为 0.2.109。
4. 在新的电脑上分别登录各平台。安装包不会带上其他电脑的账号、Cookie、草稿或 API Key。

当前包为 ad-hoc 签名、未完成 Apple 公证的 QA 版。macOS 可能拦截首次启动，请先检查下载来源、校验值和安全提示，再决定是否在系统设置的隐私与安全性中允许打开；不要全局关闭 Gatekeeper。包内校验通过不代表已完成其他 Mac 的安装验收。

## AI 文案

默认 HTTPS 服务端中转已写入 0.2.109，正常使用默认服务不要求自行填写 API Key。接口访问与额度受服务端控制；需要联网。可以改用手动文案或用户自有 API，数据范围见 [隐私说明](../PRIVACY.md)。AI 生成遵守标题 20 字、正文 60 字上限；手动修改不限这些字数，超出平台发布上限时仅提示，不截断草稿。

## 更新与保留

替换 APP 不应删除 `~/Library/Application Support/齐放Post` 中的账号、草稿、素材和任务记录。升级前备份重要数据；仅将旧 APP 移走，不要顺带清空应用数据目录。保留最新版安装包与 SHA-256，只清理已被新版替代的旧安装包。

## Windows：无需安装齐放 APP

下载同一 Release 的 `qifang-post-skill-0.2.109.zip`，按 `SHA256SUMS-skill-0.2.109.txt` 校验。由具备本机浏览器控制与文件上传能力的 AI 客户端加载技能，操作它支持的 Windows 浏览器。技能不自带 AI 或控制引擎，也不使用 Mac APP 的内置服务；仅有纯文本聊天能力不能执行网页操作。

推荐使用 Codex 配合技能使用，大语言模型选择 GPT 5.6 sol 以上模型。详细步骤、示例请求及依赖见 [Windows 技能指南](WINDOWS_SKILL.md)，测试记录见 [QA Scope](QA_SCOPE_0.2.109.md)。旧 Windows APP 安装程序仍保持下架。
