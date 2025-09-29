<div align="center">
  <a href="https://www.bright.cn/ai/mcp-server">
    <img src="https://github.com/user-attachments/assets/c21b3f7b-7ff1-40c3-b3d8-66706913d62f" alt="Bright Data Logo">
  </a>

  <h1>The Web MCP</h1>
  
  <p>
    <strong>🌐 让你的 AI 拥有实时上网超能力</strong><br/>
    <i>无缝连接 LLM 到实时网络，不再被封锁</i>
  </p>

  <p>
    <a href="https://www.npmjs.com/package/@brightdata/mcp">
      <img src="https://img.shields.io/npm/v/@brightdata/mcp?style=for-the-badge&color=blue" alt="npm version"/>
    </a>
    <a href="https://www.npmjs.com/package/@brightdata/mcp">
      <img src="https://img.shields.io/npm/dw/@brightdata/mcp?style=for-the-badge&color=green" alt="npm downloads"/>
    </a>
    <a href="https://github.com/bright-cn/brightdata-mcp/blob/main/LICENSE">
      <img src="https://img.shields.io/badge/license-MIT-purple?style=for-the-badge" alt="License"/>
    </a>
  </p>

  <p>
    <a href="#-quick-start">快速开始</a> •
    <a href="#-features">功能特性</a> •
    <a href="#-pricing--modes">价格与模式</a> •
    <a href="#-demos">演示</a> •
    <a href="#-documentation">文档</a> •
    <a href="#-support">支持</a>
  </p>

  <div>
    <h3>🎉 <strong>提供免费套餐！</strong> 🎉</h3>
    <p><strong>每月 5,000 次请求免费</strong> <br/>
    <sub>非常适合原型开发与日常 AI 工作流</sub></p>
  </div>
</div>

---

## 🌟 概览

The Web MCP 是为 AI 助手赋予真正「上网能力」的通道。告别过时回答，也不再出现“我无法访问实时信息”的窘境——只需稳定、顺畅、可用的网络访问。

