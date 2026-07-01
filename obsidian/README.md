# Obsidian への取り込み方法

`obsidian/高齢者支援事業/` フォルダに、Obsidian向けに整形したノート一式があります。

## iCloud にある Vault へ入れる（Mac・いちばん簡単）

このクラウド環境から iCloud 上の Vault には直接書き込めないため、Mac 側で次の操作をしてください。

### 手順

1. **GitHub から取得**
   - PR [#19](https://github.com/happinessisinthemind-hub/llm-daily/pull/19) をマージ後、ローカルで `git pull`
   - または GitHub の `obsidian/高齢者支援事業/` を ZIP でダウンロード

2. **iCloud 上の Vault を Finder で開く**
   - 一般的なパス:
     ```
     ~/Library/Mobile Documents/iCloud~md~obsidian/Documents/<Vault名>/
     ```
   - Finder で `移動` → `フォルダへ移動…`（⌘⇧G）に上記を貼り付けて Enter
   - または Obsidian の `Vault をFinderで開く` を使う

3. **フォルダをコピー**
   - `llm-daily/obsidian/高齢者支援事業/` を、Vault 内の好きな場所へドラッグ＆ドロップ
   - 例: `<Vault名>/仕事/高齢者支援事業/`

4. **Obsidian で確認**
   - iCloud 同期後、Obsidian で `00-索引（MOC）` を開く
   - リンクがつながっていれば OK

### ターミナルでコピーする場合（Vault名を置き換え）

```bash
VAULT_NAME="あなたのVault名"
cp -R ~/path/to/llm-daily/obsidian/高齢者支援事業 \
  "$HOME/Library/Mobile Documents/iCloud~md~obsidian/Documents/$VAULT_NAME/"
```

---

## その他の取り込み手順

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
├── 事業設計整理書.md          ← 市場調査・事業設計（15項目）
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

`docs/elderly-support-service/` にも同内容の素のMarkdownがあります。

## Notion 連携

- Notion用エクスポート: `notion/高齢者支援事業/`（Markdownインポート向け）
- 統合ガイド: `docs/integration/obsidian-notion-sync.md`
- Obsidian内メモ: [[Notion連携]]
