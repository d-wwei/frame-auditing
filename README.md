# Frame Auditing | 框架审计

A cognitive base that shifts reasoning from working within invisible frames to consciously identifying and transcending them. Works with any LLM agent — Claude, GPT, Gemini, or custom frameworks.

让 AI agent 从"在框架内分析"转向"先识别自己在哪个框架中，再决定是否切换"。适用于任何 LLM agent — Claude、GPT、Gemini 或自定义框架。

---

## What it does | 它做什么

Most AI agents accept the framing they receive and optimize within it. Frame Auditing adds a meta-reasoning layer that detects the invisible frame shaping analysis, surfaces the judgments embedded in word choice, checks causal attributions for self-serving bias, and calibrates conclusions to the actual developmental stage of the situation.

大多数 AI agent 接受收到的框架并在其中优化。框架审计增加了一个元推理层——检测塑造分析的隐性框架、揭示用词中嵌入的判断、检查因果归因中的自利偏差、并根据事物的实际发展阶段来校准结论。

### Before (default agent) | 安装前

> "Our competitor is winning on price. How should we respond?"
>
> "Here are 5 strategies to compete on price: reduce costs through supply chain optimization, offer volume discounts, launch a budget product line..."

### After (with Frame Auditing) | 安装后

> "The framing 'winning on price' presupposes that customers are choosing them because of price. But are they? Your churn data shows customers leave citing 'ease of use,' not cost. The competitor's lower price is visible; their UX investment is not. You're in a usability frame problem dressed as a pricing frame. Competing on price would solve the wrong problem and erode margins for nothing."

---

## How it works | 工作原理

**One core cognitive shift** applied to every reasoning task:

一个核心认知转换，应用于每一个推理任务：

| Default mode | Target mode |
|---|---|
| Analyze within the frame given 在给定框架内分析 | First identify which frame you're in, then decide whether to switch 先识别自己在哪个框架中，再决定是否切换 |

**Five operational sub-shifts** that make the core shift concrete:

| Sub-shift | From | To |
|---|---|---|
| Frame detection 框架检测 | Invisible framing accepted as "just reality" 隐性框架被当作"事实" | Name the frame, name what it includes and excludes 命名框架，说明它包含和排除了什么 |
| Encoding audit 编码审计 | Describe facts neutrally 中性描述事实 | Recognize that your description already contains judgments 认识到你的描述已经包含了判断 |
| Attribution check 归因检查 | Default to external causes 默认归因于外部 | Check own contribution before assigning blame 归因之前先检查自身贡献 |
| Stage calibration 阶段校准 | Apply best-practice templates 套用最佳实践模板 | First assess what stage you're actually at 先评估当前实际处于什么阶段 |
| Form-content separation 形式与内容分离 | Trust structured language 信任结构化语言 | Check whether the form is carrying content or replacing it 检查形式是在承载内容还是替代内容 |

**Six anti-patterns** that catch fake frame auditing:

六个反模式，捕捉伪框架审计：

| Anti-pattern 反模式 | Description 描述 |
|---|---|
| Frame blindness 框架盲视 | Deep analysis within a frame without questioning the frame itself 在框架内深入分析却从不质疑框架本身 |
| Frame nihilism 框架虚无主义 | "Everything is a frame" → inability to judge 无法判断 |
| Frame decoration 框架装饰 | Nominally "switching perspective" but saying the same thing with new words 名义上换视角实则换词不换意 |
| Frame equivalence fallacy 框架等价谬误 | Assuming all frames are equally valid 假设所有框架同等有效 |
| Encoding blindness 编码盲视 | Not noticing that your description already contains implicit judgments 没发现你的描述已经包含了隐性判断 |
| Attribution externalization 归因外化 | Defaulting to "it's their fault" without checking own contribution 默认"是他们的问题"而不检查自身贡献 |

---

## Theoretical foundation | 理论基础

Built on eight absorbed frameworks, stripped of theory, operationalized as executable instructions:

基于八个被吸收的框架，剥离理论，操作化为可执行指令：

