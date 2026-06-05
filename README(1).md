@ -1,190 +0,0 @@
# OpenClaw Windows（虾壳云）

Windows 上的一键 AI 助手部署工具。下载、解压、启动，按界面引导完成部署，即可在本机运行 OpenClaw Gateway，并通过图形界面管理模型、插件、渠道和 Agent。

官网下载：[https://xiake.yun/api/download/package/17?promoCode=IVD643FDE29A](https://xiake.yun/api/download/package/17?promoCode=IVD643FDE29A)

---

## 为什么选择虾壳云

OpenClaw 功能强大，但手动部署对普通用户并不友好：需要安装 Node.js、Git、Python，处理依赖、环境变量、模型配置、插件和渠道接入。虾壳云把这些步骤收进一个 Windows 桌面应用里，让部署和日常使用更直观。

| 你原本需要处理 | 虾壳云帮你处理 |
|---|---|
| 安装运行环境 | 内置便携运行环境，自动检查和修复 |
| 下载依赖和构建界面 | 安装流程自动完成 |
| 启动 Gateway 服务 | 桌面应用自动托管 |
| 修改配置文件 | 设置中心图形化配置 |
| 排查启动失败 | 安装日志、Gateway 日志和诊断入口可见 |
| 对接聊天渠道 | 渠道管理页提供安装和配置入口 |

---

## 快速开始

### 1. 下载

访问官网下载安装包：

[https://xiake.yun/api/download/package/17?promoCode=IVD643FDE29A](https://xiake.yun/api/download/package/17?promoCode=IVD643FDE29A)

### 2. 解压或安装

如果下载到的是便携版 zip：

1. 解压到纯英文路径，例如 `D:\OpenClaw-Windows\`。
2. 打开 `Openclaw-win-版本号-xk` 或类似目录。
3. 双击 `Openclaw Windows.exe`。

如果下载到的是安装包，直接双击安装并按提示启动。

### 3. 开始部署

启动后点击“开始安装”，选择 OpenClaw 安装目录，等待部署完成。安装完成后进入主界面，在“设置 -> API 配置”中填写模型服务信息即可开始使用。

---

## 核心能力

### 一键部署

虾壳云会自动完成环境检测、运行依赖准备、OpenClaw Gateway 安装、Control UI 构建、运行时配置生成和服务启动。

### 图形化配置

常用设置集中在桌面应用中：

- 模型 API Key、Base URL 和模型列表
- Agent 创建、编辑和切换
- Skills 查看和安装
- 渠道插件安装、配置和启停
- 权限、工具和扩展命令管理

### 内置聊天界面

安装完成后可直接进入聊天界面，支持流式响应、Markdown、代码块和公式渲染。Gateway 由应用自动管理，无需每次手动打开命令行。

### 渠道接入

当前重点支持：

| 渠道 | 场景 |
|------|------|
| 微信 | 个人微信扫码登录和消息接入 |
| 钉钉 | 企业内部机器人 |
| 企业微信 | 企业微信智能体或机器人 |
| 飞书 | 飞书企业自建应用或机器人 |
| QQ Bot | QQ 官方机器人 |

部分渠道需要先在对应开放平台创建应用或机器人，并按平台要求配置回调、权限和凭证。

### 多模型支持

通过 OpenClaw Gateway，可统一接入多种模型服务：

- OpenAI / OpenAI 兼容接口
- Azure OpenAI
- Claude
- Gemini
- DeepSeek
- Qwen / 通义千问 / 阿里百炼
- 智谱 GLM / Z.AI
- MiniMax
- Kimi / Moonshot
- Ollama / LM Studio / llama.cpp
- 其他兼容 OpenAI 接口的云端或本地模型

实际可用模型取决于用户自己的模型服务账号、API Key 和网络环境。

---

## 适合谁使用

- 想在 Windows 上快速体验 OpenClaw 的个人用户
- 不想折腾命令行和依赖环境的普通用户
- 需要统一管理多个模型服务的 AI 使用者
- 需要把 AI 助手接入企业 IM 或机器人渠道的团队
- 想用 Skills、Agent 和扩展命令提升日常工作效率的用户

---

## 系统要求

| 项目 | 要求 |
|------|------|
| 操作系统 | Windows 10 / 11 x64 |
| 内存 | 至少 4 GB |
| 磁盘空间 | 建议预留 2 GB 以上 |
| 网络 | 首次安装和更新阶段需要联网 |
| WebView2 | 桌面界面依赖 Microsoft Edge WebView2 Runtime |

说明：

- 安装包会尝试自动处理 WebView2 Runtime。
- 便携版需要当前 Windows 账户已有可用的 WebView2 环境。
- 建议将程序放在纯英文路径中运行。
- 不要直接在压缩包预览窗口、网盘同步目录或 OpenClaw 安装目录内部运行启动器。

---

## 常见问题

### 安装需要多久？

通常需要3-10分钟，具体取决于网络速度、磁盘速度和安全软件扫描情况。

### 安装卡住怎么办？

先查看安装界面日志。常见原因包括网络超时、下载源不可用、安全软件拦截、WebView2 缺失、系统运行库缺失或安装路径不合适。

可以尝试：

1. 换到纯英文路径重新解压。
2. 确认网络可用。
3. 临时放行安全软件。
4. 重启应用后重新安装。
5. 导出日志后联系支持。

### 为什么提示 WebView2 缺失？

OpenClaw Windows 使用 WebView2 显示桌面界面。如果系统缺少该组件，应用会提示安装。安装包会尝试自动补齐；便携版可能需要用户手动安装。

### 支持 macOS 吗？

当前公开下载和使用说明主要面向 Windows 10 / 11 x64。其他平台版本以官网实际发布为准。

### API Key 存在哪里？

模型服务配置保存在本机配置目录中，用于驱动本地 OpenClaw Gateway。请妥善保存自己的 API Key，不要把配置文件或日志发给不可信人员。

### 可以同时启用多个渠道吗？

可以。微信、钉钉、企业微信、飞书、QQ Bot 等渠道可以按需安装和启用。实际可用性取决于插件状态、平台凭证和 Gateway 是否在线。

### 服务使用有什么注意事项？

下载安装包本身可免费获取。软件中的账号服务、模型调用、额度、增值服务或商业支持，以官网、应用内提示和实际服务规则为准。

---

## 数据与隐私

虾壳云在本机运行 OpenClaw Gateway。AI 对话会根据用户选择的模型服务发送到对应模型供应商。应用可能连接服务端获取公告、版本、更新、账号状态和服务配置等必要信息。

使用建议：

- 使用自己的模型服务账号和 API Key。
- 不要共享激活信息、API Key、渠道凭证或完整日志。
- 企业使用时建议使用独立账号和最小权限配置。

---

## 关于

OpenClaw Windows（虾壳云）基于 OpenClaw 生态构建，目标是让 Windows 用户更轻松地部署、管理和使用 OpenClaw Gateway。

- 官网与下载：[https://xiake.yun/api/download/package/17?promoCode=IVD643FDE29A](https://xiake.yun/api/download/package/17?promoCode=IVD643FDE29A)
- OpenClaw 项目：[https://github.com/openclaw/openclaw](https://github.com/openclaw/openclaw)

遇到安装、启动、渠道配置或模型配置问题时，请通过官网提供的渠道联系支持，并附上错误截图和日志。