# 水杉输入法 · 游戏中文输入兼容修改版

> **本修改版是为《太空工程师》（Space Engineers）及类似存在中文输入兼容问题的游戏而修改的水杉输入法。**
>
> 目标是改善游戏聊天框中无法输入中文、候选不显示、中文无法上屏，以及英文和空格输入异常等问题。
>
> **目前仅实测通过《太空工程师 1》。其他游戏（包括《太空工程师 2》）尚未测试，不代表已支持。**

## 本修改版说明

基于官方水杉输入法 v0.11.1 的非官方兼容修改，保留原项目来源、版权和 GPL-3.0 许可证。r7 在本机测试中修复了 COMless 初始化、候选显示和全角字符兼容问题；游戏内采用半角策略，保留中文组合与空格选词。

已测试：Windows 11、Steam 版《太空工程师 1》01_210_014、DX11 窗口模式。测试者确认中文候选及上屏、英文和普通空格、选字与编辑按键、关闭聊天后的 WASD/快捷键、Alt+Tab 及记事本中文正常。其他显示模式未单独验证。

## 下载本修改版 r7

**已上传并发布：[r7 发布页（源码、DLL 测试包、补丁、SHA256）](https://github.com/stdeven521/msime-windows/releases/tag/v0.11.1-se-r7)。**

- [下载 r7 x64 DLL 测试包](https://github.com/stdeven521/msime-windows/releases/download/v0.11.1-se-r7/Metasequoia-SpaceEngineers-r7-x64.zip)（需先安装官方 v0.11.1；含安装和回滚脚本）
- [下载完整修改源码（含子模块）](https://github.com/stdeven521/msime-windows/releases/download/v0.11.1-se-r7/Metasequoia-SpaceEngineers-r7-source.zip)

当前通过 Release 附件发布 r7。Git 推送授权尚未完成，默认 develop 代码目录仍以原始代码为主；请使用上面的修改源码包，**不要把 GitHub 自动生成的 Source code 压缩包或下方原版下载链接当作 r7**。

---

## 上游原版项目资料

以下是原始水杉项目的介绍、徽章和下载入口，不代表本修改版的发布状态。

# 水杉输入法

[官网](https://msime.app) · [用户文档](https://msime.app/docs/) · [隐私说明](PRIVACY.md) · [代码签名策略 / Code signing policy](docs/code-signing-policy.md) · [English README](README.en.md)

<!-- badges:start -->
[![CI](https://img.shields.io/github/actions/workflow/status/metasequoiaime/MSIME-Windows/ci.yml?branch=develop&label=CI)](https://github.com/metasequoiaime/MSIME-Windows/actions/workflows/ci.yml)
[![CodeQL](https://img.shields.io/github/actions/workflow/status/metasequoiaime/MSIME-Windows/codeql.yml?branch=develop&label=CodeQL)](https://github.com/metasequoiaime/MSIME-Windows/actions/workflows/codeql.yml)
[![Release](https://img.shields.io/github/v/release/metasequoiaime/MSIME-Windows?include_prereleases&label=release)](https://github.com/metasequoiaime/MSIME-Windows/releases)
[![Downloads](https://img.shields.io/github/downloads/metasequoiaime/MSIME-Windows/total?label=downloads)](https://github.com/metasequoiaime/MSIME-Windows/releases)
[![License](https://img.shields.io/github/license/metasequoiaime/MSIME-Windows)](LICENSE)
[![Stars](https://img.shields.io/github/stars/metasequoiaime/MSIME-Windows?style=flat)](https://github.com/metasequoiaime/MSIME-Windows/stargazers)
<!-- badges:end -->

一款开源的自由 Windows 输入法，面向 Windows 10 / Windows 11，采用纯 TSF 方案。

## 下载与安装

- **安装包**：[Releases](https://github.com/metasequoiaime/MSIME-Windows/releases)，或[官网下载页](https://msime.app/download/)
- **安装步骤与常见问题**：[docs/installation.md](docs/installation.md)

安装后用 `Win + 空格` 切换到水杉输入法。如果切换不过去、Server 反复退出或设置窗口一闪即关，多半是缺少 Visual C++ 2015–2022 Redistributable（**x64**），处理办法见安装文档的常见问题。

其他平台：[macOS 与 iOS](https://github.com/metasequoiaime/MSIME-Apple) · [Linux](https://github.com/metasequoiaime/MSIME-Linux)

## 参与贡献

本项目现在及未来都会保持 100% 开源，欢迎提交 PR，也接受借助 AI 完成的 PR，唯一的请求是友善交流。不会写 TSF 或 C++ 也没关系。

Issue 已经逐条核过并按可接手程度打了标签，可以直接筛：

- [good first issue](https://github.com/metasequoiaime/MSIME-Windows/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)——改动小，根因和修法已经写明
- [no-code](https://github.com/metasequoiaime/MSIME-Windows/issues?q=is%3Aissue+is%3Aopen+label%3Ano-code)——不需要写代码：图标资源、词库条目、文档、调研
- [help wanted](https://github.com/metasequoiaime/MSIME-Windows/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)——根因明确、改动中等
- [needs-design](https://github.com/metasequoiaime/MSIME-Windows/issues?q=is%3Aissue+is%3Aopen+label%3Aneeds-design)——方案未定，先在 Issue 里讨论再动手

写代码、写文档、整理词库、测试 Bug、制作教程，都是非常有价值的开源贡献。可以纯手写，也可以借助 AI；但请认真检查和测试，并注意不要在 PR、Issue、截图或日志中泄露 API Key 等敏感信息。完整的贡献约定见[贡献指南](https://github.com/metasequoiaime/.github/blob/main/CONTRIBUTING.md)。

**要动代码的话，本仓的环境要求、从源码构建、打包和提交前检查全部写在 [CONTRIBUTING.md](CONTRIBUTING.md) 里。**

## 文档

- [功能说明](docs/features.md)：功能简介、各功能的用法与软件截图
- [项目结构](docs/project-structure.md)：目录职责与引擎来源

## 代码签名策略

Free code signing provided by [SignPath.io](https://about.signpath.io/), certificate by [SignPath Foundation](https://signpath.org/).

签名范围、团队角色（Committers / Reviewers / Approvers）、构建与发布流程以及当前状态见 [Code signing policy](docs/code-signing-policy.md)，隐私说明见 [PRIVACY.md](PRIVACY.md)。

## 开源协议

GPL-3.0。

## 参考

### Windows 开源输入法参考

以下是一些 Windows 的开源输入法的参考项目。

- [Microsoft TSF IME Demo](https://github.com/microsoft/Windows-classic-samples/tree/main/Samples/IME/cpp/SampleIME)
- [weasel](https://github.com/rime/weasel)
- [PIME](https://github.com/EasyIME/PIME)
- [WindInput](https://github.com/huanfeng/WindInput)

### 一些其他输入法相关的资源

- 微软双拼方案来源：<https://www.bilibili.com/opus/550351671882601523>

<!-- star-history:start -->
## Star History

<a href="https://star-history.com/#metasequoiaime/MSIME-Windows&Date">
  <img src="https://api.star-history.com/svg?repos=metasequoiaime/MSIME-Windows&type=Date" alt="Star History Chart" width="600">
</a>
<!-- star-history:end -->

## 赞赏支持

如果水杉输入法对您有帮助，欢迎请我吃个烤红薯/烤玉米/烤栗子/烤白果。

<img src="docs/images/sponsor-wechat.jpg" width="300" alt="苏小凡 Channel 的微信赞赏码">
