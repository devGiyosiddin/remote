#fr #fr-utils
# 🗂️ Z-Index System — Anime Portal

> [!NOTE] О системе Единая шкала z-index для всего проекта. Никаких `z-index: 9999` вслепую — только осознанная иерархия слоёв.

---

## 🧱 Полная таблица слоёв

|Переменная|Значение|Назначение|
|---|---|---|
|`--z-base`|`0`|Обычный контент страницы|
|`--z-content`|`1`|Карточки аниме|
|`--z-card-hover`|`5`|Карточка при `:hover`|
|`--z-sticky-card`|`10`|Прикреплённые элементы внутри секций|
|`--z-header`|`30`|Fixed header|
|`--z-header-dropdown`|`32`|Выпадающее меню навигации|
|`--z-header-btn`|`33`|Кнопки в header (Login, Search)|
|`--z-overlay`|`35`|Затемнение фона|
|`--z-sidebar`|`38`|Боковое меню (мобилка)|
|`--z-drawer`|`38`|Side panel / drawer|
|`--z-modal`|`40`|Модальное окно (аниме-карточка, трейлер)|
|`--z-modal-close`|`42`|Кнопка закрытия модала|
|`--z-lightbox`|`45`|Просмотр постера во весь экран|
|`--z-tooltip`|`50`|Подсказки|
|`--z-popover`|`50`|Popover (теги, жанры)|
|`--z-dropdown`|`52`|Dropdown select (сортировка, фильтры)|
|`--z-toast`|`60`|Toast-уведомления|
|`--z-snackbar`|`60`|Snackbar|
|`--z-loading`|`70`|Loading screen / скелетон поверх всего|
|`--z-cookie-banner`|`75`|Cookie / возрастное предупреждение|
|`--z-spotlight`|`80`|Spotlight-поиск (Cmd+K)|
|`--z-critical`|`90`|Критические системные сообщения|

---

## 🗃️ CSS переменные

```css
/* ================================
   Z-INDEX СИСТЕМА — ANIME PORTAL
   ================================ */

:root {
  /* BASE CONTENT */
  --z-base:            0;
  --z-content:         1;
  --z-card-hover:      5;
  --z-sticky-card:     10;

  /* NAVIGATION & HEADER */
  --z-header:          30;
  --z-header-dropdown: 32;
  --z-header-btn:      33;

  /* OVERLAYS */
  --z-overlay:         35;
  --z-sidebar:         38;
  --z-drawer:          38;

  /* MODALS & POPUPS */
  --z-modal:           40;
  --z-modal-close:     42;
  --z-lightbox:        45;

  /* FLOATING UI */
  --z-tooltip:         50;
  --z-popover:         50;
  --z-dropdown:        52;

  /* NOTIFICATIONS */
  --z-toast:           60;
  --z-snackbar:        60;

  /* TOP LEVEL */
  --z-loading:         70;
  --z-cookie-banner:   75;
  --z-spotlight:       80;
  --z-critical:        90;
}
```

---

## 📐 Диапазоны и логика

```
  0 – 10  ░░░░░░░░  Контент страницы
 30 – 33  ████░░░░  Навигация / Header
 35 – 38  █████░░░  Оверлеи и Drawer
 40 – 45  ██████░░  Модалки и Лайтбоксы
 50 – 52  ███████░  Floating UI
     60   ███████░  Уведомления
 70 – 90  ████████  Системный уровень
```

> [!IMPORTANT] Главное правило **Оверлей всегда ниже того, что он перекрывает.** Пример: `overlay 35` → `modal 40` → `modal-close 42` Так кнопка закрытия всегда кликабельна.

---

## ⚡ Примеры использования

```css
.header          { z-index: var(--z-header); }
.nav-dropdown    { z-index: var(--z-header-dropdown); }
.header-btn      { z-index: var(--z-header-btn); }

.overlay         { z-index: var(--z-overlay); }
.mobile-sidebar  { z-index: var(--z-sidebar); }

.anime-modal     { z-index: var(--z-modal); }
.modal-close-btn { z-index: var(--z-modal-close); }
.poster-lightbox { z-index: var(--z-lightbox); }

.genre-tooltip   { z-index: var(--z-tooltip); }
.filter-dropdown { z-index: var(--z-dropdown); }

.toast-message   { z-index: var(--z-toast); }
.search-spotlight{ z-index: var(--z-spotlight); }
```

---

## 🚫 Анти-паттерны

> [!WARNING] Никогда не делать так
> 
> ```css
> /* ❌ Плохо */
> z-index: 9999;
> z-index: 99999;
> z-index: 999999;
> 
> /* ✅ Хорошо */
> z-index: var(--z-modal);
> ```

---

## 🔗 Связанные заметки

- [[CSS Variables]]
- [[Header Component]]
- [[Modal System]]
- [[Overlay Logic]]

---

_Последнее обновление: {{date}}_ _Проект: Anime Portal_