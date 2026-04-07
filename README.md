<div align="center">

# grandma-reads-papers

### 老奶奶读文献

![Platforms](https://img.shields.io/badge/Platforms-Claude%20Code%20%7C%20Codex%20%7C%20OpenClaw-2563eb)
![Modes](https://img.shields.io/badge/Modes-Overview%20%7C%20Deep--Dive-16a34a)
![Languages](https://img.shields.io/badge/Languages-ZH%20%7C%20EN%20%7C%20More-f59e0b)
![Type](https://img.shields.io/badge/Type-Skill-7c3aed)

<p>
  <strong>一个论文辅助阅读 Skill，适用于 Claude Code、Codex、OpenClaw 以及其他支持 Skill 的 Agent / IDE / 大模型。</strong><br/>
  <strong>用通俗易懂的语言帮助你快速 / 深度理解论文观点和方法原理。</strong>
</p>

<p>
  <strong>A paper-reading skill for Claude Code, Codex, OpenClaw, and other skill-enabled agents.</strong><br/>
  <strong>Helps you understand paper ideas and method principles in plain language, fast or deep.</strong>
</p>

</div>

---

## 中文

> “我是一位100岁太奶，这东西我都看的头昏眼花的。年轻人弄的这些文章我都看不懂，不过我仍然宝刀未老，学习的劲头一点没减，越学越有精神。好孩子，劳驾你把这篇文章给老婆子我说道说道，让我能达到彻底看懂的效果，一定要帮我讲明白哈。最好翻译出来，因为我洋文一点看不懂，我只会中文。”

**老奶奶读文献** 是一个给“看不懂但想看懂论文的人”准备的 Skill。  
它不只做翻译或摘要，而是把论文里的包装拆掉，解释难以理解的词汇，并把真正重要的观点、方法、创新点和局限讲清楚。并在结尾给予提问建议。

### Features

- `概读`：快速抓住论文在解决什么问题、核心思路是什么、创新到底大不大。
- `精读`：拆开模型结构、训练逻辑、损失函数、推理流程，讲清方法原理。
- `连续追问`：后续继续问公式、模块、背景知识、技巧时，仍然保持清晰、抓重点、说人话。
- `多语言辅助阅读与翻译`：支持中、英文等多种语言的论文辅助阅读与解释。
- `关联文献`：把论文放回研究脉络里，看它和前代工作、经典论文、热点方向的关系。
- `代码解读`：有开源代码时，优先结合代码看论文，避免被花哨命名带偏。
- `类比讲解`：遇到难点时先用类比帮助上手，但类比后一定回扣真实机制和边界。

### Why This Skill

- 说人话，不卖弄
- 抓重点，不铺陈废话
- 去掉论文包装，直接看本质
- 会判断“这到底是真创新，还是小改动换了个名字”
- 讲解更有活力，但不过度表演

### Compatibility

- Claude Code
- Codex
- OpenClaw
- 其他支持 Skill 的 Agent、IDE 或大模型工作流

### Install

#### 方式一：直接对话安装

在 Claude Code、Codex、OpenClaw 等支持 Skill 的 Agent 中，直接说：

```text
安装这个 skill：https://github.com/er-go-proxy/grandma-reads-papers
```

#### 方式二：手动添加

```bash
git clone https://github.com/er-go-proxy/grandma-reads-papers.git
```

把 [`grandma-reads-papers/`](./grandma-reads-papers) 这个文件夹复制到你的 Skill 目录，并保留目录名 `grandma-reads-papers`。

示例：

```text
~/.codex/skills/grandma-reads-papers
```

Windows:

```text
C:\Users\<YourName>\.codex\skills\grandma-reads-papers
```

其中：

- [`grandma-reads-papers/SKILL.md`](./grandma-reads-papers/SKILL.md) 是最通用的核心入口
- [`grandma-reads-papers/references/`](./grandma-reads-papers/references) 是配套参考资料
- [`grandma-reads-papers/agents/openai.yaml`](./grandma-reads-papers/agents/openai.yaml) 是部分生态会读取的可选元数据

不同 Agent 的自动触发机制不完全一样，但通常主要看 `SKILL.md` 里的 `description`。  
所以这个 skill 既可以靠相关任务描述自动触发，也可以显式写 `$grandma-reads-papers` 来更稳定地调用。

### Usage

```text
用 $grandma-reads-papers 用中文概读这篇论文，先讲最重要的点，再讲核心原理；如果有难点，请先类比，再把类比对应回真实机制。
```

```text
用 $grandma-reads-papers 用中文精读这篇论文，结合相关工作和开源代码，告诉我它到底改了什么，这个创新到底算大还是小。
```

```text
继续讲刚才那个模块，它为什么有效？和前代方法相比到底差在哪？
```

### Repo Layout

```text
grandma-reads-papers/
├─ README.md
├─ .gitignore
└─ grandma-reads-papers/
   ├─ SKILL.md
   ├─ agents/
   │  └─ openai.yaml
   └─ references/
      ├─ phrasing-library.md
      ├─ reading-modes.md
      ├─ search-playbook.md
      └─ style-guide.md
```

---

## English

**grandma-reads-papers** is a paper-reading skill for Claude Code, Codex, OpenClaw, and other skill-enabled agents.  
It doesn't just translate or summarize; it strips away the academic packaging, explains jargon and obscure terminology, and clearly articulates what truly matters—the key arguments, methodologies, innovations, and limitations. It concludes with suggested questions for further inquiry.

### Features

- Fast paper overviews
- Deep method breakdowns
- Follow-up explanations that stay structured
- Multilingual paper reading and translation support, including Chinese and English
- Related-work grounding
- Code-aware interpretation
- Analogy-based teaching that maps back to the actual mechanism

### Install

#### Option 1: install by chatting with your agent

```text
Install this skill: https://github.com/er-go-proxy/grandma-reads-papers
```

#### Option 2: add it manually

```bash
git clone https://github.com/er-go-proxy/grandma-reads-papers.git
```

Then copy [`grandma-reads-papers/`](./grandma-reads-papers) into your local skills directory and keep the folder name as `grandma-reads-papers`.

The portable core lives in [`grandma-reads-papers/SKILL.md`](./grandma-reads-papers/SKILL.md).  
[`grandma-reads-papers/agents/openai.yaml`](./grandma-reads-papers/agents/openai.yaml) is optional ecosystem metadata for platforms that read it.

Explicit invocation with `$grandma-reads-papers` is the most reliable cross-agent option.

### Usage

```text
Use $grandma-reads-papers to explain this paper in my language, rank what matters most, strip the hype, and map any analogy back to the real mechanism.
```
