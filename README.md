# sbx-platform

Docker Sandboxes で使う共通定義（skills・指示文・ネットワーク許可・MCP）をまとめて管理し、kit として配布するリポジトリ。

> 雛形の段階です。中身は順に詰めていきます。

## 何をどこで管理するか

| 置き場所 | 中身 |
|---|---|
| `skills/` | 配布する skills。`manifest.yaml` が唯一の正 |
| `kits/` | v3 の mixin kit（base、team） |
| `sets/` | workload と mixin を束ねる kit set |
| `env/` | メンバーの `~/.sbxenv.yaml` の元になる base の env |
| `ci/` | CI の方針・処理・AI レビューの指示文・テスト |
| `.github/` | ワークフロー、CODEOWNERS、Dependabot |

## サイクル

1. Issue（または Slack から）で skill の追加を依頼する
2. Claude が manifest と写しを更新した PR を作る
3. 週1回、外部 skills の上流を確かめ、更新があれば PR を作る
4. 検査を通り危険度が低ければ自動マージ、そうでなければ保留して Slack に通知する
5. main に入ると kit と kit set をビルドして GHCR に push、署名し、`stable` を動かす
6. 次に作る sandbox から新しい版が使われる

## 承認のルール

`.github/` と `ci/` を変える PR は、CODEOWNERS の承認が必要。`skills/`・`kits/`・`sets/` の変更は、検査を通れば自動でマージされる。

## 状態

- [ ] skills の manifest の項目
- [ ] 取り込みスクリプト
- [ ] 危険度の判定ルール
- [ ] kit（base、team）の記述子
- [ ] kit set（standard）
- [ ] ワークフローの中身
- [ ] Slack 通知
