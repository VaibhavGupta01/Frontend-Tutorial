# Typescript Tutorial (cheatsheet)

## Basic Types

```javascript
let id: number = 5
let company: string = 'Traversy Media'
let isPublished: boolean = true
let x: any = 'Hello'
```

## Arrays

```javascript
let ids: number[] = [1, 2, 3, 4, 5]
let arr: any[] = [1, true, 'Hello']
```

## Tuples

```javascript
let person: [number, string, boolean] = [1, 'Brad', true]
let employees: [number, string][]

employee = [
  [1, 'Brad'],
  [2, 'John'],
  [3, 'Jill'],
]
```

## Unions and Enums

Union allows variables to hold more than one type
```javascript
// Union
let pid: string | number
pid = '22'
```
Enum allows us to define named constants

```javascript
enum Direction1 {
  Up = 1,
  Down,
  Left,
  Right,
}

enum Direction2 {
  Up = 'Up',
  Down = 'Down',
  Left = 'Left',
  Right = 'Right',
}
```

## Objects

```javascript
type User = {
  id: number
  name: string
}

const user: User = {
  id: 1,
  name: 'John',
}
```

### Type Assertions

(similar to typecasting) 
explicitly telling a compiler that we want this variable to treat as a different type

```javascript
let cid: any = 1
// let customerId = <number>cid
let customerId = cid as number
```

(both ways can be used for type assertion)

## Functions

```javascript
// Functions
function addNum(x: number, y: number): number {
  return x + y
}

// Void
function log(message: string | number): void {
  console.log(message)
}
```


<!-- Basic boilerplate code -->

## Interfaces

```javascript
interface UserInterface {
  readonly id: number
  name: string
  age?: number  //denotes optional
}

const user1: UserInterface = {
  id: 1,
  name: 'John',
}
```

### Functional Interface


```javascript
interface MathFunc {
  (x: number, y: number): number
}

const add: MathFunc = (x: number, y: number): number => x + y
const sub: MathFunc = (x: number, y: number): number => x - y
```
Interface for a class
```javascript
interface PersonInterface {
  id: number
  name: string
  register(): string
}
```

## Classes 

```javascript
class Person implements PersonInterface {
  id: number
  name: string

  constructor(id: number, name: string) {
    this.id = id
    this.name = name
  }

  register() {
    return `${this.name} is now registered`
  }
}

const brad = new Person(1, 'Brad Traversy')
const mike = new Person(2, 'Mike Jordan')
```

## Sub-Classes 

```javascript
class Employee extends Person {
  position: string

  constructor(id: number, name: string, position: string) {
    super(id, name)
    this.position = position
  }
}

const emp = new Employee(3, 'Shawn', 'Developer')
```
## Generics

```javascript
function getArray<T>(items: T[]): T[] {
  return new Array().concat(items)
}

let numArray = getArray<number>([1, 2, 3, 4])
let strArray = getArray<string>(['brad', 'John', 'Jill'])

strArray.push(1) // Throws error
```

Source : [BradTraversy Video](https://www.youtube.com/watch?v=BCg4U1FzODs)