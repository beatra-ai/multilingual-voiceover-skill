# Multilingual Voiceover Skill

English | [简体中文](./README.zh-CN.md) | [日本語](./README.ja.md)

> 👉 See also [Talking Avatar Video Skill](https://github.com/beatra-ai/talking-avatar-video-skill)

Create reviewable voice-over audio for each language from your per-language scripts, with voices cast for each market, pronunciation and timing pilots first, and delivery organized by language and segment, from inside Claude Code, Cursor, Codex, Windsurf, Cline, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Create reviewable multilingual voice-over audio from scripts for each language, with deliberate casting, pronunciation and timing pilots, and delivery organized by market and segment. |
| **Models** | MiniMax Voice Clone, MiniMax Speech 2.8 HD, MiniMax Speech 2.8 Turbo, Doubao Seed TTS 2.0, ElevenLabs v4 Turbo, ElevenLabs v4 |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw |

<p align="center"><img src="assets/cover.webp" width="800" alt="Cover image for a four-language voice-over sample: a dotted world map where voices from the United States, Spain, China and Japan meet in one waveform. AI-generated with Beatra."></p>

*Cover image for a four-language voice-over sample: a dotted world map where voices from the United States, Spain, China and Japan meet in one waveform. AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-multilingual-dubbing`](skills/ai-multilingual-dubbing) | [SKILL.md](skills/ai-multilingual-dubbing/SKILL.md) | 0.3.1 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-multilingual-dubbing). Report issues there.

Also known as `multilingual-voiceover` (installed under the Beatra slug `ai-multilingual-dubbing`).

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/multilingual-voiceover-skill
```

As a Claude Code plugin:

```bash
claude plugin marketplace add beatra-ai/multilingual-voiceover-skill
claude plugin install ai-multilingual-dubbing@multilingual-voiceover-skill
```

As a Codex plugin:

```bash
codex plugin marketplace add beatra-ai/multilingual-voiceover-skill
codex plugin add ai-multilingual-dubbing@multilingual-voiceover-skill
```

As a GitHub Copilot CLI plugin:

```bash
copilot plugin marketplace add beatra-ai/multilingual-voiceover-skill
copilot plugin install ai-multilingual-dubbing@multilingual-voiceover-skill
```

As a Gemini CLI extension:

```bash
gemini extensions install https://github.com/beatra-ai/multilingual-voiceover-skill
```

As an Antigravity CLI plugin:

```bash
agy plugin install https://github.com/beatra-ai/multilingual-voiceover-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/multilingual-voiceover-skill ai-multilingual-dubbing
```

Or clone this repository and copy `skills/ai-multilingual-dubbing` into `~/.claude/skills/` for Claude Code,
`~/.cursor/skills/` for Cursor, `~/.agents/skills/` for Codex, `~/.codeium/windsurf/skills/` for Windsurf,
`~/.cline/skills/` for Cline, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the ai-multilingual-dubbing skill from https://github.com/beatra-ai/multilingual-voiceover-skill (folder skills/ai-multilingual-dubbing), then follow its SKILL.md to connect my Beatra account.
```

Tested in clean-room CI: Antigravity CLI (2026-11-09).

## Examples

<p align="center"><img src="assets/cover.webp" width="800" alt="Cover image for a four-language voice-over sample: a dotted world map where voices from the United States, Spain, China and Japan meet in one waveform. AI-generated with Beatra."></p>

[▶ Listen (MP3)](assets/sample.mp3)

*The same product line for a fictional language-learning app, Lumo, voiced in English, Mandarin Chinese, Spanish and Japanese from four prepared scripts, one preset voice per language. AI-generated with Beatra.*

Ask your agent:

```text
I have the Lumo launch line in four languages (./scripts/en.txt, zh.txt, es.txt, ja.txt). Cast one fitting voice per language, do a short pronunciation check first, then deliver the four reads in order.
```

Prompt:

```text
[en] Meet Lumo, the language app that talks back. Ten minutes of real conversation a day, and new words start to stick. Open Lumo, and say hello to the world.
[zh] 认识一下 Lumo，一个会陪你开口说话的语言学习应用。每天十分钟真实对话，新单词自然记得牢。打开 Lumo，向世界打个招呼吧。
[es] Te presentamos Lumo, la app de idiomas que te responde. Diez minutos de conversación real al día, y las palabras nuevas se quedan contigo. Abre Lumo y saluda al mundo.
[ja] Lumoは、話しかけると答えてくれる語学アプリです。毎日10分、本物の会話を続けるだけで、新しい単語が自然と身につきます。Lumoを開いて、世界にあいさつしましょう。
```

## Inputs and outputs

| | Type | Formats | Specifications |
| --- | --- | --- | --- |
| **Input** | Text — Prepared script for each language and market | — | — |
| **Output** | Audio — Voice-over tracks organized by language, market, and segment | MP3, WAV, FLAC | 40 languages |

## Technical Specifications & Output Limits

As of 2026-11-14. Live list: https://docs.beatra.ai/en/docs/models

- **Uploads** — up to 100 MB per file; the per-model input limits below also apply
- **Voice cloning** — 1 model (MiniMax Voice Clone); sample 10–300 s, up to 20 MB; consent attestation required
- **Text to speech** — 5 models (MiniMax Speech 2.8 HD, MiniMax Speech 2.8 Turbo, Doubao Seed TTS 2.0, ElevenLabs v4 Turbo, ElevenLabs v4); FLAC, MP3, OPUS, PCM, WAV; 40 languages; sample rates 8, 16, 22.05, 24, 32, 44.1 kHz; up to 50000 characters per request
  - Languages (ISO 639 codes): zh, yue, en, es, fr, ru, de, pt, ar, it, ja, ko, id, vi, tr, nl, uk, th, pl, ro, el, cs, fi, hi, bg, da, he, ms, fa, sk, sv, hr, fil, hu, no, sl, ca, nn, ta, af

## Why use Beatra instead of calling model APIs directly

- **One account for every model this skill uses** — Voice cloning 1; Text to speech 5 (MiniMax Voice Clone, MiniMax Speech 2.8 HD, MiniMax Speech 2.8 Turbo, Doubao Seed TTS 2.0, ElevenLabs v4 Turbo, ElevenLabs v4) (as of 2026-11-14), behind one Beatra sign-in; no keys from individual model providers to manage.
- **You decide what gets paid for** — Paid renders run only when you ask for that exact render or approve its card, which shows the live credit estimate.
- **Direction before rendering** — the skill plans, directs, and reviews the work, then renders it on Beatra.
- **Files you can verify** — every file under `skills/` matches the release archive on cdn.beatra.ai byte for byte, checked by SHA-256 before each push.
- **Updates you control** — no self-updater; update with the tool you installed it with.
- **Runs in your agent** — Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw.

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

### What do I need for each language?

A script in each language. The wording can be tuned for local speech, and the tracks come organized by market and segment for lip sync and editing.

### Which voice is used for each language?

Each market gets a voice that supports its language and suits its audience; one voice can carry across markets when its languages and delivery fit the whole campaign.

### How are the tracks organized?

One track per segment, grouped by market and language, as MP3 for direct use or WAV or FLAC for editing.

### Can the narration match a video's length?

Yes. Give the target duration, and the script length and pace are set to fit it.

## Updates and security

Since the 2026-10 release, this skill contains no self-updater: it runs only the
files you installed and never replaces them on its own. Update it with the tool
you installed it with — `npx skills update ai-multilingual-dubbing` or `gh skill update ai-multilingual-dubbing`.
Details: `references/updates-and-security.md` inside the skill.

## License

The skill files in this repository (`SKILL.md`, references, and scripts) and this README are licensed under
[MIT-0](LICENSE): free to use, modify, and redistribute, including commercially, with no attribution required.

Media generation runs on Beatra's cloud service under the [Beatra Terms of Service](https://beatra.ai/terms?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill).

## Links

- Skill page — https://beatra.ai/skills/ai-multilingual-dubbing?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill
- Website — https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill
- Docs — https://docs.beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill
- Console — https://console.beatra.ai
- For AI agents — https://beatra.ai/llms.txt (index) · https://beatra.ai/llms-full.txt (every skill in one file)
