# コンポーネント設計

## ロール
{{DESIGN_ROLE}}（設計担当）

## 目的
UIコンポーネントの階層構造とPropsを設計する。

## 入力
- プロジェクト要件
- 画面モック（あれば）

## 成果物
- `{{SPA_SPEC_DIR}}/components.yml` - コンポーネント一覧
- `{{SPA_SPEC_DIR}}/components/` - 各コンポーネント仕様

## 指示
1. ページ構成を定義
2. コンポーネント階層を設計
3. 各コンポーネントのPropsを定義
4. コンポーネント間の依存関係を明記

## 出力形式
```yaml
# {{SPA_SPEC_DIR}}/components.yml
components:
  - name: Header
    type: layout
    props:
      - name: title
        type: string
        required: true
    children: [Navigation, UserMenu]

  - name: Navigation
    type: navigation
    props:
      - name: items
        type: NavItem[]
        required: true
```

## 注意事項
- Atomic Design原則を考慮
- 再利用性を重視
- Props型を明確に定義

---

## 履歴記録（必須）

フェーズ完了時、`.phase-manager-history.yml` に以下を追記せよ：

```yaml
- phase: "01-component-design"
  status: "complete"
  comment: "設計内容を1行で"
  timestamp: 現在時刻を取得して記録
```
