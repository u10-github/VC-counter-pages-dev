# VC-counter Pages Dev

このリポジトリは、`VC-counter` の **開発検証用** Web UI を配信するためのリポジトリです。

## 編集責務
- このリポジトリ: 検証用の静的UI（`index.html`, `app.js`, `style.css`）
- `VC-counter`: backend / JSON生成 / push制御（UIは編集しない）
- `VC-counter-pages`: 本番公開用 UI

## 送信経路マトリクス
- DS218 dev → `VC-counter-pages-dev` / `develop`
- DS218 prod → `VC-counter-pages` / `main`

## 運用方針
- 検証ブランチ: `develop`
- `data/timeseries_6m.json` と `data/meta.json` は DS218 dev から自動更新される
- 本番公開は行わず、検証完了後に変更を `VC-counter-pages` へ反映する
