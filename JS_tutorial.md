# Javascript Tutorial (cheatsheet)

## Datatypes

Basic Datatypes in javascript are :- String, Number, Boolean, null, undefined

_(There is another datatype called symbol which is rarely used)_

```javascript
const name = 'Brad';
const age = 37;
const rating = 3.5;// also number
const isCool = true;
const x = null;
const y = undefined;
let z; // undefined
```
> * string can be defined using both 'single quote' and "double quotes"
> * no floats in javascript, decimals are also number datatype


### To check type of variable
```javascript
console.log(typeof z);
```
_TODO: typeof null comes object?_

### Using Template literals
```javascript
console.log(`My name is ${name} and I am ${age}`);
```
## Arrays

```javascript
const numbers = [1,2,3,4,5];
const fruits = ['apples', 'oranges', 'pears', 'grapes', 10, true];
```
> * In JS, arrays can have multiple datatypes wihtin the same array
> * You won't be able to re-assign a const array, for ex.\
` numbers = [];` \
will give out error, although you can push new items in the array \
`numbers.push(10);` \
this will work

## Objects

```javascript
const person = {
  firstName: 'John',
  age: 30,
  hobbies: ['music', 'movies', 'sports'],
  address: {
    street: '50 Main st',
    city: 'Boston',
    state: 'MA'
  }
}
```
> * You can add new properties on runtime\
`person.email = 'jdoe@gmail.com';`
> * You can pull variables out of the object and assign it to variables(destructuring) 
> ```
> const {firstName, address:{city}}  = person;
> console.log(city);
> ```
> _TODO : check destructuring in ES6 properly_

### __For of loop__

```javascript
const todos = [
  {
    id: 1,
    text: 'Take out trash',
    isComplete: false
  },
  {
    id: 2,
    text: 'Dinner with wife',
    isComplete: false
  },
  {
    id: 3,
    text: 'Meeting with boss',
    isComplete: true
  }
];

// more conveniant than using for(let i = 0; i < todos.length; i++)
for(let todo of todos) {
  console.log(todo.text);
}
```
## High Order Array Methods

The High Order Array Methods take function as a parameter

forEach() loops through an array
```javascript
// forEach() - Loops through array
todos.forEach(function(todo, i, myTodos) {
  console.log(`${i + 1}: ${todo.text}`);
  console.log(myTodos);
});
```
map() loops and returns an array
```javascript
// map() - Loop through and create new array
const todoTextArray = todos.map(function(todo) {
  return todo.text;
});

console.log(todoTextArray);
```
filter() loops and returns an array based on some condition
```javascript
// filter() - Returns array based on condition
const todo1 = todos.filter(function(todo) {
  // Return only todos where id is 1
  return todo.id === 1; 
});
```
We can also chain on array methods
```javascript
const todo1 = todos.filter(function(todo) {
  return todo.id === 1; 
}).map(function(todo) {
  return todo.text;
});
```
_TODO: High Order Array Methods in more detail_
### Conditionals

Triple equals also checks the datatype
```javascript
const x = 10;

if(x === 10) {
  console.log('x is 10');
}
```

> In below example, the statement is still true
> ```
>const x = '10';
>
>if(x == 10) {
>  console.log('x is 10');
>}
> ```

## Functions

```javascript
function greet(greeting = 'Hello', name) {
  if(!name) {
    return greeting;
  } else {
    return `${greeting} ${name}`;
  }
}
```
## Arrow Functions

```javascript
const greet = (greeting = 'Hello', name = 'There') => `${greeting} ${name}`;
console.log(greet('Hi'));
```
> * if single line body, arrow function expression can be written in single  line, otherwise, put inside '{ }'
> * Additionally, you don't have to add 'return' statement, if you want to return something 
> * Additionally, if you have just one param, you don't have to add paranthesis \
`const addNums = num1 => num1 + 5;` \
`console.log(addNums(5));`

_TODO : check arrow functions scoping with this keyword_

<!-- basic boilerplate snippet -->
## 

```javascript

```

Source : [BradTraversy Video](https://www.youtube.com/watch?v=hdI2bqOjy3c)