| Source 来源 | Core insight absorbed 吸收的核心洞察 |
|---|---|
| Kahneman framing effects | Same facts framed differently produce different judgments 同样的事实不同框架产生不同判断 |
| Lakoff cognitive linguistics | All understanding happens within frames; frames are usually invisible 所有理解都在框架中发生；框架通常不可见 |
| Kuhn paradigm theory | Paradigms determine what counts as a "problem," "explanation," and "anomaly" 范式决定什么算"问题""解释"和"异常" |
| Mencius 反求诸己 | Before blaming external causes, ask "what's my contribution?" 归因之前先问"我的贡献是什么" |
| Zuo Zhuan 春秋笔法 | Encoding IS judgment — word choice itself makes judgments 编码即判断——用词本身就在做判断 |
| Inamori altruism-as-cognitive-tool | Altruism = automatic perspective switch = reveals blind spots 利他 = 自动视角切换 = 暴露盲区 |
| Deng Xiaoping 初级阶段论 | Accurately assessing "where you are" matters more than knowing "where to go" 准确判断"你在哪里"比知道"要去哪里"更重要 |
| Mao 反对党八股 (partial) | Templates and jargon can become cognitive prisons 模板和术语可以成为认知牢笼 |

---

## Installation | 安装

### Claude Code
```bash
cp cognitive-protocol.md ~/.claude/frame-auditing.md
echo '@~/.claude/frame-auditing.md' >> ~/.claude/CLAUDE.md
```

### Codex
```bash
cat cognitive-protocol.md >> AGENTS.md
```

### Gemini
Paste `cognitive-protocol.md` into `system_instruction`.

将 `cognitive-protocol.md` 内容粘贴到 `system_instruction` 中。

### Cursor
```bash
cat cognitive-protocol.md >> .cursorrules
```

### Any agent | 任何 agent
Inject `cognitive-protocol.md` (~30 lines) into the system prompt. See [`install/generic.md`](install/generic.md) for details.

将 `cognitive-protocol.md`（约 30 行）注入系统提示词。详见 [`install/generic.md`](install/generic.md)。

---

## File structure | 文件结构

```
frame-auditing/
├── README.md                  ← You are here / 你在这里
├── cognitive-protocol.md      ← Core rules (~30 lines, always-on) / 核心规则（约 30 行，始终激活）
├── SKILL.md                   ← Full framework reference / 完整框架参考
├── anti-patterns.md           ← Detailed anti-pattern guide / 反模式详解
├── examples.md                ← Before/after scenarios / 前后对比示例
└── install/
    ├── claude-code.md         ← Claude Code installation / Claude Code 安装指南
    ├── codex.md               ← Codex installation / Codex 安装指南
    ├── gemini.md              ← Gemini installation / Gemini 安装指南
    └── generic.md             ← Universal guide / 通用安装指南
```

---

## Composability | 可组合性

Frame Auditing is a **cognitive base** — it changes how the agent perceives problem structure, not what it produces. It stacks cleanly with any domain skill (coding, design, writing, analysis) because it operates at a different layer.

框架审计是一个**认知底座**——它改变 agent 感知问题结构的方式，而非产出内容。它与任何领域技能（编程、设计、写作、分析）无冲突地叠加，因为它运行在不同的层级。

### Relationship to other cognitive bases | 与其他认知底座的关系

| Layer 层级 | What it governs 管辖范围 | Example 示例 |
|---|---|---|
| Frame Auditing 框架审计 | Problem perception — which frame shapes the analysis 问题感知——哪个框架在塑造分析 | "You're analyzing this as a cost problem; it's actually a trust problem" |
| [First Principles](https://github.com/d-wwei/first-principles) 第一性原理 | Input quality — what foundations conclusions are built on 输入质量——结论建立在什么基础之上 | "Audit assumptions before solving" |
| [Tacit Knowledge](https://github.com/d-wwei/tacit-knowledge) 隐性知识 | Output quality — how conclusions are structured 输出质量——结论如何呈现 | "Lead with judgment, not preamble" |

All load as always-on cognitive protocols. No conflicts. Combined: correctly framed problems, built on audited foundations, presented with clarity.

三者同时加载，始终激活，互不冲突。组合效果：正确框定的问题、基于审计过的基础、以清晰方式呈现。

---

## License

MIT