由全球领先的[Bright Data](https://www.bright.cn) Web 数据平台打造，这个 MCP 服务器确保你的 AI 不再被封锁、限流或被验证码拦住。

<div align="center">
  <table>
    <tr>
      <td align="center">✅ <strong>适配任意 LLM</strong><br/><sub>Claude、GPT、Gemini、Llama</sub></td>
      <td align="center">🛡️ <strong>不再被封</strong><br/><sub>企业级解封与反封锁</sub></td>
      <td align="center">🚀 <strong>5,000 次/月免费</strong><br/><sub>按月计</sub></td>
      <td align="center">⚡ <strong>零配置</strong><br/><sub>开箱即用</sub></td>
    </tr>
  </table>
</div>

---

## 🎯 适用场景

- 🔍 实时调研——获取最新价格、新闻与实时数据
- 🛍️ 电商情报——监测产品、价格与库存  
- 📊 市场分析——跟踪竞品与行业趋势
- 🤖 AI 代理——构建真正能「浏览网页」的智能体
- 📝 内容创作——为写作获取最新可信的信息
- 🎓 学术研究——高效汇聚多源公开数据

---

## ⚡ 快速开始


<summary><b>📡 使用托管服务器——无需安装！</b></summary>

零门槛使用，只需在你的 MCP 客户端中添加以下 URL：

```
https://mcp.brightdata.com/mcp?token=YOUR_API_TOKEN_HERE
```

在 Claude Desktop 中设置：
1. 打开：Settings → Connectors → Add custom connector
2. 名称：`Bright Data Web`
3. URL：`https://mcp.brightdata.com/mcp?token=YOUR_API_TOKEN`
4. 点击 “Add”，完成！✨


<summary><b>在本地运行</b></summary>

```json
{
  "mcpServers": {
    "Bright Data": {
      "command": "npx",
      "args": ["@brightdata/mcp"],
      "env": {
        "API_TOKEN": "<your-api-token-here>"
      }
    }
  }
}
```

---

## 🚀 价格与模式

<div align="center">
  <table>
    <tr>
      <th width="33%">⚡ Rapid 模式（免费）</th>
      <th width="33%">💎 Pro 模式</th>
    </tr>
    <tr>
      <td align="center">
        <h3>$0/月</h3>
        <p><strong>5,000 次请求</strong></p>
        <hr/>
        <p>✅ Web 搜索<br/>
        ✅ 使用 Web Unlocker 抓取<br/>
        ❌ 浏览器自动化<br/>
        ❌ Web 数据工具</p>
        <br/>
        <code>默认模式</code>
      </td>
      <td align="center">
        <h3>按量计费</h3>
        <p><strong>包含 Rapid 全部内容 + 60+ 高级工具</strong></p>
        <hr/>
        <p>✅ 浏览器控制<br/>
        ✅ Web 数据 API<br/>
        <br/>
        <br/>
        <br/>
        <code>PRO_MODE=true</code>
      </td>
    </tr>
  </table>
</div>

> 💡 注意：Pro 模式不包含在免费套餐内，按使用量额外计费。

---

## ✨ 功能特性

### 🔥 核心能力

<table>
  <tr>
    <td>🔍 <b>智能网页搜索</b><br/>面向 AI 优化的类 Google 级结果</td>
    <td>📄 <b>干净 Markdown</b><br/>适配 AI 的内容抽取输出</td>
  </tr>
  <tr>
    <td>🌍 <b>全球可达</b><br/>自动绕过地理限制</td>
    <td>🛡️ <b>反机器人与防封</b><br/>不再被封、不再限流</td>
  </tr>
  <tr>
    <td>🤖 <b>浏览器自动化</b><br/>远程控制真实浏览器（Pro）</td>
    <td>⚡ <b>低时延</b><br/>为快速响应优化</td>
  </tr>
</table>

### 🎯 一些“开箱即用”的查询示例

```yaml
✅ “特斯拉当前股价是多少？”
✅ “现在东京评分最高的餐厅有哪些？”
✅ “纽约今天的天气预报是什么？”
✅ “本周有哪些电影上映？”
✅ “今天 Twitter 上的热点话题是什么？”
```

---

## 🎬 演示

> 注：以下视频展示的是早期版本，新的演示即将上线！🎥

<details>
<summary><b>查看演示视频</b></summary>

### 基础网页搜索演示
https://github.com/user-attachments/assets/59f6ebba-801a-49ab-8278-1b2120912e33

### 高级抓取演示
https://github.com/user-attachments/assets/61ab0bee-fdfa-4d50-b0de-5fab96b4b91d

[📺 更多教程（YouTube）→](https://github.com/bright-cn/brightdata-mcp/blob/main/examples/README.md)

</details>

---

## 🔧 可用工具

### ⚡ Rapid 模式工具（默认，免费）

| 工具 | 描述 | 适用场景 |
|------|------|----------|
| 🔍 `search_engine` | 面向 AI 优化的 Web 搜索 | 研究、查证、时事 |
| 📄 `scrape_as_markdown` | 将任意网页转为干净的 Markdown | 内容抽取、文档化 |

### 💎 Pro 模式工具（60+）

<details>
<summary><b>点击查看全部 Pro 工具</b></summary>

| 类别 | 工具 | 描述 |
|------|------|------|
| 浏览器控制 | `scraping_browser.*` | 全功能浏览器自动化 |
| Web 数据 API | `web_data_*` | 结构化数据抽取 |
| 电商 | 产品抓取器 | Amazon、eBay、Walmart 等 |
| 社媒 | 社交抓取器 | Twitter、LinkedIn、Instagram |
| 地图与本地 | 位置工具 | Google 地图、商家数据 |

[📚 查看完整工具文档 →](https://github.com/bright-cn/brightdata-mcp/blob/main/assets/Tools.md)

</details>

---

## 🎮 立即试用！

### 🧪 在线 Playground
无需任何配置，直接体验 Web MCP：

<div align="center">
  <a href="https://www.bright.cn/ai/playground-chat">
    <img src="https://img.shields.io/badge/Try_on-Playground-00C7B7?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyIDJMMyA3VjE3TDEyIDIyTDIxIDE3VjdMMTIgMloiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMiIvPgo8L3N2Zz4=" alt="Playground"/>
  </a>
</div>

---

## 🔧 配置

### 基础配置
```json
{
  "mcpServers": {
    "Bright Data": {
      "command": "npx",
      "args": ["@brightdata/mcp"],
      "env": {
        "API_TOKEN": "your-token-here"
      }
    }
  }
}
```

### 高级配置
```json
{
  "mcpServers": {
    "Bright Data": {
      "command": "npx",
      "args": ["@brightdata/mcp"],
      "env": {
        "API_TOKEN": "your-token-here",
        "PRO_MODE": "true",              // 启用 60+ 全部工具
        "RATE_LIMIT": "100/1h",          // 自定义限速
        "WEB_UNLOCKER_ZONE": "custom",   // 自定义解封 Zone
        "BROWSER_ZONE": "custom_browser" // 自定义浏览器 Zone
      }
    }
  }
}
```

---

## 📚 文档

<div align="center">
  <table>
    <tr>
      <td align="center">
        <a href="https://docs.brightdata.com/mcp-server/overview">
          <img src="https://img.shields.io/badge/📖-API_Docs-blue?style=for-the-badge" alt="API Docs"/>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/bright-cn/brightdata-mcp/blob/main/examples">
          <img src="https://img.shields.io/badge/💡-Examples-green?style=for-the-badge" alt="Examples"/>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/bright-cn/brightdata-mcp/blob/main/CHANGELOG.md">
          <img src="https://img.shields.io/badge/📝-Changelog-orange?style=for-the-badge" alt="Changelog"/>
        </a>
      </td>
      <td align="center">
        <a href="https://www.bright.cn/blog/ai/web-scraping-with-mcp">
          <img src="https://img.shields.io/badge/📚-Tutorial-purple?style=for-the-badge" alt="Tutorial"/>
        </a>
      </td>
    </tr>
  </table>
</div>

---

## 🚨 常见问题与解决方案

<details>
<summary><b>🔧 故障排查指南</b></summary>

### ❌ “spawn npx ENOENT” 错误
解决：安装 Node.js，或使用 node 的完整路径：
```json
"command": "/usr/local/bin/node"  // macOS/Linux
"command": "C:\\Program Files\\nodejs\\node.exe"  // Windows
```

### ⏱️ 复杂站点超时
解决：在客户端设置中将超时提高到 180s

### 🔑 鉴权问题
解决：确认 API Token 有效且具备相应权限

### 📡 远程连接问题
解决：检查网络与防火墙设置

[更多排查 →](https://github.com/bright-cn/brightdata-mcp#troubleshooting)

</details>

---

## 🤝 参与贡献

我们欢迎各种形式的贡献：

- 🐛 [提交 Bug](https://github.com/bright-cn/brightdata-mcp/issues)
- 💡 [功能建议](https://github.com/bright-cn/brightdata-mcp/issues)
- 🔧 [提交 PR](https://github.com/bright-cn/brightdata-mcp/pulls)
- ⭐ 欢迎为本仓库加星！

请遵循 [Bright Data 的代码规范](https://www.bright.cn/dna/js_code)。

---

## 📞 支持

<div align="center">
  <table>
    <tr>
      <td align="center">
        <a href="https://github.com/bright-cn/brightdata-mcp/issues">
          <strong>🐛 GitHub Issues</strong><br/>
          <sub>提交问题与需求</sub>
        </a>
      </td>
      <td align="center">
        <a href="https://docs.brightdata.com/mcp-server/overview">
          <strong>📚 文档</strong><br/>
          <sub>完整指南</sub>
        </a>
      </td>
      <td align="center">
        <a href="mailto:support@brightdata.com">
          <strong>✉️ 邮件</strong><br/>
          <sub>support@brightdata.com</sub>
        </a>
      </td>
    </tr>
  </table>
</div>

---

## 📜 许可证

MIT © [Bright Data Ltd.](https://www.bright.cn)

---

<div align="center">
  <p>
    <strong>由 ❤️ 驱动</strong><br/>
    <a href="https://www.bright.cn">
      <img src="https://idsai.net.technion.ac.il/files/2022/01/Logo-600.png" alt="Bright Data" height="30"/>
    </a>
  </p>
  <p>
    <sub>全球第一的 Web 数据平台</sub>
  </p>
  
  <br/>
  
  <p>
    <a href="https://github.com/bright-cn/brightdata-mcp">⭐ 欢迎为本仓库加星</a> • 
    <a href="https://www.bright.cn/blog">阅读我们的博客</a>
  </p>
</div>
