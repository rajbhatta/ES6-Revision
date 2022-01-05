# Working with Rest Paramter in ES6 #
- ES6 provides a new kind of parameter so-called rest parameter that has a prefix of three dots <b> (...). A rest parameter allows you to represent an indefinite number of arguments as an array.

```js

function fn(a,b,...args) {
   console.log(a)  // 1
   console.log(b)  // 2
   console.log(args) // [3,'A','B','C']
}

fn(1, 2, 3, "A", "B", "C");

```


- The last parameter (args) is prefixed with the three-dots ( ...). It’s called a rest parameter ( ...args).

```js

function fn(a,b,...args) {
   console.log(a)  // 1
   console.log(b)  // 2
   console.log(args) // []
}

fn(1, 2, []);

```

## Note: rest paramters must be appeared at the end of the function call ##

```js

function fn(a,...rest, b) {
 // error
}

SyntaxError: Rest parameter must be last formal parameter

```



