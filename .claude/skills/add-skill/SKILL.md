---
name: add-skill
description: このリポジトリに skill を追加・更新するときの手順。Issue や Slack から skill の追加を頼まれたときに使う。
---

# add-skill

手順はこれから詰める。想定している流れ:

1. `skills/manifest.yaml` に1行足す
2. 外部の skill なら、取り込みスクリプトで `skills/external/` に写しを作る
3. 自作の skill なら、`skills/internal/<名前>/SKILL.md` を作る
4. PR を作る（`.github/` と `ci/` には触れない）
