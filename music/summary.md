---
title: 音樂列表
tags: [music, summary]
created: 2022-12-25
---

```dataview  
TABLE WITHOUT ID
  link(file.link, title) as Title,
  Artist, link(Url, "Link") as Link, Language, SongTag, Rank, Remark
FROM "p.notes/music/song"
```
