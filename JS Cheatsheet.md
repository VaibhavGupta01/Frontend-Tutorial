# JS Tutorial


## 1-3. VS Code Setup
* Installing VS Code and extensions like Live Server, Bracket Colorizer
* Emmet Shortcuts
  * h1 tab generates h1 tags `(<h1></h1>)`
  * #test tab generates `(<div id="test"></div>)`
  * .test tab generates `(<div class="test"></div>)`
  * h1.test tab generates `(<h1 class="test"></h1>)`
  * *! + Tab* generates basic HTML Document head and body tags

## 2-4. File Setup
* You can run JS code in script tags -OR- you can add src external js file 

## 2-5. Using Console
- `console.table();`                        create a table for objects.
- `console.error();`                        create an error log.
- `consoe.warn();`                          create a warn log.
- `console.clear();`                        clear the console.
- `console.time(); and console.timeEnd()`   calculate the time it takes to execute the code.

## 2-6. Variables
* Const variables cannot:
  1) have to assign a value i.e. cannot init a const variable unlike var and let.
  2) cannot reasign a value for the const variable unlike var and let.
   
For Example : 
```javascript
const numbers = [1,2,3,4,5];
numbers.push(6);
```
We can add/change the array/objects; however, we cannot reassign/re-declare the array or object. For example:
```javascript
const numbers = [1,2,3,4,5];
numbers = [1,2,3,4,5,6];
```

## 2-7. Variables
### Primitive Data Types
- Stored directly in the location the variable accesses.
- Stored on the stack

When you access a primitive data type you access it by its actual value.

6 Primitive Data Types:
1) String - sequence of characters.
2) Number - a number (integers, decimals, floats are all consindered as numbers).
3) Boolean - true or false (1 or 0).
4) Null - intentional empty value.
5) Undefined - a variable that has not been assigned a value.
6) Symbols (ES6).

### Reference Data Types
- Objects accessed by reference
- Objects that are stored on the heap
- A pointer to a location in memory
The data isn't actually stored in the variable its stored in what is called the heap (to do with dynamically allocated memory - advanced topic to research after you have a grasp of the JavaScript language).

Reference Data Types are not accessed by the actual (primitve) value, they are accessed by reference. They are also considered as objects.

5 Reference Data Types:
- Arrays
- Object Leterals
- Functions
- Dates
- Anything else

### JS - Dynamically Typed Language
- Types are associated with values not variables.
- The same variable can hold multiple types (e.g. variable can hold a string then set to a number without any errors or issues).
- We do not need to specify types.
- Most other languages are statically typed (Java, C#, C++).
- There are superets of JavaScript and addons to allow static typing (TypScript, Flow).

## 2-8. Type Conversion

### Converting to a String
There are two ways in which we can convert data types into strings:
1) String(); function
2) .toString(); method

We can convert the following data types to a string:
- numbers (and expressions)
- booleans
- dates
- arrays

The .legnth property only works on string data types and returns the number of characters within a string data type.

### Converting to a Number
There are two ways in which we can convert data types into number:
1) Number(); function
2) parseInt(); & parseFloat(); methods

We can convert the following data types to a number:
- strings
- boolean (1 = true, 0 = false)
- Null (0)

The .tofixed() property only works on Number data types and returns the number as a decimal/float number based on the number within the parentheses (if left blank then no decimal point).

NaN stands for Not a Number and will apply to when we try to convert a string such as 'Hello' or an array such as [1,2,3] to a number.

parseInt() will return a integer number whereas parseFloat() will return a decimal number.

## Type Coercion
Implicit Type Conversion or Coercion (automatically done during code execution)

`'5' + 6 = 56 (JavaScript Coercion)`

## 2-9. Math Object
Math Objects allows us to do math functions such as round a number, find the absolute, powers, generate random numbers etc.

## 2-10. String Methods & Concatenation
***NOT REQUIRED***

## 2-11. Template Literals

**Example of a HTML String (ES5):**
```javascript
html = "<ul>" +
   "<li>Name: " + name + "</li>" +
   "<li>Age: " + age + "</li>" +
   "<li>Job: " + job + "</li>" +
   "<li>City: " + city + "</li>" +
   "</ul>";
```
**ES6 Template Literals**
```javascript
htmlAlt = `
   <ul>
      <li>Name: ${name}</li>
      <li>Age: ${age}</li>
      <li>Job: ${job}</li>
      <li>City: ${city}</li>
  </ul>
`;
```

We can also add JavaScript: 
- Expressions, for example ${2+2} or 
- Functions, for example ${hello()} or
- Conditionals, for example ${age > 30 ? "Over 30" : "Under 30"}

## 2-12. Arrays & Array Methods

There are two ways to create an array:
* Create a variable and assign values within the square brackets, for example:
   `const variable = [1, 2, 3, 4];`
* Using an array constructor to create an array object, for example:
   `const variable = new Array(1, 2, 3, 4);`




Source : [BradTraversy Video](https://www.udemy.com/course/modern-javascript-from-the-beginning)