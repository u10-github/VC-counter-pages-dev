# runbook: VC-counter-pages-dev

## サービス概要
- デプロイ: 検証用静的配信（develop運用）
- URL: https://u10-github.github.io/VC-counter-pages-dev/
- オーナー: u10-github

## 初動トリアージ
- 症状:
  - develop反映後に検証画面が古いままになる
- 最初の確認:
  - [ ] 最新CIステータス
  - [ ] 直近でマージされたPR
  - [ ] 障害時間帯のログ

## インシデント記録テンプレート
### ID: RB-YYYYMMDD-N
- 症状: 例）develop反映後に検証画面が古いままになる
- 影響範囲: 例）主要ユーザー操作の一部が失敗
- 再現手順: 例）直近リリース後に対象ページを開いて操作
- 確認項目:
  - [ ] data/timeseries_6m.json の更新を確認
  - [ ] 検証用ページで表示を確認
- 応急対応: 例）直前の安定コミットにロールバック
- 恒久対応: 例）原因修正 + 回帰チェック追加
- 関連eval: 例）EV-VC-counter-pages-dev-001
- 関連PR: 例）https://github.com/u10-github/VC-counter-pages-dev/pull/123

## 更新ポリシー
- runbook + evals更新前にインシデントをクローズしない。
- 記録は短く保つ: 症状 -> 確認 -> 対処 -> 恒久対応。
