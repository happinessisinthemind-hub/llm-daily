# Notion への取り込み方法

`notion/高齢者支援事業/` に、Notion向けに整形したMarkdownがあります（ウィキリンクなし・インポート向け）。

## 手順

1. Notion で親ページ **「高齢者支援事業」** を新規作成
2. ページ右上 `···` → **Import** → **Markdown & CSV** → **Markdown**
3. 以下の順でインポート（またはフォルダごと）

```
notion/高齢者支援事業/
├── 00-索引.md
├── 事業設計整理書.md
├── 面談当日チートシート.md
└── 初月成果物/
    ├── 01-現場課題マップ.md
    ├── 02-施設ヒアリングシート.md
    ├── 03-サービス範囲表.md
    ├── 04-施設向け説明トーク.md
    └── 05-リスクチェックリスト.md
```

4. 子ページとして整理し、索引からリンクを貼る

## Cursor Notion MCP で自動作成する場合

1. Cursor デスクトップ → Settings → MCP → **Notion** → Connect（認証）
2. チャットで「`notion/高齢者支援事業` の内容をNotionにページ作成して」と依頼

## Obsidian との関係

- **Obsidian** = iCloud Vault に `obsidian/高齢者支援事業/` をコピー（ウィキリンクあり）
- **Notion** = 本フォルダをインポート（共有・DB向け）
- 詳細: `docs/integration/obsidian-notion-sync.md`
