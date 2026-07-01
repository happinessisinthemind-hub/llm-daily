# Obsidian への取り込み方法

`obsidian/高齢者支援事業/` フォルダに、Obsidian向けに整形したノート一式があります。

## 取り込み手順（おすすめ）

### 方法A: フォルダをVaultにコピー

1. このリポジトリを pull（または PR #19 をマージ）
2. `obsidian/高齢者支援事業/` フォルダを、お使いの Obsidian Vault 内にコピー
3. Obsidian で `00-索引（MOC）.md` を開く

### 方法B: Obsidian Git プラグインを使っている場合

1. Vault と `llm-daily` リポジトリを連携済みなら、`obsidian/高齢者支援事業/` を Vault 内の任意の場所にシンボリックリンクまたはコピー
2. Git pull で同期

### 方法C: 個別ファイルをインポート

Obsidian の「ファイルを開く」で `obsidian/高齢者支援事業/` 内の `.md` を選択

---

## フォルダ構成

```
obsidian/高齢者支援事業/
├── 00-索引（MOC）.md          ← ここから辿る
├── 面談当日チートシート.md
└── 初月成果物/
    ├── 01-現場課題マップ.md
    ├── 02-施設ヒアリングシート.md
    ├── 03-サービス範囲表.md
    ├── 04-施設向け説明トーク.md
    └── 05-リスクチェックリスト.md
```

## Obsidian向けの整形内容

- YAML frontmatter（tags / created / aliases）
- ノート間の `[[ウィキリンク]]`
- MOC（Map of Content）索引ノート

## 元データ

`docs/elderly-support-service/` にも同内容の素のMarkdownがあります。Obsidian 以外で使う場合はそちらを参照してください。
