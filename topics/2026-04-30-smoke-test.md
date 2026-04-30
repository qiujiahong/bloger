# 今日候选主题

调研日期：2026-04-30

## 历史去重摘要

- `daily-history/2026-04-29.md` 仅记录“初始化 Bloger subagents 工作区”，没有已有选题、已写文章或已发布内容。
- `topics/`、`posts/`、`published/` 当前只有 README，没有历史主题沉淀。
- 同级本地项目检查：`/Users/jgdt/Desktop/codes/openclaw` 不存在，OpenClaw 只能联网验证；`/Users/jgdt/Desktop/codes/hermes-agent` 存在，含 `hermes-agent-install-blog.md`，可作为 Hermes Agent 文章素材基础。

## 1. Codex 正在从 CLI 变成工程团队的“Agent 工作台”

### 标题建议

1. `Codex 不是命令行玩具了：从 CLI 到团队 Agent 工作台的 5 个变化`
2. `GPT-5.5 时代的 Codex：工程师该重新理解“结对编程”了`

### 一句话判断

Codex 在 4 月底高频发版，同时 OpenAI 官方把 Codex、GPT-5.5、浏览器使用、代码审查和 IDE/CLI 工作流放在同一叙事里，适合今天写一篇“从工具升级到工程工作台”的趋势稿。

### 趋势证据

- OpenAI 官方 Codex 文档显示 Codex CLI 与 IDE extension 同属 Codex 产品线，可在本地代码库中读取、修改和运行代码；链接：https://developers.openai.com/codex/cli/
- OpenAI 官方发布页在 2026-04-16 发布“Codex for teams”，介绍 GPT-5.5、Code Red、安全审查、PR 评论等团队工程能力；链接：https://openai.com/index/codex-for-teams/
- GitHub `openai/codex` releases 在 2026-04-29 连续发布 `rust-v0.126.0-alpha.12` 到 `rust-v0.126.0-alpha.16`；链接：https://github.com/openai/codex/releases

### 文章角度

主线：不要复述“又发了一个 AI 编程工具”，而是拆 Codex 的产品形态变化：CLI、IDE、浏览器、PR review、长任务、团队策略如何合并成一个工程闭环。

读者收益：帮助开发者判断 Codex 适合放在哪些环节：需求澄清、代码修改、测试、review、文档、自动化排障。

适合平台：微信技术号、掘金、华为开发者论坛。

### 去重检查

历史目录无相似主题。与 Hermes/OpenClaw 方向不冲突，可作为“大厂 Agent 工程化”主线。

### 爆火概率

★★★★★

理由：官方更新强、工程人群关注度高、可以写出实操判断，不容易沦为新闻搬运。

## 2. MCP 进入“注册表 + 供应链安全”阶段

### 标题建议

1. `MCP 真正的风险不是连接工具，而是你信任了谁的工具`
2. `从 MCP Registry 看 Agent 工程的下一道门槛：工具供应链`

### 一句话判断

MCP 已经从“怎么接工具”进入“怎么发现、分发、信任和治理工具”的阶段，今天适合写一篇面向工程落地的安全与治理文章。

### 趋势证据

- GitHub `modelcontextprotocol/registry` 描述为 MCP servers 的社区驱动注册表服务，2026-04-29 仍有更新，约 6.7k stars；链接：https://github.com/modelcontextprotocol/registry
- MCP 官方文档已将 registry、server discovery、authorization 等列为生态基础设施；链接：https://modelcontextprotocol.io/
- GitHub Security Lab 曾披露 MCP 相关风险，核心问题包括工具投毒、提示注入与跨工具越权，适合扩展到供应链治理视角；链接：https://github.blog/security/vulnerability-research/

### 文章角度

主线：从“装 MCP server”切入，解释企业或个人 Agent 真正需要的 5 层防线：来源可信、权限最小化、输入隔离、审计日志、可撤销授权。

读者收益：读者可以拿到一份 MCP server 选型和接入检查清单。

适合平台：微信、华为开发者论坛、掘金。

### 去重检查

历史目录无 MCP 主题。与 Codex 主题有关联，但角度从产品趋势转向工具供应链安全。

### 爆火概率

★★★★☆

理由：MCP 讨论热度稳定，安全角度有传播钩子；但需要避免空泛恐慌，必须给出可执行检查表。

## 3. OpenClaw 的爆点不是“又一个 Agent”，而是第三方 Harness 的安全边界

### 标题建议

1. `OpenClaw 给所有 Agent 工具提了个醒：第三方 Harness 到底该信任什么`
2. `把 Claude Code 接进 OpenClaw 后，安全边界会发生什么变化？`

### 一句话判断

OpenClaw 星标和更新频率极高，同时围绕 Claude Code、浏览器 MCP、Feishu/Telegram gateway 的改动密集，适合写“多入口 Agent 工具的安全边界”。

### 趋势证据

- 本地验证：`/Users/jgdt/Desktop/codes/openclaw` 不存在，无法检查本地源码或配置。
- GitHub API 显示 `openclaw/openclaw` 约 366k stars，2026-04-29 仍有提交更新；链接：https://github.com/openclaw/openclaw
- 2026-04-29 最新 issues/PR 里出现 `fix(telegram,feishu): enable Claude CLI reasoning via reasoningDefault config`、`fix(browser): read Chrome MCP screenshot extension`、`fix(gateway): add cron-list transport timing diagnostics` 等，说明消息网关、浏览器、MCP、Claude CLI 集成仍在快速变化；链接：https://github.com/openclaw/openclaw/issues

