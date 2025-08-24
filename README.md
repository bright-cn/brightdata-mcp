<p align="center">
  <a href="https://www.bright.cn/ai/mcp-server">
    <img src="https://github.com/user-attachments/assets/c21b3f7b-7ff1-40c3-b3d8-66706913d62f" alt="Bright Data 标志">
  </a>


<h1 align="center">Web MCP</h1>
<h3 align="center">为你的 LLM 和 AI 代理提供实时网页访问能力</h3>

<div align="center">
  
<p align="center">
  <img src="https://img.shields.io/npm/v/@brightdata/mcp?label=version"  
       alt="npm 版本"/>
</p>

<p align="center">
  <img src="https://img.shields.io/npm/dw/@brightdata/mcp"  
       alt="npm 下载量"/>
  <a href="https://smithery.ai/server/@luminati-io/brightdata-mcp">
    <img src="https://smithery.ai/badge/@luminati-io/brightdata-mcp"  
         alt="Smithery 评分"/>
  </a>
</p>

</div>



## 🌟 概览

欢迎使用 Bright Data 官方的 Web MCP 服务器。它通过让 LLM 与 AI 代理能够高效搜索、提取与导航网页，并避免被封锁，从而解决其网页访问问题。Web MCP 支持所有主流 LLM、IDE 与智能体框架（本地、SSE 或可流式 HTTP），让你的工具无缝搜索网络、浏览网站、执行动作并获取数据——且不被封。

🚀 Web MCP 每月包含 5,000 次免费请求——非常适合日常使用与原型化智能体工作流。

