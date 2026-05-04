# Teal 使い方ガイドブック

[![Zenn Book](https://img.shields.io/badge/Zenn-Book-3ea8ff?logo=zenn)](https://zenn.dev/cobaltsato/books/teal-user-guide)

AI 自動化エージェント [**Teal**](https://teal-me.io) の使い方を、**Web ダッシュボード・LINE・Slack** からの操作と **Google・LINE・Slack・Notion・X** の5連携先まで、実例で順を追って解説するガイドブックです。

公開先 → **<https://zenn.dev/cobaltsato/books/teal-user-guide>**

## 章構成

| # | 章 |
| --- | --- |
| 01 | はじめに — このガイドの読み方 |
| 02 | 5分で始める Teal |
| 03 | Web ダッシュボードの構成 |
| 04 | 5つの連携先 — Google・LINE・Slack・Notion・X |
| 05 | カテゴリ — 業種・機能別テンプレート |
| 06 | 役割（ロール） — AI に専門分野を持たせる |
| 07 | スキル — AI が学習する能力 |
| 08 | 自動タスク — AI が定期的に動くしくみ |
| 09 | 外部サービス連携 — 5つの連携先と接続する |
| 10 | ユースケース集 — 6つの業務パターン |
| 11 | つまずきやすいポイント — よくある質問と確認順 |
| 99 | 次のステップ |

## ディレクトリ構成

```
.
├── books/
│   └── teal-user-guide/        本のチャプターと設定
│       ├── config.yaml         本のメタデータ（slug・章順）
│       ├── cover.svg / .png    カバー画像（500×700 / 1500×2100）
│       ├── *.md                各章
│       └── images/             SVG 編集ソース＋ビルド用ロゴ
└── images/
    └── teal-user-guide/        Zenn が参照する公開画像（PNG/SVG）
```

本文の画像参照は Zenn 標準の絶対パスで書きます。

```markdown
![alt](/images/teal-user-guide/01-overview.png)
```

## 図解の作り方

各章の図解は SVG で書き、`qlmanage` + `sips` で PNG に変換しています。

```bash
cd images/teal-user-guide
qlmanage -t -s 2400 -o . target.svg
sips -z 1080 1920 target.svg.png --out target.png
rm target.svg.png
```

トーンは「Official Docs 風」で統一（Stripe Docs / Linear のような落ち着いた配色）。

## 編集 → 公開フロー

1. 章 Markdown または SVG をローカルで編集
2. SVG を変えたら PNG を再生成
3. `git push origin main`
4. Zenn の GitHub 連携が自動でデプロイ

## 公開設定

- **公開ステータス**: 公開中（`books/teal-user-guide/config.yaml` の `published: true`）
- **価格**: 0円（無料で読める本）
- **ライセンス**: 本文は著者帰属、ロゴは Teal 側帰属

## クレジット

本書は Teal 運営から情報提供を受けて執筆しています。
