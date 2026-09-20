# 沟通与写作 — 手动安装指南

> 这是 `沟通与写作` skill 的离线 zip 包，包含 13 个文件（SKILL.md + 8 个 chapter + glossary + patterns + cheatsheet + README + INSTALL）。
>
> Skill 生成自王用源《沟通与写作：语言表达与沟通技能》（第 2 版，2025，人民邮电出版社）——用 [book-to-skill](https://github.com/virgiliojr94/book-to-skill) 蒸馏而成。

## 在不同 Agent 上手动安装

把整个 zip 解压后，会得到一个 `沟通与写作-skill/` 目录。把**整个目录**移动到对应 Agent 的 personal skill 根目录下即可。**目录名可以改成你喜欢的（但建议保留 `沟通与写作` 或 `goutong-yuxiezuo` 作为目录名以便识别）**。

| Agent | personal skill 根目录 |
|---|---|
| **Qoder** | `~/.qoder/skills/` |
| **GitHub Copilot CLI** | `~/.copilot/skills/` |
| **Amp** | `~/.config/agents/skills/` |
| **Claude Code** | `~/.claude/skills/` |
| **OpenAI Codex** | `~/.agents/skills/` |
| **Cross-agent（兜底）** | `~/.agents/skills/` |
| **Hermes Agent** | `${HERMES_HOME:-~/.hermes}/skills/<category>/` |
| **OpenClaw** | `${OPENCLAW_STATE_DIR:-~/.openclaw}/skills/` |

### 安装步骤（以 Qoder 为例，其他 Agent 同理）

```bash
# 1. 解压 zip
unzip 沟通与写作-skill.zip

# 2. 移动到对应 skill 根目录
mv 沟通与写作-skill/ ~/.qoder/skills/

# 3. 验证
ls ~/.qoder/skills/沟通与写作-skill/
# 应该看到：SKILL.md  README.md  chapters/  glossary.md  patterns.md  cheatsheet.md
```

### 重启 Agent 让 skill 生效

- Qoder / Claude Code：**重启 session**
- GitHub Copilot CLI：运行 `/skills reload`
- Amp：**重启 session**
- Hermes Agent：开启新 session
- OpenClaw：先看 `openclaw skills list`，如果没有，**新 session** 让 watcher 重新扫描

## 验证安装成功

在你的 Agent 会话里说：

> 用沟通与写作帮我起草一份保密检查通知

如果 Agent 调用了 5 要素 / 公文语体 / PREP 等框架，就说明 skill 已生效。

## 更新 Skill（拿到新版本 zip 后）

直接用新版 zip 覆盖旧目录即可。**注意备份** `~/.qoder/skills/沟通与写作/` 里你之前可能做过的本地修改。

## 卸载

直接删除：

```bash
rm -rf ~/.qoder/skills/沟通与写作-skill
```

## 反馈

如果你发现 zip 缺文件、安装有问题、或想给朋友发，请确认以下事实：

- 本 zip 对应 GitHub repo: `https://github.com/rayyugz/goutong-yuxiezuo-skill`（**已 public**，任何人可装）
- 离线包与 GitHub repo 完全同步（截至 2026-09-20 22:35）
- 本仓库公开的依据：内容为"transformative fair use"——对原书做结构化整理 + 方法学抽取，不含原书大段原文

---

**License of derivative work**: MIT
**License of source book**: 版权归原出版方所有