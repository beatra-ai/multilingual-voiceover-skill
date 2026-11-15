# Multilingual Voiceover Skill

[English](./README.md) | [简体中文](./README.zh-CN.md) | 日本語

> 👉 こちらもどうぞ [Talking Avatar Video Skill](https://github.com/beatra-ai/talking-avatar-video-skill)

言語ごとの台本から、市場ごとに声を選び、発音とタイミングを先に試し、言語とセグメント別に納品するナレーション音声を作成。Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw のどれからでもそのまま使えます。

> [!IMPORTANT]
> 生成には [Beatra](https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill) アカウントが必要で、クレジットを消費します。スキル自体のインストールは無料です。

| 項目 | 内容 |
| --- | --- |
| **できること** | 各言語の原稿から多言語ナレーション音声を制作。市場ごとに声を選び、発音・話し方・尺を試してから、言語とセグメント別に納品します。 |
| **モデル** | MiniMax Voice Clone、MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo、Doubao Seed TTS 2.0、ElevenLabs v4 Turbo、ElevenLabs v4 |
| **動作要件** | Python 3.10 以上と、`SKILL.md` を読み込めるエージェント |
| **費用** | インストールは無料。生成のたびに Beatra アカウントのクレジットを消費しますが、課金されるのは、その生成を明示的に依頼したとき、または確認カードを承認したときだけです。 |
| **対応エージェント** | Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw |

<p align="center"><img src="assets/cover.webp" width="800" alt="4 言語のナレーションサンプルのカバー画像：ドットで描いた世界地図の上で、アメリカ、スペイン、中国、日本の声が 1 つの波形に重なる。Beatra AI で生成。"></p>

*4 言語のナレーションサンプルのカバー画像：ドットで描いた世界地図の上で、アメリカ、スペイン、中国、日本の声が 1 つの波形に重なる。Beatra AI で生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-multilingual-dubbing`](skills/ai-multilingual-dubbing) | [SKILL.md](skills/ai-multilingual-dubbing/SKILL.md) | 0.3.0 |

このリポジトリは [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-multilingual-dubbing) から自動的に公開されています。問題の報告はそちらへお願いします。

このスキルは `multilingual-voiceover` としても知られています（インストール名：`ai-multilingual-dubbing`）。

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

Antigravity CLI プラグインとして：

```bash
agy plugin install https://github.com/beatra-ai/multilingual-voiceover-skill
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

クリーン環境で動作確認済み：Antigravity CLI (2026-11-09)。

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

## 入力と出力

| | 種類 | 形式 | 仕様 |
| --- | --- | --- | --- |
| **入力** | テキスト：言語・市場ごとの原稿 | — | — |
| **出力** | 音声：言語・市場・セグメント別に整理したナレーション音声 | MP3、WAV、FLAC | 40 言語 |

## 技術仕様と出力上限

2026-11-14 時点。最新の一覧：https://docs.beatra.ai/ja/docs/models

- **アップロード** — 1 ファイルあたり最大 100 MB。下記の各モデルの入力制限も適用されます
- **ボイスクローン** — 1 モデル（MiniMax Voice Clone）／サンプル 10〜300 秒、最大 20 MB／本人の同意確認が必要
- **音声合成** — 5 モデル（MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo、Doubao Seed TTS 2.0、ElevenLabs v4 Turbo、ElevenLabs v4）／FLAC、MP3、OPUS、PCM、WAV／40 言語／サンプルレート 8、16、22.05、24、32、44.1 kHz／1 リクエストあたり最大 50000 文字
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

### 言語ごとに何を用意すればよいですか？

言語ごとの原稿です。言い回しは現地の話し言葉に合わせて整えられ、音声は市場とセグメント別に整理して渡すので、リップシンクや編集に使えます。

### 言語ごとのボイスはどう選びますか？

各市場の言語と視聴者に合うボイスを選びます。言語範囲と話し方がキャンペーン全体に合う場合は、同じボイスを複数の市場で使います。

### 音声はどう整理されて届きますか？

セグメントごとに1本ずつ、市場と言語ごとにまとめ、そのまま使う MP3 か、編集用の WAV または FLAC で渡します。

### ナレーションを動画の尺に合わせられますか？

はい。目標の尺を伝えると、原稿の長さと話す速さをその尺に合わせます。

## 更新とセキュリティ

2026 年 10 月のリリース以降、このスキルに自動更新機能はありません。インストールしたファイルだけを実行し、
自動的に置き換えることはありません。更新はインストールに使ったツール（`npx skills update ai-multilingual-dubbing` または
`gh skill update ai-multilingual-dubbing`）で行ってください。詳細はスキル内の `references/updates-and-security.md` を参照してください。

## ライセンス

このリポジトリのスキルファイル（`SKILL.md`、リファレンス、スクリプト）とこの README は [MIT-0](LICENSE) で提供しています。商用を含め、自由に使用・改変・再配布でき、クレジット表記は不要です。

生成は Beatra のクラウドサービスで行われ、[Beatra 利用規約](https://beatra.ai/terms?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill)が適用されます。

## リンク

- スキルページ — https://beatra.ai/skills/ai-multilingual-dubbing?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill
- ウェブサイト — https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill
- ドキュメント — https://docs.beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=multilingual-voiceover-skill
- コンソール — https://console.beatra.ai
- AI エージェント向け — https://beatra.ai/llms.txt （インデックス）· https://beatra.ai/llms-full.txt （全スキルを 1 ファイルに）
