# Digital Persona Plugin

> 不是让 AI 假装成为一个人，而是让一个人的思考痕迹拥有可延续的结构。

Digital Persona Plugin 是一个面向 Codex、Claude Code、OpenCode 等 AI 工具的跨平台人格记忆插件系统。它希望把用户与 AI 的每一次交互沉淀为结构化 Markdown：问题、意图、知识、偏好、习惯、判断方式、工具选择和长期目标。

这些 Markdown 不是普通日志。它们是一个精神体的神经元。

随着交互持续发生，系统会逐渐形成一个可管理、可召回、可迁移、可演化的数字人格。它既能作为 AI 工具的上下文记忆层，也能通过桌面程序被用户查看、编辑、连接和可视化，最终形成一个属于用户自己的“神经元宇宙”。

## Why

未来的 AI 会越来越强，但模型能力会逐渐同质化。

真正稀缺的不是某一次回答的聪明，而是长期连续性：

- 它是否理解我如何提问？
- 它是否知道我如何拆解问题？
- 它是否记得我过去的选择？
- 它是否能延续我的表达、习惯、价值判断和工作方式？
- 它是否能在不同 AI 工具之间保存同一个“我”？

今天的 AI 工具大多仍然像一次性的高智商协作者。每一次新会话都需要重新解释背景、偏好、项目、审美和边界。Digital Persona Plugin 想补上的正是这一层：一个由用户自己拥有的、跨工具的个人认知连续性层。

## Vision

Digital Persona Plugin 的长期目标，是成为用户与所有 AI 工具之间的精神接口。

它不只是记录“我知道什么”，也记录：

- 我如何理解世界。
- 我如何判断问题。
- 我如何分配任务。
- 我如何使用 AI。
- 我如何在反复对话中形成稳定的偏好。
- 我如何从过去的自己走向新的自己。

这不是传统意义上的第二大脑。第二大脑更关注知识管理，而 Digital Persona 关注的是人格、知识、习惯与决策方式的共同生长。

我们可以把它理解为：

```text
Second Brain 记录知识。
Digital Persona 记录知识如何穿过一个人。
```

## Product Shape

系统由四层组成。

```text
AI Tools
Codex / Claude Code / OpenCode / ChatGPT / Future Agents
        ↓
Adapters
Tool-specific plugins, hooks, skills, MCP servers, command wrappers
        ↓
Persona Memory Core
Markdown protocol, extraction pipeline, memory index, persona synthesis
        ↓
Desktop Spirit App
Memory management, neuron graph, persona editor, visual spirit interface
```

### 1. AI Tool Adapters

不同 AI 工具的插件能力不同，因此项目采用 adapter 架构，而不是强行写一个单体插件。

- Codex adapter: 面向当前主要用户，也就是项目作者本人，优先支持 Codex。
- Claude Code adapter: 利用 hooks、plugins、skills 等机制捕获会话和工具事件。
- OpenCode adapter: 面向开源 coding agent 工作流，后续适配。
- Generic adapter: 通过命令行包装器、MCP server 或导入会话记录的方式接入其他工具。

### 2. Persona Memory Core

核心引擎负责把 AI 交互转为结构化记忆。

每次对话结束后，系统生成一份 Markdown：

```text
memories/
  2026/
    05/
      2026-05-28-codex-project-vision.md
```

每份记忆都包含：

- 本次任务
- 用户真实意图
- 对话中出现的知识
- 用户暴露出的偏好
- 用户的工作方式
- 可能影响长期人格的信号
- 下次遇到类似问题时应如何处理

### 3. Persona Synthesis

当记忆积累到一定数量后，系统会合成更稳定的人格文件：

```text
persona/
  profile.md
  values.md
  work-style.md
  communication-style.md
  tool-routing.md
  active-projects.md
  knowledge-map.md
```

这一步不是把人固定住，而是区分三种层次：

- 稳定人格：长期偏好、价值观、表达方式。
- 阶段人格：最近的项目、目标、压力和兴趣。
- 即时状态：当前任务、上下文和临时约束。

一个好的数字人格不应该困住用户过去的样子，而应该帮助用户看见自己正在变成什么。

### 4. Desktop Spirit App

桌面程序负责管理这些 Markdown，并把它们变成可操作的精神体。

未来它会提供：

- Markdown 记忆浏览与编辑
- 人格信号确认、合并、删除
- 知识节点与人格节点图谱
- 类 Obsidian 的神经元宇宙视图
- 精神体形象，不是真实头像，而是一种象征性的灵魂体界面
- 对 Codex、Claude Code、OpenCode 的上下文输出
- 对不同 AI 工具的任务路由建议

## What The Spirit Can Do

Digital Persona 的终局不是替代用户本人，而是替代用户重复性的认知流程。

它可以逐步承担：

- 记住项目背景
- 总结长期偏好
- 识别用户的提问习惯
- 按用户风格整理答案
- 判断一个问题适合交给哪个 AI 工具
- 把复杂问题切分给 Codex、Claude Code、OpenCode 或其他工具
- 在用户低效、犹豫或反复绕圈时提醒历史模式
- 在新会话开始时，把相关人格上下文注入 AI

它不能，也不应该替代：

- 用户的最终价值判断
- 用户对人生方向的选择
- 用户对关系、风险和意义的真实承担

它更像一个外置的认知骨架：保存连续性，减少重复解释，让 AI 更像长期协作者，而不是每次重新认识的陌生人。

## MVP

第一阶段只做一件事：

```text
在一次 AI 对话结束后，生成一份高质量人格记忆 Markdown。
```

最小闭环：

1. 用户在 Codex 中完成一次任务。
2. 插件或脚本读取本次交互的可用上下文。
3. 系统生成结构化 Markdown。
4. Markdown 写入本地 `memories/`。
5. 下一次 Codex 会话可以召回相关记忆。

