# How to perform object destructing in ES6 ? #
- It allows us to destruct the property of the object.

## 1. Traditional way of extracting object property ##
```js

let person = {
    firstName: 'John',
    lastName: 'Doe'
};

let firstName = person.firstName;
let lastName = person.lastName; 

```

## 2. Extracting destructing object property using ES6 ##

- <b> Sytanx </b>

```js

let { property1: variable1, property2: variable2 } = object;

```

- The identifier before the colon (:) is the property of the object and the identifier after the colon is the variable.

- <b> Example </b>
```js

let person = {
    firstName: 'John',
    lastName: 'Doe'
};

let { firstName: fname, lastName: lname } = person;

```

- In this example, the firstName and lastName properties are assigned to the fName and lName variables respectively.

## 3. Destructing nested object ###
```js

let employee = {
    id: 1001,
    name: {
        firstName: 'John',
        lastName: 'Doe'
    }
};

let {
    name: {
        firstName,
        lastName
    }
} = employee;

console.log(firstName); // John
console.log(lastName); // Doe

```

