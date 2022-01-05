# 5. Why to use default parameters in Es6 #
- In JavaScript, default function parameters allow you to initialize named parameters with default values if no values or undefined are passed into the function.

## Setting JavaScript default parameters for a function ##
- In JavaScript, a parameter has a default value of undefined. It means that if you don’t pass the arguments into the function, its parameters will have the default values of undefined.

```js
function say(message) {
    console.log(message);
}

say(); 

======= OUTPUT ===========
// undefined

```

### Scanario 1: suppose we want to give the message parameter value of 10 ###

```js

function say(message) {
    message = typeof message !== 'undefined' ? message : '10';
    console.log(message);
}
say(); 

======= OUTPUT ==========
// '10'

```

# 2. Easiest way to use ES6 in JavaScript #
- ES6 provides you with an easier way to set the default values for the function parameters like this:

```js

function fn(param1=default1, param2=default2,..) {
}
```


- In the syntax above, you use the assignment operator (=) and the default value after the parameter name to set a default value for that parameter. For example:

```js

function say(message='Hi') {
    console.log(message);
}

say(); // 'Hi'
say(undefined); // 'Hi'
say('Hello'); // 'Hello'

````

## 2.1 Creating <b>div</b> using default parameter ##
- The following createDiv() function creates a new <div> element in the document with a specific height, width, and border-style:

```js

function createDiv(height = '100px', width = '100px', border = 'solid 1px red') {
    let div = document.createElement('div');
    div.style.height = height;
    div.style.width = width;
    div.style.border = border;
    document.body.appendChild(div);
    return div;
}

createDiv();

```
