# kits

v3 の mixin kit を置く。各 kit は記述子（YAML）と Dockerfile の組でできている。skills の同梱設定は `skills/manifest.yaml` から生成するので、ここに手で書かない。

| kit | 中身 |
|---|---|
| `base/` | 全環境で使う skills、共通の指示文、許可するドメイン |
| `team/` | ロール定義、権限の設定、引き継ぎ（`.agent-handoff/`）の規約 |
