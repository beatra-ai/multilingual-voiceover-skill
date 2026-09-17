# Multilingual Voiceover Skill

[English](./README.md) | 简体中文

根据各语言口播稿制作多语言旁白音频，按市场选声，先试听读音、语气和时长，再按语言与片段清晰交付，在 Claude Code、Codex 或 OpenClaw 里直接完成。

> [!IMPORTANT]
> 生成需要 [Beatra](https://beatra.ai) 账号并消耗积分，安装本身不收费。

| 问题 | 回答 |
| --- | --- |
| **能做什么** | 根据各语言口播稿制作多语言旁白音频，按市场选声，先试听读音、语气和时长，再按语言与片段清晰交付。 |
| **运行要求** | Python 3.10+，以及能加载 `SKILL.md` 的 Agent |
| **费用** | 安装免费。每次生成消耗 Beatra 账号积分，只有你明确要求这次生成或批准确认卡后才会付费。 |
| **支持的 Agent** | Claude Code、Codex、OpenClaw |

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-multilingual-dubbing`](skills/ai-multilingual-dubbing) | [SKILL.md](skills/ai-multilingual-dubbing/SKILL.md) | 0.1.8 |

本仓库由 [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-multilingual-dubbing) 自动发布，问题请到那里反馈。

## 安装

使用 [`skills`](https://skills.sh) CLI：

```bash
npx skills add beatra-ai/multilingual-voiceover-skill
```

使用 GitHub CLI：

```bash
gh skill install beatra-ai/multilingual-voiceover-skill ai-multilingual-dubbing
```

也可以克隆本仓库，把 `skills/ai-multilingual-dubbing` 复制到 `~/.claude/skills/`（Claude Code）、`~/.agents/skills/`（Codex）或 `~/.openclaw/skills/`（OpenClaw）。

或者把下面这段话发给你的 Agent：

```text
从 https://github.com/beatra-ai/multilingual-voiceover-skill 安装 ai-multilingual-dubbing skill（目录 skills/ai-multilingual-dubbing），然后按它的 SKILL.md 连接我的 Beatra 账号。
```

## 你能得到什么

- **从各市场口播稿开始** — 配音前确认产品名、卖点、数字、价格和行动号召，避免关键信息在不同市场发生偏差。
- **为不同受众选择合适声音** — 先从支持目标语言的声音中试听选择，再用代表片段检查实际表现。
- **先试听时长，再扩大制作** — 每个市场先做一个有代表性的片段，检查读音、语气、节奏和返回时长。

## 适用场景

- **出海产品与营销视频** — 根据各语言文案制作产品发布、讲解、广告和跨境电商视频所需的多语言旁白音轨。
- **课程与培训内容** — 按语言、课程和模块整理音频，先试听关键术语、数字和时长。
- **创作者与社交视频** — 为同一内容在不同市场发布准备按语言分类的旁白音频。
- **短剧与系列内容** — 按场景和片段制作对白或旁白音频，并为视频翻译、剪辑、同步和完整内容制作清晰组织素材。

## 常见问题

### 它会自动翻译并配好整条视频吗？

它根据各语言文案制作旁白音频，也可以协助起草更适合当地表达的口播稿；交付音轨按市场和片段整理，便于转录参考、语言审校、口型同步和成片剪辑。

### 多种语言应该怎样选择音色？

为每个市场匹配支持目标语言且适合受众的音色；如果同一声音的语言范围和表达适合完整活动，也可以跨市场沿用。

### 可以先试听再做完整版本吗？

可以。每个市场先制作一个有代表性的片段，检查读音、语气、节奏和时长，再把选定方向应用到其余音频。

### 怎样让旁白贴合原视频时长？

用目标时长指导文案长度和语速，比较试读返回的实际时长，再围绕最终剪辑调整口播稿或镜头节奏。

## 更新

安装后的 skill 每天最多检查一次新版本，替换前先校验官方归档，任何一步失败都不会动你已安装的版本。
随时可以关闭，见 skill 内的 `references/automatic-updates-and-safety.md`。

## 许可证

[MIT-0](LICENSE)：可自由使用、修改和再分发，包括商用，无需署名；与这些 skill 在 ClawHub 上的条款一致。
