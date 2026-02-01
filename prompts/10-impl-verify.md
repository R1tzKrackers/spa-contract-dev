# 実装検証

## ロール
{{IMPL_ROLE}}（実装担当）

## 目的
実装がSPA仕様に準拠しているか検証する。

## 入力
- `{{SPA_SPEC_DIR}}/`
- `{{IMPL_DIR}}/`
- `{{TEST_DIR}}/`

## 検証項目
1. 全コンポーネントが実装されているか
2. 状態管理が仕様通りか
3. ルーティングが正しく動作するか
4. テストがパスしているか
5. UIが仕様に準拠しているか

## 成果物
- 検証レポート

---

## 履歴記録（必須）

フェーズ完了時、`.phase-manager-history.yml` に以下を追記せよ：

```yaml
- phase: "10-impl-verify"
  status: "complete"
  comment: "検証結果を1行で"
  timestamp: 現在時刻を取得して記録
```
