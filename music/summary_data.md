---
title: 音樂統計
tags: [music, summary]
created: 2022-12-25
---

```dataview
TABLE WITHOUT ID
  AllArtist
FROM "p.notes/music/song"
FLATTEN Artist AS AllArtist
GROUP BY AllArtist
```

```dataview
TABLE WITHOUT ID
  AllTags
FROM "p.notes/music/song"
FLATTEN Tags AS AllTags
GROUP BY AllTags
```
