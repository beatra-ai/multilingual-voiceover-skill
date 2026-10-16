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

<p align="center"><img src="assets/cover.webp" width="800" alt="Cover image for a four-language voice-over sample: a dotted world map where voices from the United States, Spain, China and Japan meet in one waveform. AI-generated with Beatra."></p>

*Cover image for a four-language voice-over sample: a dotted world map where voices from the United States, Spain, China and Japan meet in one waveform. AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-multilingual-dubbing`](skills/ai-multilingual-dubbing) | [SKILL.md](skills/ai-multilingual-dubbing/SKILL.md) | 0.2.6 |

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

## Examples

<p align="center"><img src="assets/cover.webp" width="800" alt="Cover image for a four-language voice-over sample: a dotted world map where voices from the United States, Spain, China and Japan meet in one waveform. AI-generated with Beatra."></p>

[▶ Listen (MP3)](assets/sample.mp3)

*The same product line for a fictional language-learning app, Lumo, voiced in English, Mandarin Chinese, Spanish and Japanese from four prepared scripts, one preset voice per language. AI-generated with Beatra.*

Prompt:

```text
[en] Meet Lumo, the language app that talks back. Ten minutes of real conversation a day, and new words start to stick. Open Lumo, and say hello to the world.
[zh] 认识一下 Lumo，一个会陪你开口说话的语言学习应用。每天十分钟真实对话，新单词自然记得牢。打开 Lumo，向世界打个招呼吧。
[es] Te presentamos Lumo, la app de idiomas que te responde. Diez minutos de conversación real al día, y las palabras nuevas se quedan contigo. Abre Lumo y saluda al mundo.
[ja] Lumoは、話しかけると答えてくれる語学アプリです。毎日10分、本物の会話を続けるだけで、新しい単語が自然と身につきます。Lumoを開いて、世界にあいさつしましょう。
```

## Specs

As of 2026-10-16. Live list: https://docs.beatra.ai/en/docs/models

- **Text to speech** — 2 models (MiniMax Speech 2.8 HD, MiniMax Speech 2.8 Turbo); FLAC, MP3, OPUS, PCM, WAV; 40 languages; up to 44.1 kHz; up to 50000 characters per request

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

## Updates and security

Since the 2026-10 release, this skill contains no self-updater: it runs only the
files you installed and never replaces them on its own. Update it with the tool
you installed it with — `npx skills update ai-multilingual-dubbing` or `gh skill update ai-multilingual-dubbing`.
Details: `references/updates-and-security.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.

## Links

- Website — https://beatra.ai
- Docs — https://docs.beatra.ai
- Console — https://console.beatra.ai
