# 詳細設計

## ロール
{{DESIGN_ROLE}}（設計担当）

## 目的
コンポーネントの詳細仕様とデータフローを設計する。

## 入力
- `{{SPA_SPEC_DIR}}/components.yml`
- `{{SPA_SPEC_DIR}}/state/`
- `{{SPA_SPEC_DIR}}/routing/`

## 成果物
- `{{SPA_SPEC_DIR}}/detail/` - コンポーネント詳細仕様
- `{{SPA_SPEC_DIR}}/detail/data-flow.yml` - データフロー図
- `{{SPA_SPEC_DIR}}/detail/api-integration.yml` - API連携仕様

## 指示
1. 各コンポーネントの詳細動作を定義
2. イベントハンドラを定義
3. API呼び出しタイミングを定義
4. エラーハンドリングを定義
5. ローディング状態を定義

## 詳細項目
| カテゴリ | 内容 |
|----------|------|
| コンポーネント動作 | ユーザー操作に対する反応 |
| データフロー | Props/State/Contextの流れ |
| API連携 | エンドポイント、リクエスト/レスポンス |
| エラー処理 | エラー時のUI表示 |
| ローディング | 非同期処理中のUI |

---

## 履歴記録（必須）

フェーズ完了時、`.phase-manager-history.yml` に以下を追記せよ：

```yaml
- phase: "04-detail-design"
  status: "complete"
  comment: "設計内容を1行で"
  timestamp: 現在時刻を取得して記録
```
