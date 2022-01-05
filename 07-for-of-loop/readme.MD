# How to use for .. of loop in ES6 ? #
- ES6 provides a new construct of <b> for...of </b> that creates a loop that iterate over iterable objects such as : <b> Array, String, Map, Set </b>

- <b> Syntax </b>

```js
for (variable of iterable) {
   // statements 
}
```

## 1. Iterating over array ##

```js

let scores = [80, 90, 70];

for (let score of scores) {
    score = score + 5;
    console.log(score);
}

 ------------- OUTPUT ----------
85
95
75

```

## 2. Iterating over string ##

```js

let str = 'abc';
for (let c of str) {
    console.log(c);
}


============ OUTPUT =============
a
b
c
```

## 3. Iterating over map objects ##

```js

let colors = new Map();

colors.set('red', '#ff0000');
colors.set('green', '#00ff00');
colors.set('blue', '#0000ff');

for (let color of colors) {
    console.log(color);
}

============= OUTPUT =============
[ 'red', '#ff0000' ]
[ 'green', '#00ff00' ]
[ 'blue', '#0000ff' ]

```

## 4. Iterating over set objects ##

```js

let nums = new Set([1, 2, 3]);

for (let num of nums) {
    console.log(num);
}

```

