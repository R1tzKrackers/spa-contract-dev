# 契約凍結

## ロール
{{DESIGN_ROLE}}（設計担当）

## 目的
SPA設計を凍結し、実装フェーズへの移行を宣言する。

## 凍結対象
- `{{SPA_SPEC_DIR}}/components.yml`
- `{{SPA_SPEC_DIR}}/state/`
- `{{SPA_SPEC_DIR}}/routing/`
- `{{SPA_SPEC_DIR}}/detail/`

## 凍結宣言
```
CONTRACT FROZEN

凍結日時: [日時]
凍結対象: {{SPA_SPEC_DIR}}/
凍結理由: 実装フェーズ開始のため

以降、{{IMPL_ROLE}} が実装を開始する。
設計変更が必要な場合は差し戻し手順に従うこと。
```

## 指示
凍結宣言を出力し、{{IMPL_ROLE}} に引き継げ。

---

## 履歴記録（必須）

フェーズ完了時、`.phase-manager-history.yml` に以下を追記せよ：

```yaml
- phase: "06-design-freeze"
  status: "complete"
  comment: "契約凍結完了"
  timestamp: 現在時刻を取得して記録
```
