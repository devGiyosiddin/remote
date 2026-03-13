#plans-weekly 


Цель: За 7 дней по 15-20 минут в день изучить основы JavaScript-движков, чтобы понимать, как исполняется код, и писать максимально эффективные приложения.

---

## 🗓 День 1: Знакомство с движками

### Что учим:
- Что такое JS-движки
- Зачем нужен V8 и кто его использует (Chrome, Node.js)
- Разница между интерпретацией и компиляцией
- AST (Абстрактное синтаксическое дерево)

### Полезные ссылки:
- [Как работает V8 (официальный блог)](https://v8.dev/blog/tags/architecture)
- [Видео (3 мин): JS Engines — Fireship](https://www.youtube.com/watch?v=5nmpokoRaZI)

---

## 🗓 День 2: Event Loop — сердце асинхронности

### Что учим:
- Call Stack
- Event Loop
- Macrotask vs Microtask
- Почему `setTimeout(fn, 0)` не сразу

### Ссылки:
- [Tasks, microtasks и event loop — Jake Archibald](https://jakearchibald.com/2015/tasks-microtasks-queues-and-schedules/)
- [Видео: JS Event Loop (JSConf)](https://www.youtube.com/watch?v=8aGhZQkoFbQ)

---

## 🗓 День 3: JIT-компиляция

### Что учим:
- Что такое JIT (Just-in-Time)
- Baseline и Optimizing компиляция
- Hot path, inlining, speculative optimizations

### Ссылки:
- [Официальная документация V8](https://v8.dev/docs)
- [Видео: JIT Explained (Codesmith)](https://www.youtube.com/watch?v=QzA0skIP5pQ)

---

## 🗓 День 4: Оптимизация и деоптимизация

### Что учим:
- Почему `delete obj.key` может замедлять код
- Inline cache (ICs)
- Что вызывает деоптимизацию

### Примеры:
```js
function sum(a, b) {
  return a + b;
}
// ✅ хорошо оптимизируется

function sum(a, b) {
  return a + b + Math.random();
}
// ❌ не оптимизируется (из-за Math.random)
```

---

## 🗓 День 5: Garbage Collector (GC)

### Что учим:
- Mark-and-sweep алгоритм
- Что такое утечка памяти
- Когда помогает `null` и замыкания

### Ссылки:
- [Memory Management (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_Management)
- [Chrome DevTools: Memory](https://developer.chrome.com/docs/devtools/memory/)

---

## 🗓 День 6: Инструменты разработчика

### Что учим:
- Вкладки **Performance** и **Memory** в DevTools
- Метрики: `performance.mark()` / `performance.measure()`
- Как смотреть JIT в Node:
  ```bash
  node --trace-opt script.js
  node --trace-deopt script.js
  ```

---

## 🗓 День 7: Повторение и практика

### Что делаем:
- Пишем простую JIT-friendly функцию
- Пишем функцию с деоптимизацией
- Измеряем скорость через `console.time()` и `performance.mark()`

```js
console.time("fast");
for (let i = 0; i < 1000000; i++) {}
console.timeEnd("fast");
```

---

## 🎁 Бонус:
Если хочешь углубиться:
- [V8 Blog (англ)](https://v8.dev/blog)
- [WTF is the Event Loop — FunFunFunction (YouTube)](https://www.youtube.com/watch?v=8aGhZQkoFbQ)
- [JSConf.eu — разборы движков](https://www.youtube.com/c/JSConfEU)

---

**🔥 После этого плана ты сможешь говорить с движком на одном языке.  
Фронтенд без понимания движка — как меч без клинка. Но ты теперь с клинком.**