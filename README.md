<div align="center">
  <img src="skills/qifang-post/assets/logo.png" alt="齐放Post" width="112" />
  <h1>齐放Post</h1>
  <p>面向抖音、视频号、小红书与快手的桌面短视频发布工作台</p>
</div>

> 当前公开版本为 **v0.2.103 预发布 QA 版**。安装包尚未完成 Apple 公证或 Windows Authenticode 签名，请先核对 SHA-256，并阅读下方已知限制。

## 功能概览

- 一次导入成片，为抖音、视频号、小红书、快手分别准备发布表单。
- 从完整口播提炼不超过 20 字的标题与不超过 60 字的短正文。
- 支持首帧取景或上传图片，分别管理 3:4 竖版封面与 4:3 横版/分享封面。
- 对平台原生话题候选进行选择与回读，不把纯文本 `#话题` 当成已选话题。
- 每个平台保留独立任务账本、最终确认指纹、一次性提交保护与管理列表核验。
- 登录、二维码、验证码、风控、协议或账号权限变化时进入可接管状态，不绕过平台安全门槛。

## 下载

请前往 [Releases](https://github.com/WarpDrive-Weison/qifang-post/releases) 下载：

- macOS（Apple 芯片）：`齐放Post-0.2.103-macOS-QA-arm64.dmg`
- Windows 10/11 x64：`齐放Post-0.2.103-Windows-QA-x64-Setup.exe`
- 校验清单：`SHA256SUMS-0.2.103.txt`
- Codex 技能包：`qifang-post-skill-0.2.103.zip`
- FFmpeg 对应源码：`ffmpeg-9.0.1.tar.xz`

安装前执行 SHA-256 校验，并与 Release 中的清单逐字比对。详细步骤见 [安装说明](docs/INSTALL.md)。

## 支持范围

| 系统 | 架构 | 当前状态 |
| --- | --- | --- |
| macOS 12 Monterey 或更高版本 | Apple Silicon / arm64 | 本机打包、安装、启动、迁移与结构回归；ad-hoc 签名，未公证 |
| Windows 10/11 | x64 | macOS 交叉构建、解包、架构与源码一致性核验；未做 Windows 原生运行验收，未签名 |

Intel Mac、Windows ARM 与更旧系统暂不在当前支持范围内。

## 使用流程

1. 在账号中心登录需要的平台。账号登录发生在应用自己的 Chromium 会话中。
2. 导入已完成的 MP4/MOV，确认标题、短正文、原生话题、封面及平台选项。
3. 等待每个平台达到“表单就绪”，核对最终确认指纹。
4. 明确确认后，每个平台最多执行一次最终提交。
5. 在任务记录中查看各平台独立状态；“已提交”“审核中”和“已发布”不会被混为一谈。

## AI 文案说明

公开 QA 包不内置齐放Post运营方的托管 AI 额度或私有网关。需要 AI 文案时，请在设置中配置用户自己的 DeepSeek 或 OpenAI 兼容 API；不配置时仍可手动填写标题、正文与话题。

## Codex 技能

仓库内的 [qifang-post skill](skills/qifang-post/SKILL.md) 提供齐放Post的标准发布、恢复与证据核验流程。

安装示例：

```bash
mkdir -p ~/.codex/skills
cp -R skills/qifang-post ~/.codex/skills/qifang-post
```

技能不会扩大任何发布权限。平台登录、验证码、风控与最终确认仍受账号和平台页面约束。

## 证据边界

齐放Post把视频传输、表单就绪、最终提交、平台审核、管理列表匹配与公开发布视为不同状态。上传进度或一次按钮点击都不等于公开发布成功。完整定义见 [技能证据模型](skills/qifang-post/references/evidence.md)。

## 隐私、安全与第三方组件

安装包不包含平台登录态。平台 Cookie 按本机用户、平台和账号隔离；应用不记录平台密码。视频会上传至用户选定的平台，公开 QA 包没有齐放Post托管 AI 视频上传服务。

- [隐私说明](PRIVACY.md)
- [安全策略](SECURITY.md)
- [第三方组件声明](THIRD_PARTY_NOTICES.md)
- [贡献与问题反馈](CONTRIBUTING.md)

提交问题时请勿附带密码、Cookie、令牌、二维码、私人视频或未脱敏的账号信息。

## 版本与验收

v0.2.103 的完整变更、测试数字和限制见 [Release Notes](docs/RELEASE_NOTES_0.2.103.md) 与 [QA Scope](docs/QA_SCOPE_0.2.103.md)。平台页面会持续改版，离线回归和安装验证不等同于一次新的公网投稿。

## 第三方平台声明

齐放Post 是独立开发的工具，与抖音、微信视频号、小红书、快手及其运营方不存在隶属、赞助或官方背书关系。相关平台名称、商标和标识归各自权利人所有；使用本工具仍须遵守各平台的服务条款、内容规则和账号权限要求。

## 许可

本仓库用于分发齐放Post安装包、公开说明和配套技能，不包含应用源代码，也不声明为开源软件。除 GitHub 服务条款授予的平台权利外，其他权利均保留。详见 [LICENSE](LICENSE.md)。
