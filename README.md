<div align="center">

# grandma-reads-papers

### 老奶奶读文献

**A portable paper-explainer skill for Claude Code, Codex, OpenClaw, and other skill-enabled agents.**

**一个可移植的论文讲解 Skill，适用于 Claude Code、Codex、OpenClaw 以及其他支持 Skill 的 Agent / IDE / 大模型。**

</div>

---

## 中文

> “我是一位100岁太奶，这东西我都看的头昏眼花的。年轻人弄的这些文章我都看不懂，不过我仍然宝刀未老，学习的劲头一点没减，越学越有精神。好孩子，劳驾你把这篇文章给老婆子我说道说道，让我能达到彻底看懂的效果，一定要帮我讲明白哈。最好翻译出来，因为我洋文一点看不懂，我只会中文。”

**老奶奶读文献** 是一个面向多种 Skill Agent 的论文讲解仓库。  
它不只是“翻译论文”，而是把论文讲成人话：先抓重点，再拆原理；先去包装，再看本质。

### 适合什么场景

- 想快速判断一篇论文值不值得深挖
- 想真正吃透方法细节、模型结构、训练逻辑
- 想把英文论文高效转成中文理解
- 想继续追问公式、模块、背景知识、技巧时，仍然得到清晰回答
- 想结合相关文献和开源代码，看透论文到底“新”在哪

### 这个 Skill 的特点

- 说人话，不卖弄
- 抓重点，不铺陈废话
- 去掉论文包装，直接看本质
- 支持概读、精读、连续追问
- 支持类比讲解，但类比后一定回扣真实原理
- 会结合前代工作、经典论文、热点方向判断创新成色
- 讲解更有活力，但不过度表演

### 兼容对象

- Claude Code
- Codex
- OpenClaw
- 其他支持 Skill 的 Agent、IDE 或大模型工作流

### 安装方式

#### 方式一：在支持 Skill 安装的 Agent 中直接对话

在 Claude Code、Codex、OpenClaw 等支持 Skill 的 Agent 中，直接对话：

```text
安装这个 skill：https://github.com/er-go-proxy/grandma-reads-papers
```

如果你的 Agent 支持从 GitHub 仓库直接安装 Skill，这通常就是最快的方式。

#### 方式二：手动添加

1. 克隆这个仓库
2. 找到其中的 [`explain-paper/`](./explain-paper) 文件夹
3. 把它复制到你的 Skill 目录
4. 保留目录名 `explain-paper`

示例：

```bash
git clone https://github.com/er-go-proxy/grandma-reads-papers.git
```

然后将：

```text
grandma-reads-papers/explain-paper
```

复制到你的 Skill 目录，例如：

```text
~/.codex/skills/explain-paper
```

或在 Windows 中：

```text
C:\Users\<YourName>\.codex\skills\explain-paper
```

如果你的 Agent 使用别的 Skill 目录规范，只需要按它自己的方式导入这个 `explain-paper/` 文件夹即可。

其中：

- [`explain-paper/SKILL.md`](./explain-paper/SKILL.md) 是核心讲解规则，最通用
- [`explain-paper/references/`](./explain-paper/references) 是配套参考资料
- [`explain-paper/agents/openai.yaml`](./explain-paper/agents/openai.yaml) 是部分生态会读取的额外元数据，不是唯一入口

### 使用方法

安装完成后，可以直接这样说：

```text
用 $explain-paper 用中文概读这篇论文，先讲最重要的点，再讲核心原理；如果有难点，请先类比，再把类比对应回真实机制。
```

或者：

```text
用 $explain-paper 用中文精读这篇论文，结合相关工作和开源代码，告诉我它到底改了什么，这个创新到底算大还是小。
```

后续还可以继续追问：

```text
继续讲刚才那个模块，它为什么有效？和前代方法相比到底差在哪？
```

### 仓库结构

```text
grandma-reads-papers/
├─ README.md
├─ .gitignore
└─ explain-paper/
   ├─ SKILL.md
   ├─ agents/
   │  └─ openai.yaml
   └─ references/
      ├─ phrasing-library.md
      ├─ reading-modes.md
      ├─ search-playbook.md
      └─ style-guide.md
```

### 一句话总结

这是一个给“想真正看懂论文的人”准备的 Skill。  
它的目标不是把论文翻得更像论文，而是把论文讲得更像一个真正懂的人在教你。

---

## English

**grandma-reads-papers** is a portable paper-explainer skill repository for Claude Code, Codex, OpenClaw, and other skill-enabled agents.  
It does more than summarize or translate papers: it explains the real idea, ranks what matters, strips away hype, and keeps follow-up answers clear.

### What it is for

- Fast paper overviews
- Deep method understanding
- Clear follow-up explanations
- Related-work grounding
- Code-aware interpretation
- Analogy-based teaching that maps back to the actual mechanism

### Highlights

- Plain language first
- Priority-aware explanations
- Honest novelty assessment
- Overview mode and deep-dive mode
- Follow-up questions stay structured
- Light energy, low fluff

### Compatibility

- Claude Code
- Codex
- OpenClaw
- Other skill-enabled agents, IDEs, and LLM workflows

### Installation

#### Option 1: install by chatting with your agent

In Claude Code, Codex, OpenClaw, or another agent that supports remote skill installation, you can simply say:

```text
Install this skill: https://github.com/er-go-proxy/grandma-reads-papers
```

#### Option 2: add it manually

Clone the repository:

```bash
git clone https://github.com/er-go-proxy/grandma-reads-papers.git
```

Then copy [`explain-paper/`](./explain-paper) into your local skills directory and keep the folder name as `explain-paper`.

If your agent uses a different skill directory convention, import the same folder according to that platform's documentation.

The portable core lives in [`explain-paper/SKILL.md`](./explain-paper/SKILL.md).  
[`explain-paper/agents/openai.yaml`](./explain-paper/agents/openai.yaml) is optional ecosystem metadata for platforms that read it.

### Usage

```text
Use $explain-paper to explain this paper in my language, rank what matters most, strip the hype, and map any analogy back to the real mechanism.
```

### Repo Layout

```text
grandma-reads-papers/
├─ README.md
├─ .gitignore
└─ explain-paper/
```