![MCP](https://github.com/user-attachments/assets/b949cb3e-c80a-4a43-b6a5-e0d6cec619a7)

> 注意：Web MCP 免费层在前 3 个月每月提供 5,000 次请求。之后需要绑定信用卡，但除非使用了 mcp_browser 或 Web Scrapers 等高级功能，否则不会产生额外费用。



## 目录
- [🎬 演示](#-演示)
- [✨ 功能](#-功能)
- [💡 使用示例](#-使用示例)
- [🚀 使用 Claude Desktop 的快速开始](#-使用-claude-desktop-的快速开始)
- [🔧 可用工具](#-可用工具)
- [⚠️ 安全最佳实践](#%EF%B8%8F-安全最佳实践)
- [🔧 账号设置](#-账号设置)
- [🔌 其他 MCP 客户端](#-其他-mcp-客户端)
- [🎮 试用 Bright Data MCP Playground](#-试用-bright-data-mcp-playgrounds)
- [⚠️ 故障排除](#%EF%B8%8F-故障排除)
- [👨‍💻 参与贡献](#-参与贡献)
- [📞 支持](#-支持)


## 🎬 演示

下面的视频展示了在 Claude Desktop 中的最小用例：

https://github.com/user-attachments/assets/59f6ebba-801a-49ab-8278-1b2120912e33

https://github.com/user-attachments/assets/61ab0bee-fdfa-4d50-b0de-5fab96b4b91d 

更多 YouTube 教程与演示：[Demo](https://github.com/bright-cn/brightdata-mcp/blob/main/examples/README.md)

## ✨ 功能

- 实时网页访问：直接从网络获取最新信息
- 绕过区域限制：不受地理位置限制访问内容
- Web Unlocker：在具备机器人检测的网站上顺畅导航
- 浏览器控制：远程浏览器自动化能力
- 无缝集成：支持所有兼容 MCP 的 AI 助手

## 💡 使用示例

该 MCP 服务可帮助完成的示例查询：

- “在[你所在地区]搜一搜即将上映的电影”
- “特斯拉当前的市值是多少？”
- “今天的维基百科首页条目是什么？”
- “[你的位置]未来 7 天的天气预报？”
- “薪酬最高的 3 位科技公司 CEO，他们的职业生涯各有多长？”

## 与 Cursor 的快速开始

[![安装 MCP Server](https://cursor.com/deeplink/mcp-install-dark.svg)](https://cursor.com/en/install-mcp?name=Bright%20Data&config=eyJjb21tYW5kIjoibnB4IEBicmlnaHRkYXRhL21jcCIsImVudiI6eyJBUElfVE9LRU4iOiI8aW5zZXJ0LXlvdXItYXBpLXRva2VuLWhlcmU%2BIn19)

## 🚀 在 Claude Desktop 上使用托管 MCP 的快速开始

### 通过 Connectors：

1. 打开 Claude Desktop

2. 前往：Settings → Connectors → Add custom connector

3. 选择一个名称，在 “Remote MCP server URL” 中粘贴：

```
https://mcp.brightdata.com/mcp?token=YOUR_API_TOKEN_HERE
```

4. 将 YOUR_API_TOKEN_HERE 替换为第 1 步获取的实际 API token，并点击 “Add”

### 通过 Developer 设置：

1. 打开 Claude Desktop

2. 前往：Settings → Developer → Edit Config

3. 在你的 claude_desktop_config.json 中添加：

```json
{
  "mcpServers": {
    "Bright Data": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://mcp.brightdata.com/mcp?token=YOUR_API_TOKEN_HERE"
      ]
    }
  }
}
```

4. 将 YOUR_API_TOKEN_HERE 替换为第 1 步获取的实际 API token

5. 保存并重启 Claude Desktop

## 💻 在 Claude Desktop 上使用自托管 MCP

### 通过 Claude Desktop 扩展：

1. 下载 Claude Desktop 扩展：  
   [📦 Bright Data 的 MCP 扩展](https://github.com/brightdata/brightdata-mcp/raw/refs/heads/main/brightdata-mcp-extension.dxt)

2. 打开 Claude 并前往：  
   Settings → Extensions

3. 将第 1 步下载的 .dtx 文件拖入投放区域。

4. 启用服务并重启 Claude。

5. 尽情使用！

### 通过 claude_desktop_config.json：

1. 安装 nodejs 以获得 npx 命令（node.js 模块运行器）。安装指南见 [node.js 官网](https://nodejs.org/en/download)

2. 前往 Claude > Settings > Developer > Edit Config > 编辑 “claude_desktop_config.json”，加入以下内容：

```json
{
  "mcpServers": {
    "Bright Data": {
      "command": "npx",
      "args": ["@brightdata/mcp"],
      "env": {
        "API_TOKEN": "<insert-your-api-token-here>"
      }
    }
  }
}
```

#### 🛸 更多高级选项： 

```json
{
  "mcpServers": {
    "Bright Data": {
      "command": "npx",
      "args": ["@brightdata/mcp"],
      "env": {
        "API_TOKEN": "<insert-your-api-token-here>",
        "RATE_LIMIT": "<可选，修改限流格式：limit/time+unit，如 100/1h、50/30m、10/5s>",
        "WEB_UNLOCKER_ZONE": "<可选，覆盖 Web Unlocker 的区域名——默认 mcp_unlocker>",
        "BROWSER_ZONE": "<可选，覆盖 Browser API 的区域名——默认 mcp_browser>",
        "PRO_MODE": "<可选布尔值，默认 false。设为 true 可暴露包括浏览器与 web_data_* 在内的全部工具>"
      }
    }
  }
}
```

## 🔧 可用工具

> 重要：Pro 模式不包含在免费层内，启用将产生额外费用。启用 Pro 模式后可获得全部 60 个工具的访问权限，但请注意相关成本。

启用 Pro 模式：在环境变量中添加 "PRO_MODE"=true。

[可用工具列表](https://github.com/bright-cn/brightdata-mcp/blob/main/assets/Tools.md)

注意：默认仅暴露基础工具（search_engine 与 scrape_as_markdown）。如需访问包括浏览器自动化与网页数据抽取在内的全部工具，请在配置中启用 PRO_MODE（见账号设置部分）。

## ⚠️ 安全最佳实践

重要：务必将抓取到的网页内容视为不受信任的数据。不要将原始抓取内容直接用于 LLM 提示，以避免提示注入风险。  
建议：
- 在处理前先过滤并校验全部网页数据
- 优先使用结构化数据抽取而非原始文本（使用 web_data 工具）

## 🔧 账号设置

1. 确保你拥有 www.bright.cn 的账号（新用户可获得用于测试的免费额度，并支持按需付费）

2. 在[用户设置页面](https://www.bright.cn/cp/setting/users)获取 API Key，或在你收到的欢迎邮件中查找

#### 可选：

3. 启用 Pro 模式（获取全部工具）：
   - 在环境配置中设置 PRO_MODE=true，以访问浏览器自动化、结构化数据抽取与全部可用工具
   - 默认：false（仅暴露 search_engine 与 scrape_as_markdown）
   - 详见上方高级配置示例

4. 配置限流：
   - 设置 RATE_LIMIT 环境变量以控制 API 使用率
   - 格式：limit/time+unit（例如 100/1h 表示每小时 100 次）
   - 支持单位：秒 s、分钟 m、小时 h
   - 示例：RATE_LIMIT=100/1h、RATE_LIMIT=50/30m、RATE_LIMIT=10/5s
   - 限流基于会话（服务器重启后重置）

5. 创建自定义 Web Unlocker 区域：
   - 默认情况下，我们会使用你的 API token 自动创建一个 Web Unlocker 区域
   - 若需更多控制，可在[控制面板](https://www.bright.cn/cp/zones)创建你自己的区域，并通过 WEB_UNLOCKER_ZONE 环境变量指定

6. 创建自定义 Browser API 区域：
   - 默认情况下，我们会使用你的 API token 自动创建一个 Browser API 区域
   - 若需更多控制，可在[控制面板](https://www.bright.cn/cp/zones)创建你自己的区域，并通过 BROWSER_ZONE 环境变量指定

## 🔌 其他 MCP 客户端

要在其他类型的智能体中使用该 MCP 服务器，请根据你的软件进行适配：

- 在运行服务器之前，确保已设置环境变量 API_TOKEN=<your-token>
- 运行 MCP 服务器的完整命令为 npx @brightdata/mcp

#### 💻 macOS / Linux（bash/zsh）

```bash
export API_TOKEN=your-token
npx @brightdata/mcp
```

#### 🪟 Windows（命令提示符）

```cmd
set API_TOKEN=your-token
npx @brightdata/mcp
```

#### 🪟 Windows（PowerShell）

```powershell
$env:API_TOKEN="your-token"
npx @brightdata/mcp
```

> 小贴士：你也可以使用 .env 文件与如 dotenv 之类的工具，在开发期间更轻松地管理环境变量。

---

## 🔄 更新日志

[CHANGELOG.md](https://github.com/bright-cn/brightdata-mcp/blob/main/CHANGELOG.md)

## 🎮 试用 Bright Data MCP Playground

想在无需任何本地配置的情况下试用 Bright Data MCP？

在 Smithery 上查看此 Playground：  
[Smithery](https://smithery.ai/server/@luminati-io/brightdata-mcp/tools)

[![2025-05-06_10h44_20](https://github.com/user-attachments/assets/52517fa6-827d-4b28-b53d-f2020a13c3c4)](https://smithery.ai/server/@luminati-io/brightdata-mcp/tools)

该平台提供了一种无需本地设置即可探索 Bright Data MCP 能力的便捷方式。登录后即可开始尝试网页数据采集！

## ⚠️ 故障排除

### 使用某些工具时的超时

部分工具涉及网页数据读取，在极端情况下页面加载时间可能差异很大。

为确保你的代理能顺利消费数据，请在代理设置中配置足够高的超时时间。

180s 对 99% 的请求应足够，但某些站点较慢，请按需调整。

### spawn npx ENOENT

当系统找不到 npx 命令时会出现此错误。解决方法：

#### 查找 npm/Node 路径

macOS:

```
which node
```

会显示类似 /usr/local/bin/node 的路径

Windows:

```
where node
```

会显示类似 C:\Program Files\nodejs\node.exe 的路径

#### 更新 MCP 配置：

将 npx 命令替换为 Node 的完整路径，例如在 mac 上：

```
"command": "/usr/local/bin/node"
```

## 👨‍💻 参与贡献

我们欢迎一切能改进 Bright Data MCP 的贡献！你可以这样参与：

1. 报告问题：若遇到 Bug 或有功能需求，请在我们的 GitHub 仓库提交 issue。
2. 提交 PR：欢迎 fork 本仓库并提交改进或修复的 Pull Request。
3. 代码风格：所有 JavaScript 代码应遵循 [Bright Data 的 JS 编码规范](https://brightdata.com/dna/js_code)，以确保代码库一致性。
4. 文档：包括本 README 在内的文档改进也非常欢迎。
5. 示例：分享你的使用场景，贡献示例以帮助其他用户。

对于重大改动，请先开 issue 讨论你的提案，以确保方向一致、事半功倍。

## 📞 支持

如遇问题或有疑问，请联系 Bright Data 支持团队，或在仓库中提交 issue。
