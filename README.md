# Digital Persona Plugin

> 不是让 AI 假装成为一个人，而是让一个人的思考痕迹拥有可延续的结构。

Digital Persona Plugin 是一个面向 AI 工具的数字人格基础设施。它连接 Codex、Claude Code、OpenCode 等 agentic AI 工作流，将用户与 AI 的每一次协作沉淀为可审视、可追溯、可召回、可演化的人格记忆。

这些记忆不是普通日志。它们记录的不只是“发生了什么”，还包括用户如何提问、如何判断、如何拆解任务、如何形成偏好，以及如何在长期协作中逐渐塑造自己的工作方式。

项目最终希望形成一个属于用户自己的精神体：一个由人格、知识、习惯、决策痕迹和工具使用方式组成的神经元宇宙。

## Vision

AI 会越来越强，但真正稀缺的不是单次回答的聪明，而是长期连续性。

今天的 AI 工具大多仍然像临时协作者。每一次新会话，都需要重新解释背景、偏好、项目、审美和边界。Digital Persona Plugin 希望补上这一层缺失的连续性，让用户在不同 AI 工具之间拥有同一个可迁移的个人上下文。

它不是传统意义上的第二大脑。第二大脑更关注知识管理，而 Digital Persona 关注的是人格、知识、习惯与决策方式的共同生长。

```text
Second Brain 记录知识。
Digital Persona 记录知识如何穿过一个人。
```

## What It Builds

Digital Persona Plugin 构建的是一个跨 AI 工具的个人认知层。

它会持续沉淀：

- 用户的长期目标与项目背景
- 用户的表达风格与沟通偏好
- 用户的任务拆解方式
- 用户在不同场景下的决策习惯
- 用户与 Codex、Claude Code、OpenCode 等工具的协作模式
- 对话中产生的知识、概念、判断和灵感
- 可被后续 AI 会话召回的人格上下文

随着记忆不断积累，系统会逐渐生成可审视、可追溯的数字人格。这个人格不是一个固定人设，而是一个持续演化的精神结构。

## Core Features

### Cross-AI Memory Layer

通过插件、hooks、MCP、skills 或本地自动化接入多个 AI 工具，让用户的记忆不被单一平台锁定。

### Structured Persona Memory

将 AI 交互转化为结构化 Markdown，保留用户意图、知识痕迹、偏好信号、工作方式和未来可召回上下文。

### Persona Synthesis

从分散的记忆中提炼长期人格：价值偏好、沟通风格、工作习惯、工具路由规则和阶段性目标。

### Context Recall

在新的 AI 会话开始时，自动召回相关人格记忆，让 AI 更快理解用户，而不是每次重新开始。

### Cognitive Mirror

通过长期语言、选择和行为记录，观察用户反复出现的模式，帮助用户理解自己不只是“在想什么”，而是“为什么总是这样想、这样选择”。

### Decision Companion

在重大选择面前，结合长期人格记忆、价值倾向、历史决策和行为模式，提供更深层的选择分析。它不替用户做决定，而是帮助用户更完整地看见自己的动机、矛盾和长期方向。

### Neuron Universe

通过桌面程序管理和可视化人格记忆，把知识节点、习惯节点、项目节点、工具节点和决策节点连接成一个精神体宇宙。

### Spirit Interface

未来的精神体形象不是拟真人物，而是一种象征性的灵魂体界面，用来表达用户的长期记忆、认知结构和内在变化。

## Product Architecture

```text
AI Tools
Codex / Claude Code / OpenCode / ChatGPT / Future Agents
        ↓
Adapters
Plugins / Hooks / MCP / Skills / Local Automation
        ↓
Persona Memory Core
Markdown Protocol / Extraction / Indexing / Synthesis
        ↓
Desktop Spirit App
Memory Management / Neuron Graph / Persona Editor / Spirit Interface
```

## Why Now

AI 工具正在从单一聊天窗口走向多 agent、多工具、多上下文协作。用户会越来越频繁地在不同 AI 系统之间切换，但个人记忆、偏好和工作方式仍然碎片化地散落在各个平台里。

Digital Persona Plugin 关注的正是这个缺口：

- AI 能力会增强，但用户的长期上下文仍然缺失。
- AI 工具会增多，但跨工具的人格连续性仍然缺失。
- 知识库工具很多，但真正面向“人格与工作方式”的系统仍然很少。
- 用户需要拥有自己的 AI 记忆资产，而不是让它被封存在某一个平台。

## Role Of The Digital Persona

Digital Persona 的目标不是替代用户本人，而是替代重复性的认知流程。

它可以帮助用户：

- 记住长期项目背景
- 减少重复解释
- 让 AI 延续用户偏好的表达和判断方式
- 辅助复杂任务拆解
- 判断不同问题适合交给哪个 AI 工具
- 在反复出现的工作模式中发现规律
- 根据长期记忆形成认知镜像，帮助用户理解自己的重复动机和选择模式
- 在重大选择中提供基于人格记忆的分析与陪伴
- 让 AI 从一次性工具变成长期协作者

它不能，也不应该替代用户的最终意志。真正的价值判断、人生方向和意义选择，仍然属于用户本人。

## Epistemic Integrity

Digital Persona 不是一张可以随意编辑的人格标签表。它应当像一个独立生长的精神体：所有判断、假设和人格画像都必须来源于长期记忆，而不是人为改写出来的结论。

系统可以提出镜像和假设，但不能宣判用户是谁。它可以分析用户为什么反复做出某些选择，但必须保留证据链，让每一个判断都能回到具体记忆、语言和行为痕迹。

这种不可随意篡改性，是数字人格独立性的基础。用户拥有记忆数据，但人格判断应由记忆自然推导，而不是被用户手工修饰成更舒服的样子。

## Technical Direction

Digital Persona Plugin 采用 adapter-first 架构。不同 AI 工具的扩展能力不同，因此系统不会依赖某一个封闭平台，而是通过适配器接入不同环境。

Codex 是重要的初始接入场景。它已经具备插件、hooks、MCP、skills 和本地项目上下文等扩展能力，适合作为开发者工作流中的第一类落地环境。

Claude Code、OpenCode 和其他 agentic AI 工具可以通过相同的记忆协议逐步接入。长期来看，Digital Persona Plugin 希望成为一个跨 AI 工具的用户自有记忆层。

## Principles

- 用户拥有自己的记忆数据。
- 人格判断必须来源于记忆，不允许被随意手工改写。
- Markdown 优先，透明、可读、可迁移。
- 人格不是一次生成，而是长期形成。
- 系统应保存连续性，同时允许用户变化。
- AI 可以辅助判断，但不能偷走用户的最终意志。
