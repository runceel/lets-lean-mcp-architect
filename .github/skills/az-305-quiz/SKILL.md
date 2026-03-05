---
name: az-305-quiz
description: >-
  AZ-305（Microsoft Azure Infrastructure Solutions の設計）の模擬問題を出題するスキル。
  ユーザーが「問題を出して」「クイズ」「模擬試験」「練習問題」などと言ったときに使用する。
---

## 概要

AZ-305 試験の模擬問題を出題し、ユーザーの回答に対してフィードバックを行う。

## 出題範囲

以下の 4 分野から出題する。配点の高い分野を優先的に出題すること。

| 分野 | 配点 |
|------|------|
| ID、ガバナンス、および監視ソリューションを設計する | 25〜30% |
| データ ストレージ ソリューションを設計する | 20〜25% |
| ビジネス継続性ソリューションを設計する | 15〜20% |
| インフラストラクチャ ソリューションを設計する | 30〜35% |

## Microsoft Learn からの情報取得

問題や解説の精度を高めるために、`microsoftlearn-microsoft_docs_search` ツールや `microsoftlearn-microsoft_docs_fetch` ツールを活用して Microsoft Learn の公式ドキュメントから情報を取得できる。

### 活用シーン

- 最新のサービス仕様や制約を確認してから問題を作りたいとき
- サービス比較（例: Application Gateway vs Front Door）の正確な違いを調べたいとき
- フィードバックに公式ドキュメントの URL を含めてユーザーの学習を支援したいとき

### 検索クエリの例

- `"Azure Application Gateway vs Front Door"` — サービス比較
- `"Azure SQL Database high availability"` — 可用性設計
- `"Azure Policy management group governance"` — ガバナンス設計
- `"Azure Cosmos DB consistency levels"` — データストア設計

## 出題手順

1. 問題を 1 問ずつ出題する
2. 問題文にはシナリオ（架空の企業名・状況・要件）を含め、実務に近い形式にする
3. 選択肢は 4 つ（A〜D）用意する
4. 選択肢の提示には必ず `ask_user` ツールを使い、ユーザーが選択肢を選べるようにする
5. `ask_user` の `allow_freeform` は `false` に設定する

## 回答後のフィードバック

ユーザーの回答後、以下の構成でフィードバックを提供する：

1. **正解/不正解の表示**
2. **正解の選択肢が正しい理由** — Azure 公式ドキュメントに基づいた具体的な説明
3. **不正解の選択肢がなぜ不適切か** — 表形式で各選択肢の問題点を簡潔に示す
4. **試験のポイント** — この問題から学ぶべき重要な考え方やキーワードの整理

## フィードバック後の進行

フィードバック提供後、`ask_user` ツールで「次の問題に進む」か「終了する」かを確認する。
終了時は正答数/出題数のサマリーを表示する。

## 出題のガイドライン

- 同じ分野の問題が連続しないよう、分野をローテーションする
- 難易度は実際の AZ-305 試験に合わせる
- 選択肢には「もっともらしいが不正解」な選択肢を含め、理解度を測れるようにする
- Azure のサービス比較（例: Azure SQL Database vs Cosmos DB、Application Gateway vs Front Door）を問う問題を適宜含める
- すべて日本語で出題・解説する

## 参考リンク

- 資格ページ: https://learn.microsoft.com/ja-jp/credentials/certifications/azure-solutions-architect/
- 試験ページ: https://learn.microsoft.com/ja-jp/credentials/certifications/exams/az-305/
- 学習ガイド: https://aka.ms/AZ305-StudyGuide
