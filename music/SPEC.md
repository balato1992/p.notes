# 音樂筆記規範

本規範定義音樂筆記的組織方式和元數據標準。

## 目錄結構

```
music/
├── SPEC.md              # 本規範文件
├── _inbox.md            # 收集箱：待整理的音樂連結
├── _pure_music.md       # 純音樂分類
├── summary.md           # Dataview 歌曲列表表格
├── summary_data.md      # Dataview 統計查詢
└── song/                # 歌曲檔案目錄
```

## Frontmatter 欄位

| 欄位 | 說明 | 範例 |
|------|------|------|
| `title` | 歌曲名稱 | `Lemon` |
| `artist` | 藝人名稱（支援多藝人） | `米津玄師` |
| `url` | YouTube 連結 | `https://www.youtube.com/watch?v=...` |
| `language` | 語言 | `中文`, `日文`, `英文`, `粵語` |
| `tags` | 標籤陣列 | `[music, song, anime]` |
| `rank` | 等級 | `T1`, `T2` |
| `remark` | 備註（動畫名稱等） | `NARUTO疾風伝` |
| `created` | 建立日期 | `2022-12-25` |

### Frontmatter 範例

```yaml
---
title: Lemon
artist: 米津玄師
url: https://www.youtube.com/watch?v=SX_ViT4Ra7k
language: 日文
tags: [music, song]
rank: T1
remark: 
created: 2022-12-25
---
```

## 分類標籤

### 歌曲類型標籤
| 標籤 | 說明 |
|------|------|
| `#anime` | 動畫歌曲 |
| `#old` | 老歌 |
| `#pure-music` | 純音樂 |
| `#sad` | 悲傷風格 |
| `#romantic` | 情歌 |
| `#inspirational` | 勵志歌曲 |

### 語言標籤
| 標籤 | 說明 |
|------|------|
| `#chinese` | 中文 |
| `#japanese` | 日文 |
| `#english` | 英文 |
| `#cantonese` | 粵語 |

## 檔案命名規範

檔案名稱格式：`藝人名 - 歌曲名.md`

範例：
- `米津玄師 - Lemon.md`
- `葉蒨文 - 瀟灑走一回.md`

## 等級說明

| 等級 | 說明 |
|------|------|
| `T1` | 最高推薦 |
| `T2` | 次級推薦 |

## 特殊檔案

- `_inbox.md`：收集箱，用於臨時存放未整理的音樂連結
- `_pure_music.md`：純音樂收藏，按風格分類（#Troll, #Sad 等）
- `summary.md`：Dataview 表格，快速瀏覽所有歌曲
- `summary_data.md`：Dataview 統計，藝術家和標籤分布

## Dataview 查詢

Dataview 可直接查詢 frontmatter 欄位，欄位名稱需使用大寫開頭：
- `title` → `Title`
- `artist` → `Artist`
- `url` → `Url`
- `language` → `Language`
- `tags` → `Tags`
- `rank` → `Rank`
- `remark` → `Remark`
