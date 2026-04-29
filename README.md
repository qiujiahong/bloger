# Bloger

AI/Agent 技术内容生产工作区，围绕“调研选题 -> 写文章 -> 多平台发布”组织。

## Subagents

项目级 Codex subagents 放在 `.codex/agents/`：

- `topic-researcher`：调研 AI、OpenClaw、Hermes Agent、智能体工程和技术社区趋势，筛选 5 个高潜主题。
- `article-writer`：把选题写成中文技术博客，并规划封面图、内部架构图、逻辑示意图。
- `publisher`：生成微信、华为开发者论坛、小红书发布包。

## 常用请求

```text
使用 subagents 调研今天的 AI/Agent 热门选题，调用 topic-researcher，结合 daily-history、topics、posts、published 去重，给我 5 个最可能爆火的主题。
```

```text
使用 article-writer，把主题《这里填标题》写成一篇技术博客，输出到 posts/YYYY-MM-DD-slug/，同时生成 image-requirements.md。
```

```text
使用 publisher，把 posts/YYYY-MM-DD-slug/blog.md 改写成微信、华为论坛、小红书发布包，输出到 published/YYYY-MM-DD-slug/。
```

## 工作区结构

```text
.codex/agents/   Codex subagent 定义
daily-history/   每日选题、写作、发布历史
topics/          候选主题调研材料
posts/           文章草稿和配图需求
published/       多平台发布包
```
