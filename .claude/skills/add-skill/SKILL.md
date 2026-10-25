---
name: add-skill
description: このリポジトリに skill を追加・更新するときの手順。Issue や Slack から skill の追加を頼まれたときに使う。
---

# add-skill

手順はこれから詰める。想定している流れ:

1. 外部の skill なら、`skills/external/<取得元>/<名前>/` に `skill.yaml` を作り、取り込みスクリプトで写しと `skill.lock.yaml` を作る
2. 自作の skill なら、`skills/internal/t3rm-<名前>/` に `SKILL.md` と `skill.yaml` を作る
3. 1つの PR では1つの skill だけを扱う
4. PR を作る（`.github/` と `ci/` には触れない）