### 文章角度

主线：不写 OpenClaw 安装教程，而写“第三方 Agent harness 如何定义信任边界”：它可以包住 Claude Code、浏览器、消息平台、定时任务，但也会把权限、日志、密钥、远程入口聚在一起。

读者收益：理解 OpenClaw 这类工具为什么诱人，以及在本机或服务器部署前要检查哪些安全点。

适合平台：微信、小红书技术向、华为开发者论坛。

### 去重检查

历史目录无 OpenClaw 主题。需要注意：因本地项目缺失，正文必须继续联网核验具体功能，避免过度断言。

### 爆火概率

★★★★☆

理由：OpenClaw 数据和冲突感都强，标题有传播性；风险在于项目真实性、功能细节和安全争议必须继续核实。

## 4. Hermes Agent：个人 Agent 工作台的“消息入口”比 CLI 更关键

### 标题建议

1. `我更看好带消息入口的个人 Agent：Hermes Agent 的真正价值不在终端`
2. `从终端到飞书：Hermes Agent 为什么像一个个人 AI 操作系统`

### 一句话判断

Hermes Agent 本地已有安装与飞书接入素材，GitHub 侧也显示极高热度和持续更新，适合写一篇偏实战的“个人 Agent 常驻化”文章。

### 趋势证据

- 本地文件 `/Users/jgdt/Desktop/codes/hermes-agent/hermes-agent-install-blog.md` 已记录 Hermes Agent 安装、模型配置、skills、长期记忆、gateway、飞书/Lark 接入等内容。
- GitHub API 显示 `NousResearch/hermes-agent` 约 125k stars、2026-04-29 仍有更新，描述为“The agent that grows with you”；链接：https://github.com/NousResearch/hermes-agent
- 本地稿件中已有命令和排障素材，例如 `hermes setup gateway`、`hermes gateway status`、`hermes pairing approve feishu ...`，具备快速成文基础。

### 文章角度

主线：把 Hermes 放在“个人 AI Agent 工作台”的语境里讲：CLI 只是调试入口，消息平台才是日常触达入口，skills 和记忆负责长期复用。

读者收益：读者能判断自己是否需要常驻 Agent，以及如何从本机 CLI 走到 Feishu/Lark 后台服务。

适合平台：微信、少数派、掘金、小红书技术向。

### 去重检查

历史目录无相似主题。本地已有长稿，后续 article-writer 可改成更自然、更传播的中文技术博客。

### 爆火概率

★★★★☆

理由：实操基础强、读者收益清晰；传播热度略低于 Codex，但更容易写出差异化体验。

## 5. CLI Agent 发版竞赛：Codex、Claude Code、Gemini CLI 都在抢“工程入口”

### 标题建议

1. `AI 编程工具的下一战：谁能成为工程师每天打开的第一个 CLI？`
2. `Codex、Claude Code、Gemini CLI 连续发版，真正该比较的不是模型分数`

### 一句话判断

多个头部 CLI Agent 在 4 月底高频更新，适合写一篇横向比较：工程入口、权限模型、扩展生态、自动化能力，而不是只比模型强弱。

### 趋势证据

- GitHub `openai/codex` 在 2026-04-29 连续发布多个 `rust-v0.126.0-alpha.*` 版本；链接：https://github.com/openai/codex/releases
- GitHub `anthropics/claude-code` 在 2026-04-28 至 2026-04-29 发布 `v2.1.121`、`v2.1.122`、`v2.1.123`；链接：https://github.com/anthropics/claude-code/releases
- GitHub `google-gemini/gemini-cli` 在 2026-04-28 至 2026-04-29 发布 `v0.40.0`、`v0.41.0-preview.0`、`v0.42.0-nightly...`；链接：https://github.com/google-gemini/gemini-cli/releases

### 文章角度

主线：用“工程入口”替代“谁更聪明”：比较三类 CLI Agent 在上下文管理、权限确认、MCP/工具生态、review、自动化、团队协作上的产品取舍。

读者收益：给个人开发者和小团队一份选择框架，知道什么时候该用哪个工具，什么时候不要把所有流程都交给 Agent。

适合平台：微信、掘金、华为开发者论坛。

### 去重检查

历史目录无横评主题。与 Codex 单篇主题重合度较高，如果今天只写一篇，建议优先写 Codex 深挖；横评可作为后续第二篇。

### 爆火概率

★★★★☆

理由：横评天然有点击率；缺点是需要继续补齐实际体验，否则容易变成版本号罗列。

# 最推荐

最推荐今天优先写：**Codex 正在从 CLI 变成工程团队的“Agent 工作台”**。

原因：

1. 时效最好：OpenAI 官方在 2026-04-16 已经给出团队化叙事，GitHub releases 在 2026-04-29 仍高频更新，今天写正合适。
2. 传播钩子强：不是“某工具更新了”，而是“AI 编程工具从个人 CLI 进入团队工程流程”，更适合中文技术社区讨论。
3. 可验证材料多：官方文档、官方发布页、GitHub releases 都能支撑，不需要依赖传闻。
4. 后续可扩展：写完 Codex 后，可以自然接第二篇 MCP 供应链安全，或第三篇 CLI Agent 横评。
