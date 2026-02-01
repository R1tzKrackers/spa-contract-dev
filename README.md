# SPA Contract Framework

**SPA開発フレームワーク / SPA Development Framework**

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)]()
[![Phase Manager](https://img.shields.io/badge/requires-Phase%20Manager-green.svg)]()

---

## 概要 / Overview

SPA Contract Frameworkは、コンポーネント設計を起点としたSPA開発ワークフローを提供するフレームワークです。
コンポーネント設計から状態管理、実装までの一貫したフローを定義します。

*SPA Contract Framework provides a component-first development workflow for Single Page Applications.
It defines a consistent flow from component design to state management and implementation.*

---

## 特徴 / Features

- **コンポーネント駆動設計** - コンポーネント階層設計を起点とした開発フロー
  *Component-Driven Design - Development flow starting from component hierarchy design*

- **状態管理設計** - Store/Contextの明確な設計
  *State Management Design - Clear design of Store/Context*

- **契約凍結** - 設計凍結後の変更を防止
  *Contract Freeze - Prevents specification changes after design completion*

---

## ワークフロー / Workflow

```
[Setup]
  00c-project-config      プロジェクト設定 / Project Configuration
       |
[Design - Component]
  01-component-design     コンポーネント設計 / Component Design
  01r-component-review    コンポーネント設計レビュー / Component Review
       |
[Design - State]
  02-state-design         状態管理設計 / State Management Design
  02r-state-review        状態管理レビュー / State Review
  03-state-fix            状態管理修正（任意）/ State Fix (optional)
       |
[Design - Routing]
  03-routing-design       ルーティング設計 / Routing Design
       |
[Design - Detail]
  04-detail-design        詳細設計 / Detail Design
  04r-detail-review       詳細設計レビュー / Detail Review
       |
[Handoff]
  05-handoff-check        引継ぎ判定 / Handoff Check
  06-design-freeze        契約凍結 / Contract Freeze
       |
[Implementation]
  07-impl-start           実装開始 / Implementation Start
  08-impl-execute         実装 / Implementation Execute
  09-test-execute         テスト実装 / Test Execute
  10-impl-verify          実装検証 / Implementation Verification
  10r-impl-verify-review  実装検証レビュー / Implementation Review
  11-impl-complete        実装完了 / Implementation Complete
```

---

## ディレクトリ構成 / Directory Structure

```
spa-contract-dev/
├── framework.yml      # フレームワークマニフェスト / Framework manifest
├── prompts/           # フェーズ別プロンプト / Phase-specific prompts
├── templates/         # テンプレート / Templates
│   └── AGENTS.md.template
└── docs/              # ドキュメント / Documentation
    └── development-flow.md
```

---

## 使用方法 / Usage

### 前提条件 / Prerequisites

- [Phase Manager](https://github.com/R1tzKrackers/phase-manager) がインストール済みであること

### セットアップ / Setup

1. Phase Managerの初期化フェーズで本フレームワークを選択
2. `project-config.yml` でプロジェクト固有の設定を行う

---

## 変数 / Variables

| 変数 / Variable | 説明 / Description |
|-----------------|---------------------|
| `{{PROJECT_NAME}}` | プロジェクト名 / Project name |
| `{{DESIGN_ROLE}}` | 設計担当ロール名 / Design role name |
| `{{IMPL_ROLE}}` | 実装担当ロール名 / Implementation role name |
| `{{SPA_SPEC_DIR}}` | SPA仕様書ディレクトリ / SPA spec directory |
| `{{IMPL_DIR}}` | 実装ディレクトリ / Implementation directory |
| `{{TEST_DIR}}` | テストディレクトリ / Test directory |

---

## ライセンス / License

MIT License

---

## 関連 / Related

- [Phase Manager](https://github.com/R1tzKrackers/phase-manager) - ワークフロー管理ツール
