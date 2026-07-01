---
tags:
  - 高齢者支援
  - Notion連携
created: 2026-07-01
aliases:
  - Notion
---

# Notion 連携

Obsidian（iCloud Vault）と Notion の両方で同じ資料を使うためのメモです。

## 正本（GitHub）

- `llm-daily` リポジトリが正本
- Obsidian用: `obsidian/高齢者支援事業/`
- Notion用: `notion/高齢者支援事業/`

## Notion への入れ方

1. Notion でページ「高齢者支援事業」を作成
2. `···` → Import → Markdown
3. `notion/高齢者支援事業/` 内の `.md` をインポート

詳細はリポジトリ内 `docs/integration/obsidian-notion-sync.md` を参照。

## Cursor から自動で Notion に入れる

Cursor デスクトップで **Notion MCP を認証**すると、チャットから直接ページ作成可能。

> 未認証の間は、上記の Markdown インポートを使う。

## 使い分け

| Obsidian | Notion |
|----------|--------|
| 面談前の素早い参照 | 共有・提案の見せ方 |
| iPhone / iPad（iCloud） | Web・チーム |
| [[ウィキリンク]] | DB・進捗管理 |

## 関連ノート

- [[00-索引（MOC）]]
- [[事業設計整理書]]
- [[面談当日チートシート]]
