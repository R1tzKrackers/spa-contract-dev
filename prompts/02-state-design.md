# 状態管理設計

## ロール
{{DESIGN_ROLE}}（設計担当）

## 目的
アプリケーション状態の管理方式とデータフローを設計する。

## 入力
- `{{SPA_SPEC_DIR}}/components.yml`

## 成果物
- `{{SPA_SPEC_DIR}}/state/store.yml` - Store構造定義
- `{{SPA_SPEC_DIR}}/state/actions.yml` - アクション定義
- `{{SPA_SPEC_DIR}}/state/selectors.yml` - セレクタ定義

## 指示
1. グローバル状態とローカル状態を分離
2. Store構造（スライス）を定義
3. アクション・リデューサを定義
4. セレクタを定義
5. 非同期処理フローを定義

## 出力形式
```yaml
# {{SPA_SPEC_DIR}}/state/store.yml
store:
  slices:
    - name: auth
      state:
        user: User | null
        isLoading: boolean
        error: string | null

    - name: ui
      state:
        sidebarOpen: boolean
        theme: 'light' | 'dark'
```

## 注意事項
- 状態の正規化を検討
- 不要なグローバル状態を避ける
- 派生状態はセレクタで計算

---

## 履歴記録（必須）

フェーズ完了時、`.phase-manager-history.yml` に以下を追記せよ：

```yaml
- phase: "02-state-design"
  status: "complete"
  comment: "設計内容を1行で"
  timestamp: 現在時刻を取得して記録
```
