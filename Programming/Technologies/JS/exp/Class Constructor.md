#js-exp 
# **Class yaratilishi**
```js
class Car {
  constructor(type, color) {
    this.type = type;
    this.color = color;
  }
}

const car = new Car('sedan', 'red');
console.log(car);
```
---
```js
// Declaration
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}

// Expression; the class is anonymous but assigned to a variable
const Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};

// Expression; the class has its own name
const Rectangle = class Rectangle2 {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
```

```js
class Car {
	constructor (props) {
		this.props = props;
	}
} 
```
---
-  Class ichida funciyalar ham yaratish mumkin va buning uchun bizga *const*, *let* kabi kalit so'zlar shart emas;
- *Constructor* bu propslarni saqlaydigan **obj**  
	```js
class Person {
	constructor(name, age) {
		this.name = name;
		this.age = age;
	}
	greeting() {
		return console.log(this.name, this.age);
	}
}
const firstPerson = new Person('Cyrex', 21);
firstPerson.greeting();
```
---
- Classdan nusxa olish uchun *extends* dan fodalalnamiz;
- *super* bu nusxani yuklovchi **metod**;
```js
 // Class yaratamiz
class Person {
	constructor(name, age) {
		this.name = name;
		this.age = age;
	}
	greeting() {
		return console.log(this.name, this.age);
	}
};

// Ikkinchi nusxa oladigan klass
class StatusPerson extends Person {
	// constructor ichiga o'zimizning qo'shimcha propslarni qo'shish mumkin
	constructor(name, age, isMarried) {
    // super ichiga nusxalanadigan propslarni beramiz
		super(name, age);
		this.isMarried = isMarried;
	}
	get() {
		return console.log(`${this.name} ${this.isMarried ? 'got' : 'was not'} married at the ${this.age}.`);
	};
};
const sudlanuvchi = new StatusPerson('Cyrex', 21, true);
sudlanuvchi.get();
```
---
## **Rest** operatori
- qachonki funkciyada *1chi va 2chi* **parametrlar** aniq va undan keyingilari noaniq bo'lsa biz ularni <span style="background:rgba(240, 107, 5, 0.2)">**...rest**</span> operatori orqali massivga o'rab olishimiz mumkin.
 ```js
 function calc(a, b, ...rest) {
  console.log(a + b);
  console.log(rest)
}
calc(1,2, 12,232,43,43,5,345,35,3,53,34);
```
Bizga *console* <font color="#ffff00">Array</font> qaytaradi.
```js
3
[ 12, 232, 43, 43, 5, 345, 35, 3, 53, 34 ] // ...rest
```
---
## Parametrga <font color="#9bbb59">default</font> qiymat berish:
- agar user parametrga qiymat kiritmasa unga default berib ketish mumkin.
```js
const calc = (a, b = 4) => {
	console.log(a + b); //ikkinchisi default b = 4
};
calc(2)
```
Console:
```js
6
```
yokida
<font color="#4f81bd">Codition</font> orqali ham qilsa bo'ladi:
```js
const calc = (a, ) => {
	b = b || 4 // yokida operatori orqali = || 
	console.log(a + b);
};
calc(2)
```