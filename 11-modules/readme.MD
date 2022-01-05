# 11. How to use module in ES6 ? #
- First, create a new file called message.js and add the following code:

```js
export let message = 'ES6 Modules';

```

- The message.js is a module in ES6 that contains the message variable. The export statement exposes the message variable to other modules.

- Second, create another new file named app.js that uses the message.js module. The app.js module creates a new heading 1 (h1) element and attaches it to an HTML page. The import statement imports the message variable from the message.js module.

```js
import { message } from './message.js'

const h1 = document.createElement('h1');
h1.textContent = message

document.body.appendChild(h1)
````

Third, create a new HTML page that uses the app.js module:
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>ES6 Modules</title>
</head>
<body>
<script type="module" src="./app.js"></script>
</body>
</html>
```
Note that we used the <b>type="module"</b> in the script tag to load the app.js module.

## 1. Exporting ##

- To export a variable, a function, or a class, you place the export keyword in front of it as follows:


```js

// log.js
export let message = 'Hi';

export function getMessage() {
  return message;
}

export function setMessage(msg) {
  message = msg;
}

export class Logger {
}
```

## 2. Importing ##
- Once you define a module with exports, you can access the exported variables, functions, and classes in another module by using the import keyword. The following illustrates the syntax:

```js

import { what, ever } from './other_module.js';

```

## 3. Example ##

```js

// greeting.js
export let message = 'Hi';

export function setMessage(msg) {
  message = msg;
}

```


```js

// app.js
import {message, setMessage } from './greeting.js';
console.log(message); // 'Hi'

setMessage('Hello');
console.log(message); // 'Hello' 

```

## 4. Importing multiple binding ##
```js

// cal.js
export let a = 10,
           b = 20,
           result = 0;

export function sum() {
  result = a + b;
  return result;
}

export function multiply() {
  result = a * b;
  return result;
}

```

```js

import {a, b, result, sum, multiply } from './cal.js';
sum();
console.log(result); // 30

multiply();
console.log(result); // 200

```

## 5. Import entire module as an object ##

```js

// cal.js
export let a = 10,
           b = 20,
           result = 0;

export function sum() {
  result = a + b;
  return result;
}

export function multiply() {
  result = a * b;
  return result;
}

```

```js

import * as cal from './cal.js';

cal.a;
cal.b;
cal.sum();

```

## 6. Alias Import ##
```js

// math.js  
function add( a, b ) {
   return a + b;
}

export { add as sum };

```

```js

import { sum } from './math.js';
import {sum as total} from './math.js';

sum.a
sum.b

```


