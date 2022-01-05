# When to use <b> ...for...in </b> loop? #
- ....for .. in loop is used for enumerating the enumerable properties of an object in JavaScript
- Object is a key valur pair in JavaScript
- <b> Sytanx </b>

```js

const person = {
    firstName: 'John',
    lastName: 'Doe
};

for (const key in person) {
    console.log(key);
}

======= OUTPUT ======
firstName
lastName
age

```
