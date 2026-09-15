# 小黑日报助手

本仓库用于发布小黑日报助手安装包。

## 下载 1.7.1

| 系统 | 国内加速 | 原始链接 |
| --- | --- | --- |
| Windows | [加速下载](https://ghfast.top/https://github.com/shjiyue/xiaoheiribao/releases/download/v1.7.1/XiaoheiDailyAssistant-Setup-1.7.1.exe.zip) | [GitHub 下载](https://github.com/shjiyue/xiaoheiribao/releases/download/v1.7.1/XiaoheiDailyAssistant-Setup-1.7.1.exe.zip) |
| macOS · Apple 芯片 | [加速下载](https://ghfast.top/https://github.com/shjiyue/xiaoheiribao/releases/download/v1.7.1/XiaoheiDailyAssistant-1.7.1-mac-arm64.dmg.zip) | [GitHub 下载](https://github.com/shjiyue/xiaoheiribao/releases/download/v1.7.1/XiaoheiDailyAssistant-1.7.1-mac-arm64.dmg.zip) |
| macOS · Intel 芯片 | [加速下载](https://ghfast.top/https://github.com/shjiyue/xiaoheiribao/releases/download/v1.7.1/XiaoheiDailyAssistant-1.7.1-mac-x64.dmg.zip) | [GitHub 下载](https://github.com/shjiyue/xiaoheiribao/releases/download/v1.7.1/XiaoheiDailyAssistant-1.7.1-mac-x64.dmg.zip) |

[查看全部版本](https://github.com/shjiyue/xiaoheiribao/releases)

下载后请先解压：Windows 运行 `.exe` 安装程序；Mac 打开 `.dmg`，按提示安装。
Mac 用户请根据「关于本机」中的芯片信息选择 Apple 芯片版或 Intel 芯片版。

加速链接使用第三方服务 ghfast；如暂时不可用，可尝试 GitHub 原始链接。

## 文件校验

安装包 ZIP 的 SHA-256 可在对应 Release 的 [SHA256SUMS.txt](https://github.com/shjiyue/xiaoheiribao/releases/download/v1.7.1/SHA256SUMS.txt) 中查看。

## 自动更新

当前 Release 提供手动下载安装包。客户端自动更新接入需要另行配置更新地址，并上传同次构建生成的更新文件：

- Windows：安装程序 `.exe`、`latest.yml` 和对应的 `.blockmap`。
- macOS：包含 `.app` 的更新 ZIP、对应的 `latest-mac.yml` 及构建生成的 `.blockmap`，按芯片架构分别发布。

本页提供的 `.dmg.zip` 是 Mac 安装镜像的压缩包，不能替代客户端自动更新所需的应用 ZIP。
