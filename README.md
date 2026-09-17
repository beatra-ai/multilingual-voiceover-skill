# Multilingual Voiceover Skill

English | [简体中文](./README.zh-CN.md)

Create reviewable voice-over audio for each language from your per-language scripts, with voices cast for each market, pronunciation and timing pilots first, and delivery organized by language and segment, from inside Claude Code, Codex, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Create reviewable multilingual voice-over audio from scripts for each language, with deliberate casting, pronunciation and timing pilots, and delivery organized by market and segment. |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Codex, OpenClaw |

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-multilingual-dubbing`](skills/ai-multilingual-dubbing) | [SKILL.md](skills/ai-multilingual-dubbing/SKILL.md) | 0.1.8 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-multilingual-dubbing). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/multilingual-voiceover-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/multilingual-voiceover-skill ai-multilingual-dubbing
```

Or clone this repository and copy `skills/ai-multilingual-dubbing` into `~/.claude/skills/` for Claude Code,
`~/.agents/skills/` for Codex, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the ai-multilingual-dubbing skill from https://github.com/beatra-ai/multilingual-voiceover-skill (folder skills/ai-multilingual-dubbing), then follow its SKILL.md to connect my Beatra account.
```

## What you get

- **Start from market-ready spoken copy** — Keep product names, claims, numbers, and calls to action clear in every script before audio production.
- **Cast for each audience** — Choose from voices that support the target language and compare previews with a representative pilot.
- **Pilot timing before scale** — Test a representative segment for pronunciation, pace, tone, and returned duration before producing the rest.

## Use cases

- **Product and marketing videos** — Create localized narration audio for launches, explainers, ads, and cross-border commerce videos from prepared scripts.
- **Courses and training libraries** — Organize narration by language, lesson, and module, with a representative timing and pronunciation pilot.
- **Creator and social videos** — Prepare reusable voice-over tracks for channels publishing the same story in several markets.
- **Short drama and episodic narration** — Produce dialogue or narration as organized audio segments for translation, editing, synchronization, and the wider localization workflow.

## FAQ

### Does it translate and dub an uploaded video automatically?

It creates narration audio from scripts prepared for each language and can help shape localized spoken wording. The organized tracks are ready for transcription references, language review, lip sync, and finished-video editing.

### How are voices selected across languages?

Match each market with a voice that supports its language and audience; reuse one voice across markets when its language range and delivery fit the full campaign.

### Can I test before producing the whole release?

Yes. Pilot one meaningful segment per market, review pronunciation, tone, pace, and duration, then carry the selected direction into the remaining narration tracks.

### How do I tune the narration to a video duration?

Use the target duration to guide script length and pace, compare the returned pilot duration, and refine the spoken wording or edit timing for the final cut.

## Updates

Each installed skill checks for a new version at most once a day, verifies the
official archive before replacing itself, and leaves your installation untouched
if anything fails. Turn it off at any time — see
`references/automatic-updates-and-safety.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.
