# skills-active — 我的 AI 技能启用集

从这里拷贝 skill 到你的 AI 工具技能目录，用到哪个拷哪个，避免一次全装造成冲突。

## 来源

本目录的 skill 均来自开源仓库 [mattpocock/skills](https://github.com/mattpocock/skills)（MIT 协议），作者 Matt Pocock（Total TypeScript 创始人）。更新 skill 时先同步上游仓库再重新拷贝。

## 当前启用

| Skill | 用途 |
|---|---|
| `grill-me` | 需求不清楚时，让 AI 向你连环提问，把想法磨锋利再动手 |
| `to-spec` | 把对话讨论固化成 spec 文档（问题陈述 → 用户故事 → 实现决策 → 测试决策） |
| `setup-matt-pocock-skills` | 一次性配置向导：指定 to-spec 的问题跟踪器（GitHub issue / 本地文件等） |
| `grilling` | grill-me 依赖的底层「拷问」引擎，由 grill-me 调用，也可单独使用 |

均为「人主动调用」型（`disable-model-invocation: true`），不会自动触发，互不干扰。

## 新机器重建（2 分钟）

```bash
# 1. 克隆本启用集
git clone https://github.com/Ydking12/skills-active.git

# 2. 获取上游完整仓库（取最新版 skill 用）
git clone https://github.com/mattpocock/skills.git

# 3. 把要用的 skill 整个文件夹拷进你 AI 工具的技能目录（见下表）
```

## 各工具的技能目录

| 工具 | 项目级 | 全局 |
|---|---|---|
| Claude Code | `.claude/skills/` | `~/.claude/skills/` |
| Codex / Antigravity | `.agents/skills/` | `~/.agents/skills/` |
| Cursor | `.cursor/skills/` | `~/.cursor/skills/` |
| Gemini CLI | `.gemini/skills/` | `~/.gemini/skills/` |
| GitHub Copilot | `.github/skills/` | `~/.copilot/skills/` |

拷贝时带上文件夹里的全部内容（`SKILL.md` + `agents/` 等）。

## 如何增删

- **加 skill**：从上游仓库 `skills/engineering` 或 `skills/productivity` 里挑，整个文件夹拷进本目录，再拷到工具目录
- **删 skill**：从本目录和工具目录各删掉对应文件夹即可
- **改 skill**：直接改本目录里的 `SKILL.md`，然后把改动同步到工具目录；上游更新后注意 diff 合并
