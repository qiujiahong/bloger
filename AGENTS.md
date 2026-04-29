# Bloger Agent Workflow

本仓库用于 AI/Agent 技术内容的选题、写作和多平台发布。处理内容生产任务时，优先使用项目级 Codex subagents。

## Subagents

- `topic-researcher`：调研 AI、OpenClaw、Hermes Agent、智能体工程和技术社区趋势，结合历史主题筛选 5 个高潜选题。
- `article-writer`：把已选主题写成去 AI 味、易传播的中文技术博客，并规划封面图、架构图、逻辑示意图。
- `publisher`：把成稿改写成微信、华为开发者论坛、小红书发布包，并生成检查清单。

## Default Flow

1. 需要“今天写什么/选题/热点/爆款方向”时，调用 `topic-researcher`。
2. 用户选定主题后，调用 `article-writer` 生成 `posts/YYYY-MM-DD-slug/blog.md` 和 `image-requirements.md`。
3. 文章确认后，调用 `publisher` 生成 `published/YYYY-MM-DD-slug/` 下的平台发布包。
4. 任何阶段都要读取历史记录，避免短期重复主题、重复标题和重复平台表达。

## Repository Structure

- `.codex/agents/`：Codex subagent 定义。
- `daily-history/`：每日选题和发布历史。
- `topics/`：候选主题研究材料。
- `posts/`：文章草稿和配图需求。
- `published/`：多平台发布包和发布记录。

## Quality Bar

- 趋势判断必须有证据；没有证据就标注“待验证”。
- 技术文章必须具体、可验证、少模板腔。
- 发布包不能声称已经完成发布，只能生成可执行素材和人工检查项。
