# 実装完了

## ロール
{{IMPL_ROLE}}（実装担当）

## 目的
実装の完了を宣言する。

## 完了条件
- 全コンポーネントが実装済み
- 状態管理が実装済み
- ルーティングが実装済み
- 全テストがパス

## 完了宣言
```
IMPLEMENTATION COMPLETE

完了日時: [日時]
実装範囲: {{IMPL_DIR}}/
テスト: {{TEST_DIR}}/

本実装は {{SPA_SPEC_DIR}}/ の仕様に準拠しています。
```

---

## 履歴記録（必須）

フェーズ完了時、`.phase-manager-history.yml` に以下を追記せよ：

```yaml
- phase: "11-impl-complete"
  status: "complete"
  comment: "実装完了"
  timestamp: 現在時刻を取得して記録
```
