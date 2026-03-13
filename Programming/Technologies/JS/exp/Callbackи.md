#js-exp 
# Callback в JavaScript — простое объяснение

**Callback** — это функция, которую передают в другую функцию как аргумент, чтобы вызвать позже. Это удобно, когда нужно выполнить действие после завершения другого (например, загрузки данных).

## 📦 Пример:

```js
function sayHi(name) {
  console.log("Привет, " + name);
}

function doSomething(callback) {
  console.log("Сначала делаем что-то...");
  callback("Giyu");
}

doSomething(sayHi);
```

## 🧠 Зачем нужны callbacks?

- Для асинхронности (таймеры, запросы).
    
- Для порядка действий.
    
- Чтобы передать пользовательскую логику.
---
🧟 Проблема: callback hell`
`
```js
login(user, () => {
  getProfile(user, () => {
    loadFeed(user, () => {
      showComments(user);
    });
  });
});
```

Поэтому появились:
- `Promise`    
- `async/await`

---
> Callback — это “позвони мне позже”, Promise — “обещаю перезвонить”, а `async/await` — “тебе просто нужно дождаться, когда я освобожусь” 😄