# 沟通与写作 — 王用源沟通方法学 Skill

Agent skill generated from《沟通与写作：语言表达与沟通技能》（第 2 版）by **王用源**，人民邮电出版社，2025-07（ISBN 9787115665256，188 千字，343 页），使用 [book-to-skill](https://github.com/virgiliojr94/book-to-skill) 把章节内容蒸馏为可被 LLM Agent 调用的高密度方法学 skill。

## 这个 skill 用来做什么

在以下场景套用作者的具体方法与"5 要素 / 4 功能 / 瓦伦达心态"等高密度心智模型：

- **写作**：撰写演讲稿、通知、报告、邮件、新闻稿等
- **即兴发言**：课堂发言、会议临时发言、答辩追问
- **面试**：自我介绍、压力应对、行为面试 STAR 答题
- **汇报**：口头汇报、向上汇报、邮件周报
- **组织会议**：主持会议、达成共识、撰写会议纪要
- **克服紧张**：上台前、面试前、任何"出场"关键场景
- **日常交际**：自我介绍、电话沟通、称呼礼仪

## 怎么用

在任何兼容 **Agent Skills 规范**的客户端（GitHub Copilot CLI / Amp / Claude Code / Hermes Agent / OpenClaw / Qoder 等）里调用：

```bash
# 任何 GitHub 用户都可一键安装（仓库已 public）
npx skills add https://github.com/rayyugz/goutong-yuxiezuo-skill --skill 沟通与写作
```

调用示例（在 agent 会话里直接说）：

- "用沟通与写作帮我写一篇开学典礼发言稿"
- "沟通与写作 第七章 关于职场单向表达的关键要点"
- "用沟通与写作的紧张克服 4 招帮我设计面试预案"
- "用沟通与写作 ch01 §1.2 的公文语体，起草一份《关于办公室开展保密检查的通知》"

> **注意**：本 repo 名为 `goutong-yuxiezuo-skill`（拼音 slug），是 GitHub 平台对中文 repo 名支持不完善后的 fallback。安装后的 skill 在客户端显示为"沟通与写作"。

## 文件清单

```
沟通与写作-skill/
├── README.md                       ← 本文件
├── SKILL.md                        ← skill 顶层入口（描述 + Core Frameworks + Chapter Index + Topic Index）
├── chapters/
│   ├── ch01-goutong-gaishu.md      ← 第 1 章 语言表达与沟通概述
│   ├── ch02-ziwo-renzhi.md         ← 第 2 章 自我认知与沟通素养
│   ├── ch03-richang-jiaoji.md      ← 第 3 章 日常交际与沟通方法
│   ├── ch04-geren-zhanshi.md       ← 第 4 章 个人展示与沟通方式
│   ├── ch05-jiti-jiaoliu.md        ← 第 5 章 集体交流与沟通效果
│   ├── ch06-mianshi.md             ← 第 6 章 保研、考研与求职面试
│   ├── ch07-zhichang-goutong.md    ← 第 7 章 职场语言与管理沟通
│   └── ext-jiaoyu-goutong.md       ← 拓展资料 教学语言与教育沟通
├── glossary.md                     ← 核心术语表（按章节 + 主题聚类）
├── patterns.md                     ← 可复用方法库（8 大类 30+ 方法）
└── cheatsheet.md                   ← 快速决策表（按"问题 / 场景 / 反例"索引）
```

## 内容结构（How to navigate）

- **SKILL.md** 是首要入口——`description` 字段决定了 agent 路由；`Core Frameworks` 段落列出 10 个最常被套用的心智模型；`Chapter Index` + `Topic Index` 给出"按问题查"的导航。
- **chapters/*.md** 是 on-demand 详细展开。每个章节按 `Core Idea → Frameworks → Key Concepts → Mental Models → Anti-patterns → Worked Example` 结构组织。
- **glossary.md** 是术语速查；**patterns.md** 是分场景方法合集；**cheatsheet.md** 是卡片式决策表。

## 元信息

- **Skill name (frontmatter)**：`goutong-yuxiezuo`（拼音 slug；frontmatter key 需 ASCII）
- **Display name**：沟通与写作
- **深度**：study（含 1 个 Worked Example / 章节）
- **来源书字数**：188 千字（PDF 343 页）
- **抽取方式**：pdfminer.six + NFKC normalize（修复 PDF 字体子集错位）
- **生成日期**：2026-09-20
- **覆盖 host**：GitHub Copilot CLI / Amp / Claude Code / Hermes Agent / OpenClaw / Qoder（5 host lens 已验证通过）

## 版权说明

本仓库的章节文件（`chapters/*.md`）、术语表、方法库、决策表均为**对原书的结构化整理与摘要**，按 book-to-skill SKILL.md 的"Extract structure, not summaries"原则生成——保留作者的方法学框架与术语，但**不含原书的逐字段落、案例全文、拓展训练题目**。本仓库的内容按"transformative fair use"原则公开。

原书《沟通与写作：语言表达与沟通技能》（第 2 版）版权归 **王用源 / 人民邮电出版社** 所有。如需引用原书的具体段落、案例，请购买原书。

如果你认为本仓库内容侵权，请联系 repo 所有者 rayyugz 处理。

## 如何贡献 / 反馈

本仓库作为个人学习产出，目前不开放 PR。如有问题或建议，可在 [book-to-skill 主项目](https://github.com/virgiliojr94/book-to-skill) 提 issue。

## 引用方式

如果你觉得这个 skill 有用，可以这样引用：

```bibtex
@misc{wangyongyuan2025goutong,
  title  = {沟通与写作：语言表达与沟通技能},
  author = {王用源},
  year   = {2025},
  edition= {第 2 版},
  publisher = {人民邮电出版社},
  isbn   = {9787115665256}
}
```

---

**License of derivative work**: MIT
**License of source book**: 版权归原出版方所有