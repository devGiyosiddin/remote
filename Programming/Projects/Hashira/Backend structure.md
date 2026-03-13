###### {{title_original}}  
> *{{title_english}}*

![Banner]({{banner_url}})

---

## 🎬 Основная информация
- **Тип**: {{type}}  
- **Статус**: {{status}}  
- **Год выпуска**: {{year}}  
- **Сезон**: {{season}}  
- **Эпизодов**: {{episodes}}  
- **Длительность серии**: {{duration}}

---

## 📖 Синопсис

**Кратко**:  
> {{short_synopsis}}

**Полный сюжет**:  
{{synopsis}}

---

## 💮 Жанры и Студии
- **Жанры**: `{{genres.join(", ")}}`  
- **Студии**: `{{studios.join(", ")}}`

---

## 📊 Рейтинги
- ⭐ **Оценка**: {{score}}  
- 🏅 **Ранг**: #{{rank}}  
- 🔥 **Популярность**: {{popularity}}

---

## 🕰️ Время выхода
- **Начало показа**: {{aired_from}}  
- **Конец показа**: {{aired_to || "—"}}

---

## 🖼️ Медиа
![Poster]({{poster_url}})

- 🎞️ [Смотреть трейлер]({{trailer_url}})

---

## 🌐 Статистика
- 👁️ Просмотров: {{views_count}}  
- 💬 Комментариев: {{comments_count}}

---

## 🔗 Дополнительно
- **Slug**: `{{slug}}`  
- 🧩 **ID**: {{id}}  
- 🧷 **Избранное**: {{is_featured ? "Да" : "Нет"}}  
- 🚩 **Опубликовано**: {{is_published ? "Да" : "Нет"}}  
- 🕓 Создано: {{created_at}}  
- ✏️ Обновлено: {{updated_at}}

---

## 🧭 Связанные тайтлы
{{related_anime.map(a => `- [${a.title}](/anime/${a.slug})`).join("\n")}}

---

## 🌍 Переводы
{{translations.map(lang => `- ${lang.code}: ${lang.title}`).join("\n")}}

---

## 🏷️ Теги
- Тип: `{{movie || serie}}`  
- Возрастной рейтинг: {{yosh_chegarasi}}+  
- Дата начала: {{chiqqan}}  
- Дата завершения: {{tugagan || "—"}}  
- Жанры: {{janr.join(", ")}}
- Японское название: {{yaponcha_nomi}}