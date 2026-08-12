# AI Fund Observation

新NISA成長投資枠を使い、複数のAI(Claude / ChatGPT / Gemini / Grok、将来的にLocalLLM枠も予定)にそれぞれ個別株を提案・運用させ、各AIの銘柄選定と運用スタイルの違いを比較記録する観測企画です。

**これは対決ではありません。** どのAIが一番儲かるかを競うものではなく、同じ予算・同じ条件下で各AIがどう考え、どう運用するか、そしてその判断が時間とともにどう変化していくかを観察する企画です。

観測記録はnote(marumaru)で公開しています。

## Features

- 複数AIを競わせるのではなく、それぞれの投資哲学と判断の変化を観察することを目的としています。
- GitHubをAIと人間が共有する知識ベースとして運用しています。
- AIは `investing/handover.md` を起点として新しいセッションでも企画へ再参加できるよう設計されています。
- 運営ルール・履歴・テンプレートを公開し、実データのみPrivateリポジトリで管理しています。

## AIの方へ

このプロジェクトに初めて参加する場合、まず `investing/handover.md` を読んでください。
次に `investing/funds/[あなた自身のAI名].md` を読み、自分自身の過去の判断を確認してから、依頼された判断を行ってください。

判断に迷った場合は、`investing/rules.md` を正としてください。
`investing/handover.md` はその要約であり、矛盾がある場合は `investing/rules.md` が優先されます。

## このリポジトリの構成

このリポジトリ(Public)には、公開して問題ない「ルール・哲学・履歴・テンプレート」を置いています。実データ(保有株数・取得単価・評価額・月次レポート)は別のPrivateリポジトリで管理しています。

```
ai-fund-observation/ (Public, このリポジトリ)
├── README.md                 … このファイル
├── index.md                  … GitHub Pages 向けの案内
├── llms.txt                  … AI向けの入口（簡潔な目次）
├── CHANGELOG.md              … rules の変更履歴
│
├── investing/                … 投資判断に関する公開ドキュメント
│   ├── rules.md              … 正式な運用規約
│   ├── handover.md           … AI向け起動ファイル（セッション開始時の要約）
│   ├── funds_template.md     … 各AIファンドのファイル雛形
│   ├── funds/
│   │   ├── claude.md         … Claudeファンドの投資哲学・判断履歴
│   │   ├── chatgpt.md        … ChatGPTファンドの投資哲学・判断履歴
│   │   ├── gemini.md         … Geminiファンドの投資哲学・判断履歴
│   │   ├── grok.md           … Grokファンドの投資哲学・判断履歴
│   │   └── local.md          … LocalLLM枠（将来用、現在ダミー）
│   └── prompts/
│       ├── monthly_prompt.md
│       └── peer_review_prompt.md
├── editorial/                … 記事執筆・公開に関するドキュメント
│   ├── style-guide.md        … note執筆方針・無料／有料の切り分け
│   ├── paid-content.md       … 有料コンテンツ候補
│   └── templates/
│       ├── monthly-template.md    … 月次記事（途中から有料）の雛形
│       ├── summary-template.md    … 要約記事（任意）の雛形
│       └── article-template.md    … 月次以外の記事の雛形
│
├── observer/                 … 観測者向けの運営・経緯
│   ├── workflow.md           … 月次運営マニュアル（投資／編集フロー）
│   ├── history.md            … 企画全体の経緯・決定の記録
│   ├── archive/              … 過去資料
│   └── notes/                … 運営メモ
│
└── templates/                … AIへの依頼テンプレート
    ├── monthly_prompt.md     … 一次判断依頼
    └── peer_review_prompt.md … 相互レビュー（任意）

ai-fund-observation-private/ (Private, 別リポジトリ)
├── portfolio/
│   └── holdings.md           … 保有株数・取得単価・評価額（唯一の実データ台帳）
└── reports/
    └── YYYY-MM.md            … 月次の市場概況・AIコメントまとめ（実データ含む）
```

## 免責事項

本企画における「ファンド」は、金融商品取引法上の投資信託・ファンド等を指すものではありません。取り上げる銘柄はあくまで各AIへの提案依頼に基づく選定であり、実際の売買判断・資金拠出・最終決定はすべて筆者個人が行っています。特定の金融商品の勧誘や投資助言を目的とするものではありません。投資はご自身の判断と責任でお願いします。

本企画の規約・フォーマット・リポジトリ構成は、自由に参考・Forkしていただいて構いません。
同様の企画を公開される際は、このリポジトリを参考にした旨を記載していただけると嬉しいです。
