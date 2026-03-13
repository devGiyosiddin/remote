##Mutabel va immutabel yangilanish
```js
{
  "counters": {
    "first": {
      "counter": 10,
      "startAt": "2024-25-05"
    },
    "second": {
      "counter": 12,
      "startAt": "2024-25-05"
    }
  },
  "someAnotherValue": {
    "field": "string"
  }
}
```
bu yerrdagi secondni ichidagi counterni o'zgartirish uchun 2 xil yo'l bor.

Mutabel shunchaki:
```js
state.counters.second.counter ++
```

Immutabelda esa yangi obj yaratib uni ichidagi o'zgargan qismini yangilaymiz
```js
{
  ...state,
  "counters": {
    ...state.counters,
    "second": {
      ...state.counters.second,
      counter: state.counters.second.counter + 1
    }
  }
}
```
---

Immutabel yangilanishni islatish zarur emas lekin 3 vaqtda qo'l keladi.
	- Ma'lumotlar o'zgarmasligiga kafolat
		- O'zgarishlar tarixini yaratib kuzatib borish mumkin
	- Toza funkciyalar
	- Redux optimizatsiya uchun shu yo'ldan foydalandi.

Qo'shimcha:
[[Redux toolkit]]
