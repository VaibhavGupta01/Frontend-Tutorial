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

<!-- Basic boilerplate code -->

## 

```javascript
```

Source : [BradTraversy Video](https://www.youtube.com/watch?v=BCg4U1FzODs)