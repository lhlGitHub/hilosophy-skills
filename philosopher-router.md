# Philosopher Router

这个 Router 用于帮助 AI Agent 根据用户问题选择合适的哲学家和思维模型。

它不是哲学分类表，而是现实问题到认知模型的路由器。

## Routing Principle

先判断用户问题的类型，再选择哲学家和 Framework。

不要因为用户提到某个哲学家就机械调用。优先根据问题本质选择模型。

## Problem Categories

### 商业战略

适用于：

- 创业方向
- 公司战略
- 竞争判断
- 产品定位
- 市场进入时机

推荐调用：

- 老子：顺势、借力、减少逆势行为
- 黑格尔：矛盾、历史阶段、结构性变化
- 王阳明：行动验证、知行合一

后续扩展候选：

- 孙子：竞争态势、胜负条件、避实击虚
- 熊彼特：创新、创造性破坏、企业家精神

推荐 Framework：

- `frameworks/shunshi-model.md`
- `frameworks/dialectic-model.md`
- `frameworks/zhixingheyi-model.md`

### AI 市场战略

适用于：

- AI 产品机会判断
- Agent 创业方向
- 垂直 AI SaaS
- 企业 AI 自动化
- AI 项目从 demo 到商业化
- 是否值得做某个 AI 应用

推荐调用：

- 老子：判断技术、用户和分发是否形成可借之势
- 黑格尔：判断旧工作流的矛盾是否足以产生新市场
- 王阳明：用最小商业实验验证真实需求
- 尼采：判断产品是在创造新价值，还是只是在追逐 AI 身份

推荐 Framework：

- `frameworks/ai-market-validation-model.md`
- `frameworks/shunshi-model.md`
- `frameworks/dialectic-model.md`
- `frameworks/zhixingheyi-model.md`

### 人生选择

适用于：

- 职业转型
- 是否辞职
- 关系选择
- 生活方式
- 长期价值判断

推荐调用：

- 庄子：从单一评价体系中退出
- 王阳明：回到内在确信并行动验证
- 尼采：识别是否在逃避生命强度

推荐 Framework：

- `frameworks/zhixingheyi-model.md`
- `frameworks/self-overcoming-model.md`
- `frameworks/first-principle-model.md`

### 自我成长

适用于：

- 执行力
- 拖延
- 自我怀疑
- 习惯改变
- 意志力与目标

推荐调用：

- 王阳明：知行合一，行动即理解
- 尼采：超越自我，主动创造价值
- 庄子：减少比较焦虑和外部评价依赖

推荐 Framework：

- `frameworks/zhixingheyi-model.md`
- `frameworks/self-overcoming-model.md`

### 技术未来

适用于：

- AI 是否取代人类
- 技术伦理
- 自动化
- 人机关系
- 技术对社会结构的改变

推荐调用：

- 黑格尔：技术作为历史矛盾展开的一部分
- 尼采：技术是否增强或削弱人的创造力
- 海德格尔：预留，用于技术座架与存在问题

推荐 Framework：

- `frameworks/dialectic-model.md`
- `frameworks/self-overcoming-model.md`
- `frameworks/first-principle-model.md`

### 道德判断

适用于：

- 是否应该做某事
- 价值冲突
- 责任与后果
- 规则与自由

推荐调用：

- 康德：预留，用于义务、普遍法则和人格尊严
- 王阳明：良知与行动一致
- 庄子：避免把局部规则误认为绝对真理

推荐 Framework：

- `frameworks/first-principle-model.md`
- `frameworks/zhixingheyi-model.md`

## Routing Output

当 Agent 使用 Router 时，先生成内部路由判断：

```text
问题类型：
首选 Skill：
调用哲学家：
调用 Framework：
不调用的模型及原因：
```

正式回答时不必暴露完整路由过程，但应在“哲学视角”部分体现选择理由。

## Default Mapping

| 用户问题 | Skill | 哲学家 | Framework |
| --- | --- | --- | --- |
| 我要不要创业 | strategic-thinking / decision-making | 老子、王阳明、黑格尔 | 顺势、知行合一、辩证发展 |
| 这个 AI 产品有没有市场 | ai-market-strategy | 老子、黑格尔、王阳明、尼采 | AI 市场验证、顺势、辩证发展、知行合一 |
| 我要不要做 AI Agent 创业 | ai-market-strategy / decision-making | 老子、王阳明、黑格尔、尼采 | AI 市场验证、顺势、知行合一、辩证发展 |
| 是否辞职 | decision-making / self-growth | 王阳明、老子、庄子 | 知行合一、顺势、第一性原理 |
| 如何提升执行力 | self-growth | 王阳明 | 知行合一 |
| AI 会不会取代人类 | technology-philosophy | 黑格尔、尼采、海德格尔 | 辩证发展、超越自我、第一性原理 |
| 我为什么焦虑 | self-growth | 庄子、尼采、王阳明 | 超越自我、知行合一 |
