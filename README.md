# Claude Code / CC / ClaudeCode

## Claude Code + Kimi K2

使用 Gemini CLI 查找 ~/.claude/settings.json 并且打开

终端编程很多人对前端的知识不懂，后边我写一篇有关运行时相关的博客，请保持关注。

说正题：Claude Code + Kimi 怎么配置？怎么搞？很简单，没心智负担。

[ 1 ] 你已经安装了 Claude Code ，如果你没安装你用个啥。

[ 2 ] 你的Claude Code 没充值，或者到期了，你都买了20美元的Pro，你为啥使用 Kimi K2。

[ 3 ] 你得充值一下 Kimi , 充个50元人民币吧，先用着，慢，没事，先用着。

[ 4 ] 找一下你的key ，这是 env.ANTHROPIC_AUTH_TOKEN 的值

[ 5 ] 找一下 base URL 的值，我去，你在月之暗面的哪个域名下买的，你就用哪个啊base URL 啊。人家两个域名呢：
https://api.moonshot.ai/anthropic
https://api.moonshot.cn/anthropic
这个是 env.ANTHROPIC_BASE_URL 值。

[ 6 ] 找到 CC 的配置文件 ~/.claude/settings.json
配置进去就行了呀。

![alt text](image.png)

## CC发展史

```
timeline
    title Claude Code 发展时间线

    section 2025年2月
        2025-02-24 : 研究预览版首次发布
                   : 与Claude 3.7 Sonnet同时发布
                   : 终端代理编程工具

    section 2025年5月
        2025-05-22 : 正式版(GA)发布
                   : 从研究预览转为正式可用

    section 2025年6月
        2025-06-04 : 支持Pro和Max计划
                   : 扩大用户覆盖范围
        2025-06-11 : SDK发布
                   : TypeScript和Python支持
        2025-06-18 : MCP服务器支持
                   : SSE和HTTP传输
                   : OAuth 2.0认证
        2025-06-30 : Hooks功能
                   : 社区反馈驱动的功能
```

## Claude Code 本质

Claude Code 的本质是一个 npm 的包。如果你对趋势感兴趣可以在下述网站查阅安装趋势

- https://npmjs.com/package/@anthropic-ai/claude-code?activeTab=versions
- https://npmtrends.com/@anthropic-ai/claude-code
- https://npm-stat.com/charts.html?package=%40anthropic-ai%2Fclaude-code&from=2025-02-23&to=2025-07-05
- https://npmcharts.com/compare/@anthropic-ai/claude-code?interval=1&log=false

使用代理搜索，无需手动选择上下文即可理解您的整个代码库

## 常用的 commands

| Command                      | Description        |
| ---------------------------- | ------------------ |
| claude "fix the build error" | 执行一次任务       |
| claude -p "解释一下函数"     | 运行一次查询就退出 |
| claude -c                    | 继续最近的对话     |

# Gemini CLI

在2025年06月25的时候，谷歌发了 Gemini CLI。虽然谷歌这一路走的很飘逸：在AI编程的这个产品方向上一会又是在浏览器中的，一会又在终端的，一会又是插件呢，一会又扩展。不过作为Claude Code 竞品，不发也不行。

因为是终端操作，所以终端记得代理一下，然后代理节点开一下。因为是npm 包，你需要在终端执行：

```sh
npm install -g @google/gemini-cli@latest。
```

有的小伙伴可能不是前端，我来解释一下：

npm 是个Node.js 的官方的包管理 https://nodejs.org/en/learn/getting-started/an-introduction-to-the-npm-package-manager
install 安装 ，-g 是全局安装的意思， @latest 总是安装最新的就好

@google/gemini-cli 是一个包https://npmjs.com/package/@google/gemini-cli?activeTab=versions

接着你执行 gemini 。可能Gemini 登录的时候有问题。
echo 'export GOOGLE_CLOUD_PROJECT="你的ID"' >> ~/.bashrc

把GOOGLE_CLOUD_PROJECT写到环境变量中即可。

主要是执行一些翻译任务。不仅仅是代码。

# Amp

Amp 是 Sourcegraph 构建的一个代理式编码工具。an agentic coding tool

```sh
npm install -g @sourcegraph/amp@latest
```

第一性原理：您并不是在使用 Amp——您是在直接与模型对话
