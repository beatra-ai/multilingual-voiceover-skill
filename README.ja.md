# Multilingual Voiceover Skill

[English](./README.md) | [简体中文](./README.zh-CN.md) | 日本語

> 👉 こちらもどうぞ [Talking Avatar Video Skill](https://github.com/beatra-ai/talking-avatar-video-skill)

言語ごとの台本から、市場ごとに声を選び、発音とタイミングを先に試し、言語とセグメント別に納品するナレーション音声を作成。Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw のどれからでもそのまま使えます。

> [!IMPORTANT]
> 生成には [Beatra](https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill) アカウントが必要で、クレジットを消費します。スキル自体のインストールは無料です。

| 項目 | 内容 |
| --- | --- |
| **できること** | 各言語の原稿から多言語ナレーション音声を制作。市場ごとに声を選び、発音・話し方・尺を試してから、言語とセグメント別に納品します。 |
| **モデル** | MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo |
| **動作要件** | Python 3.10 以上と、`SKILL.md` を読み込めるエージェント |
| **費用** | インストールは無料。生成のたびに Beatra アカウントのクレジットを消費しますが、課金されるのは、その生成を明示的に依頼したとき、または確認カードを承認したときだけです。 |
| **対応エージェント** | Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw |

<p align="center"><img src="assets/cover.webp" width="800" alt="4 言語のナレーションサンプルのカバー画像：ドットで描いた世界地図の上で、アメリカ、スペイン、中国、日本の声が 1 つの波形に重なる。Beatra AI で生成。"></p>

*4 言語のナレーションサンプルのカバー画像：ドットで描いた世界地図の上で、アメリカ、スペイン、中国、日本の声が 1 つの波形に重なる。Beatra AI で生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-multilingual-dubbing`](skills/ai-multilingual-dubbing) | [SKILL.md](skills/ai-multilingual-dubbing/SKILL.md) | 0.2.9 |

このリポジトリは [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-multilingual-dubbing) から自動的に公開されています。問題の報告はそちらへお願いします。

## インストール

[`skills`](https://skills.sh) CLI を使う場合：

```bash
npx skills add beatra-ai/multilingual-voiceover-skill
```

Claude Code プラグインとして：

```bash
claude plugin marketplace add beatra-ai/multilingual-voiceover-skill
claude plugin install ai-multilingual-dubbing@multilingual-voiceover-skill
```

Codex プラグインとして：

```bash
codex plugin marketplace add beatra-ai/multilingual-voiceover-skill
codex plugin add ai-multilingual-dubbing@multilingual-voiceover-skill
```

GitHub Copilot CLI プラグインとして：

```bash
copilot plugin marketplace add beatra-ai/multilingual-voiceover-skill
copilot plugin install ai-multilingual-dubbing@multilingual-voiceover-skill
```

Gemini CLI 拡張機能として：

```bash
gemini extensions install https://github.com/beatra-ai/multilingual-voiceover-skill
```

GitHub CLI を使う場合：

```bash
gh skill install beatra-ai/multilingual-voiceover-skill ai-multilingual-dubbing
```

または、このリポジトリをクローンして `skills/ai-multilingual-dubbing` を次の場所にコピーします：Claude Code は `~/.claude/skills/`、Cursor は `~/.cursor/skills/`、Codex は `~/.agents/skills/`、Windsurf は `~/.codeium/windsurf/skills/`、Cline は `~/.cline/skills/`、OpenClaw は `~/.openclaw/skills/`。

または、次の文をエージェントに貼り付けてください：

```text
https://github.com/beatra-ai/multilingual-voiceover-skill から ai-multilingual-dubbing スキル（フォルダ skills/ai-multilingual-dubbing）をインストールし、その SKILL.md に従って私の Beatra アカウントに接続してください。
```

## 作例

<p align="center"><img src="assets/cover.webp" width="800" alt="4 言語のナレーションサンプルのカバー画像：ドットで描いた世界地図の上で、アメリカ、スペイン、中国、日本の声が 1 つの波形に重なる。Beatra AI で生成。"></p>

[▶ 試聴する（MP3）](assets/sample.mp3)

*架空の語学学習アプリ Lumo の同じ商品コピーを、用意した 4 本の台本から英語、中国語（普通話）、スペイン語、日本語で読み上げたもの。言語ごとに 1 つのプリセットボイス。Beatra AI で生成。*

エージェントへの依頼例：

```text
Lumo のローンチコピーを 4 言語で用意しました（./scripts/en.txt、zh.txt、es.txt、ja.txt）。言語ごとに合う声を 1 つ選び、先に短い発音チェックをしてから、4 本を順番に納品して。
```

プロンプト：

```text
[en] Meet Lumo, the language app that talks back. Ten minutes of real conversation a day, and new words start to stick. Open Lumo, and say hello to the world.
[zh] 认识一下 Lumo，一个会陪你开口说话的语言学习应用。每天十分钟真实对话，新单词自然记得牢。打开 Lumo，向世界打个招呼吧。
[es] Te presentamos Lumo, la app de idiomas que te responde. Diez minutos de conversación real al día, y las palabras nuevas se quedan contigo. Abre Lumo y saluda al mundo.
[ja] Lumoは、話しかけると答えてくれる語学アプリです。毎日10分、本物の会話を続けるだけで、新しい単語が自然と身につきます。Lumoを開いて、世界にあいさつしましょう。
```

## 技術仕様と出力上限

2026-10-18 時点。最新の一覧：https://docs.beatra.ai/ja/docs/models

- **音声合成** — 2 モデル（MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo）／FLAC、MP3、OPUS、PCM、WAV／40 言語／サンプルレート 8、16、22.05、24、32、44.1 kHz／1 リクエストあたり最大 50000 文字
  - 言語（ISO 639 コード）：zh, yue, en, es, fr, ru, de, pt, ar, it, ja, ko, id, vi, tr, nl, uk, th, pl, ro, el, cs, fi, hi, bg, da, he, ms, fa, sk, sv, hr, fil, hu, no, sl, ca, nn, ta, af

## 得られるもの

- **市場ごとの読み原稿から開始** — 商品名、訴求、数字、価格、行動を促す表現を音声制作前に確認します。
- **市場に合う声を選択** — 対象言語に対応する声のプレビューを聞き、代表箇所で実際の仕上がりを確かめます。
- **尺を試してから展開** — 各市場の代表箇所で発音、話し方、テンポ、実際の長さを確認します。

## 活用シーン

- **海外向け商品・マーケティング動画** — 商品発表、説明、広告、越境EC動画に使う多言語ナレーション音声を、各言語原稿から制作します。
- **講座と研修コンテンツ** — 言語、講座、モジュール別に音声を整理し、重要な用語、数字、尺を先に確認します。
- **クリエイター・SNS動画** — 同じ内容を複数市場へ届けるためのナレーション音声を言語別に用意します。
- **ショートドラマとシリーズ** — 台詞やナレーションを場面・セグメント別に音声化し、翻訳確認、編集、同期、全体の制作に使いやすく整理します。

## よくある質問

### 動画をアップロードすれば、自動で翻訳と吹き替えまで完了しますか？

各言語原稿からナレーション音声を制作し、自然な現地向け表現の案も整えます。音声は、文字起こし参照、言語確認、リップシンク、完成動画の編集に使いやすい形で納品します。

### 多言語ではどのように声を選びますか？

各市場の言語と視聴者に合う声を選び、言語範囲と表現がキャンペーン全体に合う場合は同じ声を複数市場で使います。

### 全体を作る前に試せますか？

はい。各市場の代表箇所で発音、話し方、テンポ、尺を確認し、選んだ方向を残りの音声へ展開します。

### ナレーションを元動画の尺に合わせるには？

目標尺を原稿の長さと話速に反映し、試作の実際の長さを比べて、完成編集に合わせて話す原稿や映像のテンポを整えます。

## 更新とセキュリティ

2026 年 10 月のリリース以降、このスキルに自動更新機能はありません。インストールしたファイルだけを実行し、
自動的に置き換えることはありません。更新はインストールに使ったツール（`npx skills update ai-multilingual-dubbing` または
`gh skill update ai-multilingual-dubbing`）で行ってください。詳細はスキル内の `references/updates-and-security.md` を参照してください。

## ライセンス

[MIT-0](LICENSE)：商用を含め、自由に使用・改変・再配布できます。クレジット表記は不要です。ClawHub 上のこれらのスキルと同じ条件です。

## リンク

- ウェブサイト — https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill
- ドキュメント — https://docs.beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill
- コンソール — https://console.beatra.ai
- AI エージェント向け — https://beatra.ai/llms.txt （インデックス）· https://beatra.ai/llms-full.txt （全スキルを 1 ファイルに）
