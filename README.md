# 起身啦 · UpYouGo

[English](i18n/en/README.md) | [日本語](i18n/ja/README.md) | [한국어](i18n/ko/README.md) | **简体中文** | [繁體中文](i18n/zh-Hant/README.md)

> 文档支持五种语言查看。当前 1.1.1 桌面应用界面仍以简体中文为主，选择文档语言不会改变应用界面语言。

Windows 坐站交替提醒与桌面猫咪。支持工作日程、午休、中国调休、免打扰和本地统计。

**[下载最新版](https://github.com/elvinzou/upyougo-releases/releases/latest)** · [使用说明](USER_GUIDE.md) · [功能需求](docs/REQUIREMENTS.md) · [后续规划](docs/ROADMAP.md) · [更新记录](CHANGELOG.md)

## 安装

1. 在 Releases 下载 **UpYouGo-Setup.exe**。
2. 选择独立、可写的安装目录，例如 `D:\Apps\UpYouGo`，点击安装。
3. 设置坐站时间及工作日程，开始计时。

需要 Windows x64、.NET Framework（建议 4.8）和 Microsoft Edge WebView2 Runtime。安装器不附带完整 WebView2 Runtime。关闭主面板不会退出；右键托盘小猫可退出。

## 功能

- 坐站交替计时，暂停/继续、确认姿势和稍后提醒。
- 像素猫陪伴，气泡提醒不抢占当前输入焦点。
- 工作时段、星期、中国调休与可选午休。
- 锁屏/睡眠处理，手动及全屏自动免打扰。
- 本地统计、行为反馈和开机启动选项。
- 自定义目录、新版提示、在线/本地更新及失败回退。

## 在线更新

安装版启动后及每 6 小时检查此仓库的正式 Release。点击托盘更新通知或“版本与更新”，查看说明后下载更新。程序先校验文件，再保存退出并验证新版；失败恢复原安装状态。

`UpYouGo-Windows-x64.zip` 可用于便携运行或本地更新。`.sha256` 是更新校验文件，普通用户无需手动操作。GitHub 自动提供的 Source code 压缩包仅包含本仓库文档，不是安装包。

## 数据与限制

个人设置和统计留在 `%APPDATA%\LumbarReminder`，更新不删除它们；这些记录不上传。联网用于版本检查、下载及日历同步。

更新不接续原倒计时，重启遵循启动设置。目前尚无完整卸载与旧版本自动清理入口。此仓库仅用于公开软件分发和使用文档，完整开发源码保持私有。

问题反馈请描述 Windows 版本、应用版本、重现步骤及错误提示，勿在公开 Issue 中附带个人数据或凭证。
