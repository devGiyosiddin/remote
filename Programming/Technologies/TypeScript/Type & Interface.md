
| Характеристика                                  | `interface`                               | `type`                                          |
| ----------------------------------------------- | ----------------------------------------- | ----------------------------------------------- |
| Расширение                                      | Да (`extends`)                            | Да (через `&`)                                  |
| Объединение                                     | Да (декларативное слияние)                | Нет                                             |
| Использование с примитивами                     | ❌                                         | ✅                                               |
| Использование с функциями, union, tuples и т.п. | Ограничено                                | ✅                                               |
| Предназначение                                  | Описание **структуры объектов и классов** | Описание **всего, включая типы, алиасы, union** |
## 💠 Примеры

### 1. Общее использование — практически идентичны:
```ts
interface Anime {
  title: string;
  episodes: number;
}

type Manga = {
  title: string;
  chapters: number;
}

```
### 2. Расширение (наследование || meros)

**interface:**
```ts
interface Anime {
  title: string;
}

interface ExtendedAnime extends Anime {
  episodes: number;
}

```
type:
```ts
type Anime = {
  title: string;
};

type ExtendedAnime = Anime & {
  episodes: number;
};
```
👉 Оба работают, но `interface` читается более декларативно.

### 3. Union / Tuple / Примитивы — тут побеждает `type`:
```ts
type Status = "ongoing" | "finished" | "upcoming";
type Pair = [number, string];
type UserId = string | number;
```
⚠️ `interface` не может описывать union или примитивные типы.
### 4. Declaration merging — фишка `interface`
```ts
interface User {
  name: string;
}

interface User {
  age: number;
}

// В итоге: User = { name: string; age: number }
```
✅ Это полезно для расширения внешних библиотек и API.
❌ С `type` такое не сработает — будет ошибка.

#### 🤖 Когда использовать?
| Когда...                                  | Используй                                          |
| ----------------------------------------- | -------------------------------------------------- |
| Описываешь структуру объекта, класса, API | `interface`                                        |
| Нужны union, tuple, алиасы                | `type`                                             |
| Работаешь с React props                   | Лично дело вкуса: и `interface`, и `type` работают |
#### **🧘 Итог:**
> **`interface` — это для структур.**  
> **`type` — это для всего.**

Но помни: **в 90% случаев ты можешь выбрать любой**, особенно если не используешь declaration merging.