MVP 不追求完整人格，也不急着做炫酷可视化。精神体的第一颗种子，是稳定、准确、可复用的记忆协议。

## Memory Protocol Draft

```md
# Memory: 2026-05-28 Codex Project Vision

## Source
- tool: codex
- project: digital-persona-plugin
- type: conversation

## User Intent
用户希望构建一个跨 AI 工具的插件系统，把 AI 交互沉淀为可管理、可召回、可演化的数字人格。

## Task Summary
本次对话讨论了项目愿景、产品形态、Codex-first MVP、桌面程序和精神体神经元宇宙。

## Knowledge Traces
- Codex、Claude Code、OpenCode 可以通过不同扩展机制接入。
- Markdown 适合作为第一阶段的人格记忆存储格式。
- 桌面程序负责后续管理、可视化和人格合成。

## Persona Signals
- 用户偏好哲学感与产品感结合。
- 用户希望系统最终具备长期人格连续性。
- 用户重视自己拥有 AI 记忆资产，而不是被单一平台锁定。

## Work Style
- 先明确项目主体，再进入代码实现。
- 喜欢把抽象灵感转成系统架构。
- 倾向把不同 AI 工具当作可调度能力，而不是单一聊天窗口。

## Future Recall
当用户讨论 AI 插件、数字人格、第二大脑、精神体、知识图谱或 Codex-first 实现时，应召回本条记忆。
```

## Codex-first Strategy

项目的第一个用户是作者本人，因此第一阶段优先支持 Codex。

当前调研结论：

- Codex 官方文档已经提供 Plugins、Build plugins、Hooks、MCP、Skills、AGENTS.md 等扩展入口。
- Codex plugins 可以打包 skills、app integrations、MCP servers，也可以打包 lifecycle hooks。
- Codex hooks 是官方扩展框架，支持在 agentic loop 中运行确定性脚本；官方示例场景中已经包含“总结对话以自动创建持久记忆”。
- Codex plugin-bundled hooks 可以通过插件根目录的 `hooks/hooks.json` 或 `.codex-plugin/plugin.json` 中的 `hooks` 字段加载。
- Codex MCP 支持 CLI 和 IDE extension，可以让 Codex 访问第三方工具和上下文，也适合作为本项目的人格记忆读写层。
- 对个人工作流而言，官方建议可以先从 local skill 开始；当需要跨项目共享、打包 MCP config、生命周期 hooks 或发布稳定包时，再做完整 plugin。

因此 Codex-first 不应押注单一能力，而应采用三条路并行：

1. **Plugin path**: 研究并实现 `.codex-plugin/plugin.json` 插件结构，用于分发技能、命令、MCP 和 hooks。
2. **MCP path**: 提供一个本地 Persona MCP server，让 Codex 可以读取记忆、写入记忆、召回人格上下文。
3. **Wrapper path**: 在 hooks 不稳定或事件不足时，用命令行包装器或手动命令先完成“会话总结 -> Markdown 写入”的闭环。

第一版 Codex adapter 的目标不是自动化所有事件，而是让作者本人每天使用 Codex 时，可以稳定产生人格记忆。

## Research Notes

本项目的接入路线参考了以下公开资料：

- Codex plugins overview: https://developers.openai.com/codex/plugins
- Codex build plugins: https://developers.openai.com/codex/plugins/build
- Codex hooks: https://developers.openai.com/codex/hooks
- Codex MCP: https://developers.openai.com/codex/mcp
- OpenAI plugins examples: https://github.com/openai/plugins
- OpenAI Codex CLI: https://github.com/openai/codex
- Codex configuration and lifecycle hooks: https://github.com/openai/codex/blob/main/docs/config.md
- Claude Code hooks: https://code.claude.com/docs/en/hooks
- Claude Code hooks guide: https://code.claude.com/docs/en/hooks-guide

Codex 当前已经足够支持本项目的第一阶段：用 hooks 或手动命令生成 Markdown 记忆，用 MCP 读写人格上下文，用 plugin 进行打包和分发。Claude Code 的 hooks 事件体系也很成熟，适合成为第二个 adapter。OpenCode 后续作为开源生态适配目标。

## Roadmap

### Phase 0: Project Foundation

- 写清项目愿景与 README。
- 定义 Markdown memory protocol。
- 确定本地目录结构。
- 调研 Codex 插件、hooks、MCP 可行性。

### Phase 1: Codex Memory MVP

- 实现本地 memory writer。
- 提供手动命令：把一段对话总结成 Markdown。
- 探索 Codex plugin / hooks / MCP 三种接入方式。
- 让作者本人在 Codex 日常使用中产生第一批记忆。

### Phase 2: Persona Core

- 从多份 memory 中合成 `persona/*.md`。
- 提取用户偏好、工作风格、工具路由规则。
- 支持按项目、主题、时间召回记忆。

### Phase 3: Desktop Spirit App

- 管理 Markdown 记忆。
- 可视化人格节点和知识节点。
- 支持用户确认、修正、删除错误人格信号。
- 形成神经元宇宙视图。

### Phase 4: Cross-AI Adapters

- Claude Code adapter。
- OpenCode adapter。
- 通用 MCP 接入。
- 多 AI 工具任务路由。

## Principles

- 用户拥有自己的记忆数据。
- Markdown 优先，透明、可读、可迁移。
- 人格不是一次生成，而是长期形成。
- AI 可以辅助判断，但不能偷走用户的最终意志。
- 系统应保存连续性，同时允许用户变化。
- 先做可自用的小闭环，再扩展成平台。

## Status

This project is in the concept and foundation stage.

The first milestone is a Codex-first memory plugin that turns AI conversations into structured Markdown traces.
