#pr-exp
```js
const user = 'Sanjar';
if (user === `G'iyosiddin` || 'Jamshid' || 'Bobur') console.log('Access granted')
else console.log(`Access denied`);
```
Если каждое сase проверять так, то консоль выдает  эту:
```js
'Access granted'
```
Причина в том что выражение
```js
user === `G'iyosiddin` || 'Jamshid' || 'Bobur'
```
интерпретируется так:
```js
(user === `G'iyosiddin`) || Boolean('Jamshid') || Boolean('Bobur')
```
А строка `'Jamshid'` **всегда считается `true`**, потому что любая непустая строка в `if` — это true.

➡️ Поэтому `if` всегда будет `true`, **независимо от значения `user`**.

✅Если нужно проверить строки то сделает вот так:
```js
if (user === "G'iyosiddin" || user === 'Jamshid' || user === 'Bobur')
```
каждую строку проверяем к user отдельно

💠Альтернатив и лучшее решением будет обернуть все строки на массив
```js
const user = 'Sanjar';
if ([`G'iyosiddin`,'Jamshid','Bobur'].includes(user)) console.log('Access granted')
else console.log(`Access denied.`)
```
тогда наш консоль выдает нужный нам  ответ:
```js
'Access denied.
```

```chart
type: bar
labels: []
series:
  - title: 
    data: []
tension: 0.2
width: 80%
labelColors: false
fill: false
beginAtZero: false
bestFit: false
bestFitTitle: undefined
bestFitNumber: 0
```
