# OpenCode サブエージェント設定

`.opencode/agents/deepseek-flash.md` に、OpenCode Go 経由の **DeepSeek V4.1 Flash（推論レベル max）** をサブエージェントとして定義しています。

## セットアップ（初回のみ）
1. https://opencode.ai/zen にサインインし、Go プランを購読して API キーをコピーする。
2. リポジトリ直下で `opencode` を起動し、`/connect` → `OpenCode Go` を選んでキーを貼り付ける。
3. `/models` に `opencode-go/deepseek-v4.1-flash` が表示されれば準備完了。

## 使い方
- 手動で呼ぶ: プロンプト内で `@deepseek-flash` とメンションする。
  例: `@deepseek-flash src/components/AsciiHero.astro の回転速度を調整して`
- 自動で呼ばれる: primary エージェント（build / plan）が Task ツール経由で必要に応じて委譲する。

## 設定の要点
| 項目 | 値 | 意味 |
| --- | --- | --- |
| `model` | `opencode-go/deepseek-v4.1-flash` | OpenCode Go のモデル ID |
| `variant` | `max` | DeepSeek の reasoning effort（low / high / max）の最大 |
| `mode` | `subagent` | primary としては使わず、委譲・@メンション専用 |
| `steps` | `60` | 1 回の委譲で許可する最大ループ回数 |

推論レベルを下げたい場合は `variant` を `high` や `low` に変更してください。
