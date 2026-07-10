# 哲学思想 Skill 库

Philosophical Reasoning Skills for AI Agents

给 AI Agent 安装人类思想家的决策模型。

> Installing philosophical reasoning patterns into AI agents.

## 这不是哲学百科

这个项目不追求收集更多哲学知识，而是把哲学家的思想蒸馏成 AI Agent 可以调用的认知模型。

AI 不缺信息，缺少的是：

- 判断框架
- 第一性原理
- 长期视角
- 价值判断
- 复杂系统理解

本项目的核心假设是：

知识不等于智慧。  
真正有用的哲学 Skill，应该帮助 AI 在现实问题中分析、判断和行动。

## 项目定位

本项目提供一组 Markdown-first 的 Reasoning Skills，用于让 AI Agent 在面对商业、人生、技术和战略问题时，调用哲学家的思维框架。

第一版本只使用 Markdown：

- `skills/`：面向任务的 Agent Skill
- `thinkers/`：哲学家认知模型
- `frameworks/`：可复用推理模型
- `examples/`：使用样例
- `tests/`：回答质量验收清单

未来可扩展：

- MCP Server
- RAG
- Embedding Search
- 自动评测系统

## 目录结构

```text
philosophy-skills/
├── README.md
├── philosopher-router.md
├── skills/
│   ├── strategic-thinking/
│   │   └── SKILL.md
│   ├── ai-market-strategy/
│   │   └── SKILL.md
│   ├── decision-making/
│   │   └── SKILL.md
│   ├── self-growth/
│   │   └── SKILL.md
│   └── technology-philosophy/
│       └── SKILL.md
├── thinkers/
│   ├── laozi.md
│   ├── zhuangzi.md
│   ├── wang_yangming.md
│   ├── hegel.md
│   ├── nietzsche.md
│   ├── kant.md
│   └── heidegger.md
├── frameworks/
│   ├── shunshi-model.md
│   ├── zhixingheyi-model.md
│   ├── dialectic-model.md
│   ├── self-overcoming-model.md
│   ├── ai-market-validation-model.md
│   └── first-principle-model.md
├── examples/
│   ├── startup.md
│   ├── career-choice.md
│   ├── ai-future.md
│   └── gpt-usage-examples.md
└── tests/
    └── evaluation.md
```

## 安装方式

### Claude Code Skill

将 `skills/` 下的目录复制到 Claude Code 可识别的 Skill 目录中。每个 Skill 都包含标准 `SKILL.md`：

```text
---
name:
description:
---
```

### ChatGPT Custom GPT

将以下文件作为 Knowledge 上传：

- `philosopher-router.md`
- `skills/**/*.md`
- `thinkers/*.md`
- `frameworks/*.md`

系统提示中加入：

```text
当用户提出现实问题时，不要回答哲学知识。
请先使用 philosopher-router.md 选择适合的哲学家和思维模型，
再按对应 Skill 的 Output Format 输出分析和行动建议。
```

### 未来 MCP

未来版本可以将 Router、Thinkers 和 Frameworks 封装成 MCP Server，让 Agent 通过工具调用选择模型、读取框架并执行评测。

## 设计原则

- 面向现实问题，而不是哲学史复述
- 输出行动建议，而不是概念堆砌
- 每个哲学家必须转化为可执行 Reasoning Pattern
- 每个 Framework 必须有输入、步骤和输出
- 每个 Skill 必须能独立被 Agent 调用

## 当前首版包含

核心哲学家：

- 老子
- 庄子
- 王阳明
- 黑格尔
- 尼采

伦理与技术哲学模型：

- 康德
- 海德格尔

核心思维模型：

- 顺势模型
- 知行合一模型
- 辩证发展模型
- 超越自我模型
- 第一性原理模型
- AI 市场验证模型

市场化 Skill：

- AI 市场战略：用于判断 AI 产品、Agent 应用、垂直 SaaS、自动化工作流是否具备真实市场机会

## 快速示例

用户问题：

```text
我要不要进入 AI 创业？
```

Agent 应判断：

- 这是 AI 市场战略 + 创业决策问题
- 调用老子的顺势模型判断趋势
- 调用王阳明的知行合一模型判断行动能力
- 调用黑格尔的辩证发展模型判断时代结构变化
- 调用 AI 市场验证模型判断客户、场景、付费和分发

输出结构：

1. 问题本质
2. 哲学视角
3. 思维模型
4. 现实应用
5. 行动建议

## GPT 使用验证

将本仓库作为 GPT Knowledge 后，可以使用 [examples/gpt-usage-examples.md](examples/gpt-usage-examples.md) 中的示例问题验证回答质量。

一个合格回答应做到：

- 先路由问题，而不是直接泛泛回答
- 调用哲学家作为推理模型，而不是介绍哲学知识
- 对 AI 市场问题输出客户、痛点、付费、分发和验证动作
- 给出明确的下一步实验

## License

MIT
