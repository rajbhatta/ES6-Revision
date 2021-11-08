# 01 : Declaring Block-scoped variable #
- In ES5, when you declare a variable using the var keyword, the scope of the variable is either global or local. If you declare a variable outside of a function, the scope of the variable is global. When you declare a variable inside a function, the scope of the variable is local.
- ES6 provides a new way of declaring a variable by using the let keyword. The let keyword is similar to the var keyword, except that these variables are blocked-scope that is variable defined within a block won't be accessible from outside the block.

## Redeclaration ##
- The var keyword allows you to redeclare a variable without any issue:

```js
var counter = 0;
var counter;
console.log(counter); // 0
```

- However, redeclaring a variable using the let keyword will result in an error:

```js
let counter = 0;
let counter;
console.log(counter);
```
- Here’s the error message:

```js
Uncaught SyntaxError: Identifier 'counter' has already been declared
```

## Reference ##
- http://www.javascripttutorial.net/es6/javascript-let/ 