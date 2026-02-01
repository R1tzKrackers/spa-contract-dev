# 実装

## ロール
{{IMPL_ROLE}}（実装担当）

## 目的
SPA仕様に基づいてコンポーネント・状態管理を実装する。

## 入力
- `{{SPA_SPEC_DIR}}/components.yml`
- `{{SPA_SPEC_DIR}}/state/`
- `{{SPA_SPEC_DIR}}/routing/`
- `{{SPA_SPEC_DIR}}/detail/`

## 成果物
- `{{IMPL_DIR}}/components/` - UIコンポーネント
- `{{IMPL_DIR}}/store/` - 状態管理
- `{{IMPL_DIR}}/routes/` - ルーティング
- `{{IMPL_DIR}}/hooks/` - カスタムフック

## 指示
1. 共通コンポーネントを実装
2. ページコンポーネントを実装
3. 状態管理（Store/Context）を実装
4. ルーティングを実装
5. API連携を実装
6. エラーハンドリングを実装

## 注意事項
- 仕様書に記載のない機能を追加しない
- 仕様と実装の乖離を発見した場合は `STOP: SPEC ISSUE FOUND` を報告

---

## 履歴記録（必須）

フェーズ完了時、`.phase-manager-history.yml` に以下を追記せよ：

```yaml
- phase: "08-impl-execute"
  status: "complete"
  comment: "実装内容を1行で"
  timestamp: 現在時刻を取得して記録
```
