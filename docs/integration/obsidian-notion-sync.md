# Obsidian × Notion 連携ガイド

高齢者支援事業の資料を **Obsidian（iCloud Vault）** と **Notion** の両方で使うための手順です。

## 全体像

```
GitHub llm-daily（正本）
    └── export/高齢者支援事業-まとめ一式.md   ← ★ Notion・Obsidian 共通（これ1つでOK）
    ├── obsidian/高齢者支援事業/   → 個別ノート版（ウィキリンク）
    └── notion/高齢者支援事業/     → ページ分割インポート用
```

| ツール | 向いている用途 |
|--------|----------------|
| **Obsidian** | 面談前の素早い参照、ウィキリンク、オフライン、iPhone/iPad |
| **Notion** | チーム共有、進捗管理、データベース化、Webからのアクセス |

---

## 1. Obsidian（iCloud Vault）

### 初回セットアップ

1. PR [#19](https://github.com/happinessisinthemind-hub/llm-daily/pull/19) をマージ後 `git pull`
2. Obsidian → **VaultをFinderで開く**
3. `llm-daily/obsidian/高齢者支援事業/` を Vault 内にコピー
4. `00-索引（MOC）` から辿る

### 更新時

```bash
cd ~/path/to/llm-daily && git pull
cp -R obsidian/高齢者支援事業/* \
  "$HOME/Library/Mobile Documents/iCloud~md~obsidian/Documents/<Vault名>/高齢者支援事業/"
```

### Obsidian で開くノート

- [[00-索引（MOC）]]
- [[事業設計整理書]]
- [[面談当日チートシート]]
- [[Notion連携]]

---

## 2. Notion

### 方法A: Markdownインポート（いまできる）

1. Notion で新規ページ **「高齢者支援事業」** を作成
2. ページ内で `···` → **Import** → **Markdown**
3. `notion/高齢者支援事業/` フォルダ内のファイルを順にインポート
   - まず `00-索引.md`
   - 次に `事業設計整理書.md`
   - 面談・初月成果物フォルダ

### 方法B: Cursor の Notion MCP（自動同期・要認証）

Cursor デスクトップで **Notion MCP を認証**すると、チャットから直接ページ作成が可能です。

1. Cursor → Settings → MCP → Notion → Connect
2. 認証後、「高齢者支援事業の資料をNotionに作成して」と依頼

> 現時点のクラウド環境では Notion 未認証のため、自動作成はできません。認証後に再依頼してください。

### Notion で推奨するページ構成

```
📁 高齢者支援事業（親ページ）
├── 📄 索引
├── 📄 事業設計整理書
├── 📄 面談当日チートシート
└── 📁 初月成果物
    ├── 現場課題マップ
    ├── 施設ヒアリングシート
    ├── サービス範囲表
    ├── 施設向け説明トーク
    └── リスクチェックリスト
```

### Notion データベース化（任意）

面談後の記録用に、以下のDBを追加すると便利です。

| DB名 | プロパティ例 |
|------|-------------|
| ヒアリング記録 | 日付、相手役職、Top3困りごと、紹介可否、メモ |
| リスクチェック | 項目、OK/要確認/NG、面談日、メモ |
| 資料一覧 | 資料名、状態（作成済/未作成）、優先度、リンク |

---

## 3. 両方を使い分ける例

| シーン | 使うツール |
|--------|-----------|
| 面談30分前の最終確認 | Obsidian `面談当日チートシート` |
| 事業者への提案の骨子 | Notion `事業設計整理書` を共有リンク |
| ヒアリング後のメモ | Notion DB に記録 → 必要なら Obsidian に要約 |
| 外出先・iPhone | Obsidian（iCloud同期） |

---

## 4. ファイル対応表

| 内容 | Obsidian | Notion |
|------|----------|--------|
| 索引 | `00-索引（MOC）.md` | `00-索引.md` |
| 事業設計 | `事業設計整理書.md` | `事業設計整理書.md` |
| 面談 | `面談当日チートシート.md` | `面談当日チートシート.md` |
| 初月成果物 | `初月成果物/*.md` | `初月成果物/*.md` |
| 連携説明 | `Notion連携.md` | 本ガイドをNotionにインポート |

---

## 5. 更新の流れ（おすすめ）

1. GitHub `llm-daily` で資料を更新（Cursor / Codex）
2. `git pull` 後、Obsidian フォルダを上書きコピー
3. Notion は差分があるページだけ再インポート、または MCP で更新

---

*正本: `docs/elderly-support-service/` および `obsidian/` / `notion/`*
