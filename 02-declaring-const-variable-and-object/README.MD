# 02: Declaring constant in ES6 #
- ES6 provides a new way of declaring a constant by using const keyword. The const keyword creates a read only reference to a value.


```js
const CONSTANT_NAME = value;
```

- Constant keyword is also blocked-scoped variables.
- We can not reassign the constant variable once defined.

## 2.1 constant for object in JavaScript ##
- The const keyword ensures that the variable it creates is read-only. However, it doesn’t mean that the actual value to which the const variable reference is immutable. For example:

```js
const person = { age: 20 };
person.age = 30; // OK
console.log(person.age); // 30
```

- Even though the person variable is a constant, you can change the value of its property.

- However, you cannot reassign a different value to the person constant like this:

```js
person = { age: 40 }; // TypeError
```

- If you want the value of the person object to be immutable, you have to freeze it by using the Object.freeze() method:

```js
const person = Object.freeze({age: 20});
person.age = 30; // TypeError
```

## Const for Arrays ##
- we declare an array colors that has one element using the const keyword. Then, we can change the array’s elements by adding the green color. 

- However, we cannot reassign the array colors to another array.

```js
const colors = ['red'];
colors.push('green');
console.log(colors); // ["red", "green"]

colors.pop();
colors.pop();
console.log(colors); // []

colors = []; // TypeError
```

## Const for for loop ##
- ES6 provides a new construct called that allows you to create a loop iterating over iterable objects such as arrays, maps and sets.
```js
for ... of 
```


```js
let scores = [75, 80, 95];

for (let score of scores) {
	console.log(score);
}
```

- If you don’t intend to modify the score variable inside the loop, you can use the const keyword instead.

```js
let scores = [75, 80, 95];
for (const score of scores) {
    console.log(score);
}
```

### const work in traditional loop ###

- Notice that the const will not work in an imperative for loop. Trying to use the const keyword to declare a variable in the imperative for loop will result in a TypeError:

```js
for (const i = 0; i < scores.length; i++) { // TypeError
    console.log(scores[i]);
}
```