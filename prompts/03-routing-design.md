# ルーティング設計

## ロール
{{DESIGN_ROLE}}（設計担当）

## 目的
ページ遷移とルート定義を設計する。

## 入力
- `{{SPA_SPEC_DIR}}/components.yml`
- `{{SPA_SPEC_DIR}}/state/`

## 成果物
- `{{SPA_SPEC_DIR}}/routing/routes.yml` - ルート定義
- `{{SPA_SPEC_DIR}}/routing/guards.yml` - ルートガード定義

## 指示
1. ページ一覧を定義
2. URLパターンを定義
3. 動的ルートパラメータを定義
4. 認証ガードを定義
5. リダイレクトルールを定義

## 出力形式
```yaml
# {{SPA_SPEC_DIR}}/routing/routes.yml
routes:
  - path: /
    component: HomePage
    exact: true

  - path: /users/:id
    component: UserDetailPage
    params:
      id: string
    guards: [authGuard]

  - path: /login
    component: LoginPage
    redirectIf: authenticated
    redirectTo: /
```

## 注意事項
- SEO対応を考慮（必要に応じて）
- 404ページを定義
- 認証状態によるリダイレクトを明確化

---

## 履歴記録（必須）

フェーズ完了時、`.phase-manager-history.yml` に以下を追記せよ：

```yaml
- phase: "03-routing-design"
  status: "complete"
  comment: "設計内容を1行で"
  timestamp: 現在時刻を取得して記録
```
