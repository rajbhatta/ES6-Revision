# How to perform array destructing in ES6 ? #
- It allows you to destructure an array into individual variables.

- <b> Regular way: </b>
```js

function getScores() {
   return [70, 80, 90, 100];
}

let [x, y, z] = getScores();

console.log(x); // 70
console.log(y); // 80
console.log(z); // 90

```

- <b> With array destructing: </b>

```js
function getScores() {
   return [70, 80, 90, 100];
}

let [x, y ,...args] = getScores();
console.log(x); // 70
console.log(y); // 80
console.log(args); // [90, 100]

```

- <b> Array destructing continue: </b>

```js

let a, b;
[a, b] = [10, 20];
console.log(a); // 10
console.log(b); // 20

```

## Example of nested array destructing ##
```js

function getProfile() {
    return [
        'John',
        'Doe',
        ['Red', 'Green', 'Blue']
    ];
}

let [
    firstName,
    lastName,
    [
        color1,
        color2,
        color3
    ]
] = getProfile();

console.log(color1, color2, color3); // Red Green Blue