```dataview
TABLE date, file.link, "🎯 Основная цель" as Goal
FROM "remote-blog/Daily notes"
WHERE contains(file.tags, "daily")
SORT date DESC
```
