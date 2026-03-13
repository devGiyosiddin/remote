#js-exp #js 
# This - har doim nimagadir osiluvchi silka
## funckiya ichida this 
```js
function showThis() {
	console.log(this);
};
showThis();
```
bu yerda this hechnarsaga bog'lanmagani sababli avtomatik default ***<font color="#f79646">Windowga</font>*** bog'lanadi.
 Agar qat'iy rejim ishlasa, ya'ni 'use strict' bu holda this <font color="#8064a2">undefined</font> ga teng bo'ladi.

## Object ichida this
```js
const person = {
	name: 'cyrex',
	age; 32,
	greeeting: function () {
		console.log(this);
	}
};
```
obj ichida *this chaqirilsa alabatta u <font color="#f79646">Object</font> ni o'ziga teng bo'ladi

---
## **Obj** ichida *this function va metod orqali ishlatilishi
``
```js
const per = {
  name: 'salom',
  age: 34,
  salomlash: function() {
    function showThis() {
      console.log(this);
    };
    showThis();
    console.log(this);
  },
};
per.salomlash();
```
bu yerda birinchi <font color="#4bacc6">showThis</font> function ichidagi <font color="#938953">this</font> Windowga osiladi
ikkinchisi uni ichidagi metod kabi kelgani uchun <font color="#ffff00">Obj</font> ni o'ziga osiladi.

agar bu yerda <font color="#4bacc6">showThis</font> funckciyasi <font color="#95b3d7">Arrow</font> function bo'lganda:
``
```js
const showThis = () => {
	console.log(this);
};
```
bu xolatda arrow funciton o'zidan tepadagi <font color="#ffff00">obj</font> ga osiladi.

###
Hulosa:
- <font color="#9bbb59">Context this</font> hardoim <font color="#ffff00">obj</font> ga osiladi u bo'lmasa windowga 'use strict' bo'lsa undefined bo'ladi.
- 

slaom sardorbekkdslajfkjafadslkjlkj\
cosnole.lgo(salom').

1999
2004

sajdfklaskjks dflkjas
dlfajlkj lfdkjsa


+6 SOAT
backend 6 oy 3 dim qiyin  2yil
frontend 9 oy 5 oy dim oson
html css js react  angular vuse types.cript  3 yil 