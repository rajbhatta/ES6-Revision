# 3. Working with spread operator #
- ES6 provides a new operator called spread operator that consists of three dots (...). The spread operator allows you to spread out elements of an iterable object such as an array,a  map, or a set.

```js
const odd = [1,3,5];
const combined = [2,4,6, ...odd];
console.log(combined);
```

# 4. Copying array in ES6 #
```js
let scores = [80, 70, 90];
let copiedScores = [...scores];
console.log(copiedScores); 
```

## Spread operator for object continue 1 ##
- ES6 has added spread property to object literals in javascript. The spread operator (…) with objects is used to create copies of existing objects with new or updated values or to make a copy of an object with more properties. Let’s take at an example of how to use the spread operator on an object,

```js
const user1 = {
    name: 'Jen',
    age: 22
};
  
const clonedUser = { ...user1 };
console.log(clonedUser);
```

## Spread operator operation continue 2 ##
```js
const circle = {
    radius: 10
};

const coloredCircle = {
    ...circle,
    color: 'black'
};

console.log(coloredCircle);


======= OUTPUT ======
{
    radius: 10,
    color: 'black'
}
```

## Spread operator operation continue 3 (clone object) ##
```js
const circle = {
    radius: 10,
    style: {
        color: 'blue'
    }
};

const clonedCircle = {
    ...circle
};


clonedCircle.style = 'red';

console.log(clonedCircle);

============ OUTPUT ============
{ radius: 10, style: 'red' }
```

## Spread opreator operation continue 4  (merging) ##
```js

const circle = {
    radius: 10
};

const style = {
    backgroundColor: 'red'
};

const solidCircle = {
    ...circle,
    ...style
};

console.log(solidCircle);

===== OUTPUT =====
{ radius: 10, backgroundColor: 'red' }
```



# Reference #
- http://www.javascripttutorial.net/es6/javascript-spread/