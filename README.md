# Chinese Normative Academic Writing

一套面向中文哲学、伦理学、科技伦理学及相邻规范研究的 Codex Skill。

它不只是润色文字，而是帮助作者完成一条完整的学术写作链：

~~~text
确认问题确实需要回答
→ 锁定一个中心回答
→ 按读者理解顺序展开
→ 用具体对象和必要概念完成推理
→ 控制证据强度
→ 发布最强贡献
~~~

## 为什么创建这个 Skill

学术写作中的很多问题并不是句子不够漂亮，而是：

- 从抽象术语出发制造了一个伪问题；
- 一篇论文同时追逐多个中心问题；
- 段落之间只有连接词，没有真正的理由关系；
- 概念越来越多，读者却看不见谁在做什么；
- 文献、案例和数据进入正文，却没有明确论证职责；
- 为了显得谨慎，作者主动替审稿人扩大攻击面；
- 每一轮修改都增加新框架，论文永远无法达到充分状态。

本 Skill 把这些经验转化为可复用的写作方法，而不是一份抽象的风格偏好清单。

## 标志性原则

- **先确认问题确实需要回答。**
- **一篇论文只保留一个中心问题和一个对应回答。**
- **下一步必须由上一步产生。**
- **问题应从材料中出现，而不是从术语中出现。**
- **让概念帮助理解，而不是代替理解。**
- **每一节、每一段和每份材料都要推动同一条论证链。**
- **小问题不升级，真问题不隐藏。**
- **保留边界，但不要穿盔甲。**
- **先诊断，后改写；不要用重写代替判断。**
- **论文追求清楚、成立和充分，不追求无穷完备。**

## 它适合什么任务

- 中文哲学、伦理学与科技伦理学论文构思；
- 研究问题、中心论点和提纲澄清；
- 中文论文段落、章节、摘要、引言和结论起草；
- 论证链、规范前提和章节职责检查；
- 抽象语言、术语堆砌、机械重复和翻译腔修改；
- 文献、案例、数据与说明性例子的职责判断；
- 防御性写作和自我削弱表达修正；
- 论文压缩、局部修订与定稿。

它不负责项目管理、版本权限、多模型分工，也不会在普通写作任务中自动启动无边界的全文审核。

## 目录结构

~~~text
Chinese-Normative-Academic-Writing/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── real-question-and-argument.md
    ├── concrete-language-and-story.md
    ├── evidence-and-academic-release.md
    └── revision-and-sufficiency.md
~~~

各文件职责：

| 文件 | 内容 |
| --- | --- |
| [SKILL.md](SKILL.md) | 核心写作链、默认工作方式、参考文件路由与条件协同 |
| [real-question-and-argument.md](references/real-question-and-argument.md) | 研究问题、单一问题、问题—答案对应、规范推理与原创贡献 |
| [concrete-language-and-story.md](references/concrete-language-and-story.md) | 读者故事、段落推进、具体语言、抽象阶梯、术语、例子与重复 |
| [evidence-and-academic-release.md](references/evidence-and-academic-release.md) | 证据强度、材料职责、文献综述、学术发布、边界与非防御表达 |
| [revision-and-sufficiency.md](references/revision-and-sufficiency.md) | 先诊断后修改、最小完整修订、奥卡姆剃刀与学术充分性 |

## 安装

### 让 Codex 安装

可以直接告诉 Codex：

~~~text
请从 https://github.com/gearssocial-arch/Chinese-Normative-Academic-Writing
安装 chinese-normative-academic-writing Skill。
~~~

### 手动安装

将仓库克隆到 Codex Skills 目录。

Windows PowerShell：

~~~powershell
git clone https://github.com/gearssocial-arch/Chinese-Normative-Academic-Writing.git "$env:USERPROFILE\.codex\skills\chinese-normative-academic-writing"
~~~

macOS 或 Linux：

~~~bash
git clone https://github.com/gearssocial-arch/Chinese-Normative-Academic-Writing.git ~/.codex/skills/chinese-normative-academic-writing
~~~

安装后，可在新任务中显式调用：

~~~text
$chinese-normative-academic-writing
~~~

也可以直接提出中文规范学术写作任务，让 Codex 根据 Skill 的描述自动匹配。

## 使用示例

### 判断研究问题

~~~text
使用 $chinese-normative-academic-writing 判断这个问题是否确实需要回答，
并检查它是否依赖未经证明的前提。
~~~

### 审核论证故事

~~~text
使用 $chinese-normative-academic-writing 检查这一节是否按照读者能够理解的顺序推进。
不要直接重写，先说明真正缺失的推理步骤。
~~~

### 修改抽象语言

~~~text
使用 $chinese-normative-academic-writing 修改这段中文论文。
优先写清谁在做什么、判断什么、根据什么，以及最后影响什么结果。
~~~

### 控制防御性写作

~~~text
使用 $chinese-normative-academic-writing 压缩这段局限性讨论。
保留会改变结论的真实边界，不主动发布非承重小问题。
~~~

## 与其他 Skills 协同

当对应 Skill 已安装并满足触发条件时，本 Skill 可以条件调用：

- anti-defensive-writing：研究日志式叙事、自我削弱和预先防御；
- citation-verification：文献、页码、引文和作者主张核验；
- paper-self-review：用户明确要求的投稿前全文审核；
- writing-anti-ai：用户明确要求去除 AI 写作痕迹或改善自然度。

这些 Skills 不是硬依赖。缺失时，本 Skill 会按自身原则继续工作，不应中断任务。

真实性、推理和来源边界始终优先。反防御性写作不能成为隐藏关键事实的理由。

## 设计边界

这个 Skill 不追求把论文写成一套无懈可击、预先回应所有质疑的封闭系统。

一篇合格的论文需要让读者清楚理解：

1. 论文研究什么；
2. 为什么这个问题确实需要回答；
3. 相邻研究已经完成什么；
4. 本文继续完成哪一步；
5. 证据如何支持关键推理；
6. 本文最后得到什么有限但明确的回答。

如果读者只能记住一串术语，却不能复述推理，论文仍然没有写清楚。

## 版本纪律

当前版本：**V1.0**

V1.0 内容层面已经封版。后续只有在真实使用中观察到可重复失败时，才针对失败更新 V1.1；不因为还能想象更多规则，就继续扩展框架。
