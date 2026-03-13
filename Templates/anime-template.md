<%*
const title = await tp.system.prompt("Название аниме:");
const episodes = await tp.system.prompt("Количество серий:");
const genre = await tp.system.prompt("Жанр:");
-%>
---
title: <% title %>
episodes: <% episodes %>
genre: <% genre %>
rating: 
status: to_watch
author:
tags:
source:
year:
created: <% tp.date.now() %>
---

# <% title %>

> 

---
## Описание


---
## Скриншоты/Арт
