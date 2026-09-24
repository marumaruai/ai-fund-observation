# AI Fund Observation

このサイトは、AIファンド観測企画の**公開ドキュメント**です。  
実データ（保有株数・評価額・月次レポート本文）は Private リポジトリ側にあり、ここには含まれません。

**これは対決ではありません。**  
どのAIが一番儲かるかを競うものではなく、同じ予算・同じ条件で各AIがどう考え、どう運用し、その判断が時間とともにどう変化するかを観察する企画です。

---

## 初めて読む方（人間向け）

1. [README](README.md) … 企画の概要
2. [investing/rules.md](investing/rules.md) … 正式な運用規約
3. [observer/history.md](observer/history.md) … なぜこのルールになったか（任意）

観測記録の公開先: note（marumaru）

---

## AIとして参加する場合

**最初に読むファイル**

1. [investing/handover.md](investing/handover.md) … 起動用要約（毎回ここから）
2. [investing/funds/](investing/funds/) の自分のファイル … 投資哲学と過去の判断履歴
3. [investing/rules.md](investing/rules.md) … 迷ったときの正式ルール（handover と矛盾したら rules 優先）

**月次判断の依頼テンプレート**

- [investing/prompts/monthly_prompt.md](investing/prompts/monthly_prompt.md) … 一次判断
- [investing/prompts/peer_review_prompt.md](investing/prompts/peer_review_prompt.md) … 相互レビュー・最終判断（任意）

**重要**

- 自分のファンドについてのみ売買判断・最終提案を行う
- 他ファンドはレビュー（分析・批評）のみ。代わりに売買判断しない
- 継続保有でも、「何が確認できれば売却・比率低下・入れ替えを検討するか」を観察可能な形で1つ以上書く
- 入れ替えで新規銘柄を採用する場合も、同様にトリガーを書く
- 月次の最終判断後、自分の `investing/funds/[AI名].md` に判断履歴を追記する（必須）
- 保有数量・評価額などの実データは `portfolio/holdings.md`（Private）が唯一の正。ここには転記しない

保有状況・当月レポートは観測者が Private から渡します。

---

## 運営者向け

- [observer/workflow.md](observer/workflow.md) … 月次運営マニュアル
- [observer/history.md](observer/history.md) … 企画全体の経緯
- [editorial/](editorial/) … 記事テンプレート・執筆方針

---

## Public / Private の役割

| 区分 | 内容 |
|---|---|
| Public（このサイト・このリポジトリ） | ルール、handover、各AIの哲学・判断履歴、プロンプト、運営ドキュメント |
| Private | `portfolio/holdings.md`（実データ台帳）、`reports/YYYY-MM.md`（月次実データ） |

---

## AI向け入口

機械可読の案内: [llms.txt](llms.txt)