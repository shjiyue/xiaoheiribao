# 小黑日报助手

小黑日报助手是一款帮助你**自动理解每天做了什么**的桌面效率工具：自动记录工作轨迹，用 AI 理解工作内容，生成日报周报、提取待办，并把下一步计划接回你的工作流。

官网：[www.xiaoheiribao.com](https://www.xiaoheiribao.com)

> **本仓库仅用于发布桌面端安装包与版本更新说明，不包含产品源代码。**

## 产品能力

### 自动记录并理解工作

截图、应用活动、文本、剪贴板、图片和音视频都能形成工作记录。在不打断工作的情况下持续记录屏幕与应用活动，AI 识别你正在处理的事情，结合个人记忆和自定义分类，整理成清晰的工作时间线。

### 日报、周报、月报一键生成

根据真实工作时间线生成报告，支持自定义模板与模板市场。查看工作时间线、应用使用、热力图、分类分布、词云和专注时段，按天、周或月汇总工作成果，下班前选择模板即可生成可直接交付的日报。

### 从工作记录到下一步行动

AI 从时间线中提取待办，并结合后续工作记录辅助评估完成情况。用自然语言创建、修改和完成待办，让复盘真正推动事情向前。

### 超能伙伴：带着工作背景，在对话中接着做

同一客户端内的超能伙伴可查询工作时间线、历史报告与应用统计，在对话里梳理进展、生成日报周报。支持按职责创建专属伙伴、多伙伴协作、文件处理与定时任务，让工作记忆成为对话的背景。

### 本地优先

工作记录默认保存在本地；在线 AI 能力会将相关内容发送至你所选的模型服务。通过本地服务开放 API，供本地 Agent 查询时间线、报告、应用统计和待办。

## 下载安装包

选择适合你电脑的版本，点击后从本仓库 [Releases](https://github.com/shjiyue/xiaoheiribao/releases) 下载 ZIP 安装包：

| 系统 | 适用设备 | 安装包 |
| --- | --- | --- |
| Windows | 64 位 Windows 电脑 | [下载 Windows 版](https://github.com/shjiyue/xiaoheiribao/releases/download/v1.8.3/XiaoheiDailyAssistant-Setup-1.8.3.exe.zip) |
| macOS · Apple 芯片 | 搭载 M 系列芯片的 Mac | [下载 Mac Apple 芯片版](https://github.com/shjiyue/xiaoheiribao/releases/download/v1.8.3/XiaoheiDailyAssistant-1.8.3-mac-arm64.dmg.zip) |
| macOS · Intel 芯片 | 搭载 Intel 处理器的 Mac | [下载 Mac Intel 芯片版](https://github.com/shjiyue/xiaoheiribao/releases/download/v1.8.3/XiaoheiDailyAssistant-1.8.3-mac-x64.dmg.zip) |

### 安装方法

1. 下载上表对应的 ZIP 安装包并解压。
2. **Windows：** 双击解压后的 `.exe`，按提示完成安装。
3. **Mac：** 打开解压后的 `.dmg`，将「小黑日报助手」拖入「应用程序」文件夹，再从「应用程序」启动。

不确定 Mac 的芯片类型？点击屏幕左上角 ** → 关于本机**：显示「Apple M…」请选择 Apple 芯片版，显示「Intel」请选择 Intel 芯片版。

<details>
<summary>文件校验（可选）</summary>

上表三个 ZIP 安装包的 SHA-256 校验值见 [INSTALLER-ZIP-SHA256SUMS.txt](https://github.com/shjiyue/xiaoheiribao/releases/download/v1.8.3/INSTALLER-ZIP-SHA256SUMS.txt)。

</details>

## 小黑日报助手 Lite

小黑日报助手 Lite 是独立的轻量桌面应用，专注于「自动记录工作 → 本地保存时间线 → 供其他 Agent 查询」。如果你主要需要回顾每天做了什么，或希望现有的 AI Agent 结合真实工作记录生成日报、周报，可以选择 Lite。

### 基础功能

- **自动记录**：按设定间隔截取选中的显示器，调用视觉模型生成文字记录；支持回车键触发记录、闲置暂停、画面去重与焦点窗口特写。
- **记忆时间线**：按日期、分类和关键词查看记录，支持编辑、删除及复制文字。
- **工作概览与热力图**：查看每日记录、活跃时长、主要分类，以及时段和年度热力图。
- **模型用量统计**：查看调用记录、Token 用量与失败情况。
- **Agent 接入**：通过仅监听本机的 HTTP API 查询时间线、每日概览和热力图，也可由 Agent 写入记录；「Skill 调用」页提供接入说明。
- **日常使用**：托盘后台运行、开机自启、可选截图留存、性能监控和运行日志；可选通过 Hook 上报记录。

### 与小黑日报助手的区别

Lite 聚焦记录、查询和基础统计，不包含小黑日报助手中的内置 Bot 对话、多 Bot 协作、待办管理、报告模板市场及音视频等多种记录入口。Lite 本身不内置日报、周报生成页面，可由你正在使用的 Agent 查询记录后生成报告。

Lite 使用 Rust + GPUI 开发，支持 macOS 和 Windows。模型服务需自行配置 API Key、接口地址和支持图片识别的模型；模型费用由对应服务商收取。时间线和配置保存在本机，截图识别会发送到你配置的模型服务；截图默认不落盘，可在设置中开启保存。开启 Hook 后，记录也会按设置上报到指定地址。

Lite 使用独立的机器授权与免费试用机制，实际试用次数、价格及可购买方案以应用内显示为准；启动和使用期间需要联网校验授权。无需登录账号，现有小黑日报助手的账号或订阅不会自动转为 Lite 授权。

### Lite 0.1.0 下载

Lite 使用独立的 `lite-v` 前缀发布版本，与原有小黑日报助手的 Release 分开命名。原有版本名称和下载入口保持不变。

| 系统 | 适用设备 | 下载 |
| --- | --- | --- |
| Windows | x64 Windows 电脑 | [下载 Lite Windows x64](https://github.com/shjiyue/xiaoheiribao/releases/download/lite-v0.1.0/xiaohei-lite-0.1.0-windows-x64.zip) |
| macOS | Apple M 系列芯片 | [下载 Lite macOS Apple 芯片版](https://github.com/shjiyue/xiaoheiribao/releases/download/lite-v0.1.0/xiaohei-lite-0.1.0-macos-arm64.zip) |
| macOS | Intel 处理器 | [下载 Lite macOS Intel 版](https://github.com/shjiyue/xiaoheiribao/releases/download/lite-v0.1.0/xiaohei-lite-0.1.0-macos-x86_64.zip) |

解压 ZIP 后，Windows 双击 `.exe` 即可运行；macOS 建议将 `.app` 拖入「应用程序」后启动，两个 Mac 版本均已完成 Developer ID 签名及 Apple 公证。首次使用请配置模型并按提示授予系统权限。关闭窗口后仍在托盘运行，退出请使用托盘菜单。

更新前先彻底退出旧版本，再替换程序文件；配置和历史记录保存在用户数据目录。此仓库本次仅提供 Lite 说明与安装包，不包含 Lite 源码。
