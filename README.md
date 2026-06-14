# JavaScript Cheat Sheet

## Table of Contents

|     Title    |     Contents    |
|--------------|-----------------|
|[Comments](#comments)|Single-Line, Multi-Line, JSDoc|
|[Console Output Methods](#console)| log, info, warn, error, clear|
|[Dialog Methods](#browser)| alert, confirm, prompt|
|[Variables & Consts](#vars)|var, let, const|
|[Conditional Statements](#conditional)|if, ternary, switch|
|[Loops](#loops)|for, while, do-while, for-of, for-in, break, continue|
|[Operators](#operators)|Arithmetic, Assignment, Comparison, Logical, Ternary, Typeof, Spread|
|[Timing Functions](#timing) | timeout, interval, clear|
|[Data Types](#data-types)|Primitive Data Types(number, string, boolean, null, undefined), Non-Primitive (Reference) Types(array, object, date)|
|[Strings](#strings)|Template Literals, length, padStart, padEnd, startsWith, endsWith, indexOf, lastIndexOf, includes, slice, substring, substr, split, repeat, replace, trim, trimStart, trimEnd, toUpperCase, toLowerCase, charAt|
|[Booleans](#booleans)| truthy, falsy(null, 0, "", [], undefined, NaN)|
|[Numbers](#numbers)|Conversion(Number, BigInt, parseInt, parseFloat), Validations(isNaN), toFixed, toPrecision|
|[Date](#date)|Declaration, Getters, Setters, Conversions|
|[Arrays](#arrays)|length, validation, destructuring,  spread operator, push, pop, shift, unshift, sort, reverse, map, filter, find, findIndex, every, some, forEach, includes, indexOf, lastIndexOf, splice, slice, join|
|[Objects](#objects)|Destructuring, Spread Operator|
|[Functions](#functions)|Traditional Functions, Function Expressions, Arrow Functions, IIFE, Closures, Async Functions|
|[Math Object](#math)|PI, abs, sign, trunc, floor, ceil, sqrt, pow, min, max, random, round|
|[Promises](#promises)|new promise, async/await, then/catch|
|[Error Handling](#errors)|try/catch, throw error|
|[Local/ Session Storage](#storage)| length, setItem, getItem, removeItem, clear|
|[JSON](#json)|stringify, parse|
|[Fetch API](#fetch)| method, body, response, error handling|



<h2 id="comments"> ✔️ Comments: </h2>

### Single-Line Comments:
```javascript
// This comment occupies one line
let count = 5; // Can be placed after code
```
### Multi-Line Comments:
```javascript
/*
  This comment spans
  multiple lines
*/
```

### JSDoc Comments:
```javascript
/**
 * JSDoc comment
 * Used for documentation
 */

/**
 * Returns sum of two numbers
 * @param {number} a
 * @param {number} b
 * @returns {number}
 */
function sum(a, b) {
    return a + b;
}
```

<h2 id="console"> ✔️ Console Output Methods: </h2>

### Log:
```javascript
console.log('Message');       // Regular logging
```

### Info:
```javascript
console.info('Information');  // Informational message
```

### Warn:
```javascript
console.warn('Warning!');     // Warning message (yellow)
```

### Error:
```javascript
console.error('Error!');      // Error message (red)
```

### Clear: 
```javascript
console.clear();              // Clear messages
```

<h2 id="browser"> ✔️ Dialog Methods: </h2>

### Alert:
```javascript
// Displays a message.
// Returns nothing
alert('This is an alert message!');
```

### Prompt:
```javascript
// Displays an input field.
// Returns a string or null.
const name = prompt('Please enter your name:');
```

### Confirm:
```javascript
// Displays OK and Cancel buttons.
// Returns true or false.
const isConfirmed = confirm('Are you sure?');

if (isConfirmed) {
  // Proceed
} else {
  // Cancel
}
```

<h2 id="vars"> ✔️ Variables & Consts: </h2>

### Const:
const by default - For all variables that won't be reassigned
```javascript
const PI = 3.14;
const config = {apiUrl: '...'};
```

### Let:
let when needed - For loop counters or variables that change
```javascript
let counter = 0;
counter++; // Valid
```

### Var:
var rarely - Only in specific cases
```javascript
var something = true;
```

<h2 id="conditional"> ✔️ Conditional Statements: </h2>

```javascript
// Basic if/else
if (condition) {
  // code to execute if true
} else {
  // code to execute if false
}

// Multiple conditions
if (score > 90) {
  grade = 'A';
} else if (score > 80) {
  grade = 'B';
} else if (score > 70) {
  grade = 'C';
} else {
  grade = 'F';
}

// Ternary operator (shorthand if/else)
const message = isLoggedIn ? 'Welcome back!' : 'Please log in';

// Switch statement
switch (dayOfWeek) {
  case 0:
    dayName = 'Sunday';
    break;
  case 1:
    dayName = 'Monday';
    break;
  // ...
  default:
    dayName = 'Unknown';
}

// Switch with multiple cases
switch (month) {
  case 12:
  case 1:
  case 2:
    season = 'Winter';
    break;
  case 3:
  case 4:
  case 5:
    season = 'Spring';
    break;
  // ...
}
```

<h2 id="loops"> ✔️ Loops: </h2>

```javascript
// Standard for loop
for (let i = 0; i < 10; i++) {
  console.log(i);
}

// Loop through array
const fruits = ['apple', 'banana', 'orange'];
for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}

// While loop
let i = 0;
while (i < 10) {
  console.log(i);
  i++;
}

// Do-while (executes at least once)
let j = 0;
do {
  console.log(j);
  j++;
} while (j < 10);

// Iterate over array values
const colors = ['red', 'green', 'blue'];
for (const color of colors) {
  console.log(color);
}

// Works with strings
const str = 'hello';
for (const char of str) {
  console.log(char);
}

// Iterate over object properties
const person = { name: 'John', age: 30 };
for (const key in person) {
  console.log(`${key}: ${person[key]}`);
}

// Check if property belongs to object
for (const key in person) {
  if (person.hasOwnProperty(key)) {
    console.log(key); // Only own properties (not inherited)
  }
}

// Break statement
for (let i = 0; i < 10; i++) {
  if (i === 5) break; // Exit loop
  console.log(i);
}

// Continue statement
for (let i = 0; i < 10; i++) {
  if (i % 2 === 0) continue; // Skip even numbers
  console.log(i);
}
```

<h2 id="operators"> ✔️ Operators: </h2>

### Arithmetic Operators:
```javascript
// Basic arithmetic
const sum = 10 + 5;    // 15 (Addition)
const diff = 10 - 5;   // 5 (Subtraction)
const product = 10 * 5; // 50 (Multiplication)
const quotient = 10 / 5; // 2 (Division)
const remainder = 10 % 3; // 1 (Modulus/Remainder)
const power = 2 ** 3;  // 8 (Exponentiation)

// Increment/Decrement
let count = 1;
count++; // Post-increment (returns 1, then sets to 2)
++count; // Pre-increment (sets to 3, then returns 3)
count--; // Post-decrement (returns 3, then sets to 2)
--count; // Pre-decrement (sets to 1, then returns 1)
```

### Assignment Operators:
```javascript
let x = 10; // Simple assignment

x += 5;  // x = x + 5
x -= 3;  // x = x - 3
x *= 2;  // x = x * 2
x /= 4;  // x = x / 4
x %= 3;  // x = x % 3
x **= 2; // x = x ** 2

// Destructuring assignment
const [a, b] = [1, 2];       // a=1, b=2
const {name, age} = person;   // name=person.name, age=person.age
```

### Comparison Operators:
```javascript
// Strict equality (type + value)
3 === 3   // true
3 === '3' // false

// Loose equality (value only)
3 == 3    // true
3 == '3'  // true

// Inequality
3 !== 4     // true (strict)
3 != '4'    // true (loose)
5 > 3       // true
5 < 3       // false
5 >= 5      // true
5 <= 4      // false
```

### Logical Operators:
```javascript
// AND (&&) - returns first falsy or last truthy
true && false    // false
0 && 'anything'  // 0
1 && 'hello'     // 'hello'

// OR (||) - returns first truthy or last falsy
false || true    // true
null || 'hello'  // 'hello'
0 || false       // false

// NOT (!)
!true           // false
!!'hello'       // true (double negation converts to boolean)

// Nullish coalescing (??) - returns right if left is null/undefined
null ?? 'default'    // 'default'
0 ?? 'default'       // 0 (unlike || which would return 'default')
```

### Ternary Operator:
```javascript
// Syntax: condition ? exprIfTrue : exprIfFalse
const status = age >= 18 ? 'Adult' : 'Minor';

// Chained ternary
const grade = score >= 90 ? 'A'
             : score >= 80 ? 'B'
             : score >= 70 ? 'C'
             : 'F';
```

### Type Operators:
```javascript
typeof 42        // 'number'
typeof 'hello'   // 'string'
typeof true      // 'boolean'
typeof undefined // 'undefined'
typeof null      // 'object' (historical bug)
typeof {}        // 'object'
typeof []        // 'object'
typeof Symbol()  // 'symbol'
typeof BigInt(1) // 'bigint'

// Instanceof
[] instanceof Array    // true
new Date() instanceof Date // true

// in operator (checks property existence)
'name' in person // true if person has 'name' property
```

### Spread Operator:

#### Array Operations:
```javascript
// Copying arrays
const original = [1, 2, 3];
const copy = [...original]; // [1, 2, 3]

// Concatenating arrays
const arr1 = [1, 2];
const arr2 = [3, 4];
const combined = [...arr1, ...arr2]; // [1, 2, 3, 4]
```

#### Object Operations:
```javascript
// Copying objects
const obj = { a: 1, b: 2 };
const objCopy = { ...obj }; // { a: 1, b: 2 }

// Merging objects
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };
const merged = { ...obj1, ...obj2 }; // { a: 1, b: 2, c: 3, d: 4 }

// Overwriting properties
const defaults = { theme: 'light', fontSize: 14 };
const userSettings = { theme: 'dark' };
const finalSettings = { ...defaults, ...userSettings };
// { theme: 'dark', fontSize: 14 }

// Adding new properties
const user = { name: 'Alice' };
const withAge = { ...user, age: 30 }; // { name: 'Alice', age: 30 }
```

<h2 id="timing"> ✔️ Timing Functions: </h2>

### Timeout:
Use for one-time delayed execution
```javascript
// Example
const timer = setTimeout(() => {
  console.log('This runs after 2 seconds');
}, 2000);

// Cancel the timeout before it executes
clearTimeout(timer);
```

### Interval:
Use for repeating delayed executions
```javascript
// Example
let counter = 0;
const interval = setInterval(() => {
  counter++;
  console.log(`Tick ${counter}`);
  if (counter >= 5) {
    clearInterval(interval);
  }
}, 1000);

// Stop the interval execution
clearInterval(interval);
```

<h2 id="data-types"> ✔️ Data Types: </h2>

### Primitive Data Types:
```javascript
// number:
let age = 25;
let pi = 3.14;

// string:
let name = "Alice";
let greeting = 'Hello World';

// boolean:
let isActive = true;
let isComplete = false;

// undefined:
let x;
console.log(x); // undefined

// null:
let empty = null;
```

### Non-Primitive (Reference) Type:
object - Collections of properties
```javascript
let person = { name: "John", age: 30 };
let colors = ["red", "green", "blue"];
let date = new Date();
```

### The typeof Operator:
```javascript
typeof "Hello"       // "string"
typeof 42            // "number"
typeof true          // "boolean"
typeof undefined     // "undefined"
typeof null          // "object" (historical bug)
typeof {a: 1}        // "object"
typeof [1, 2, 3]     // "object"
typeof function() {} // "function"
```

<h2 id="strings"> ✔️ Strings: </h2>

### Template Literals:
```javascript
const name = "Alice";
const greeting = `Hello ${name}!`; // "Hello Alice!"
const multiLine = `
  This is a
  multi-line
  string
`;
```

### Length:
```javascript
const str = "Hello";
console.log(str.length); // 5
```

### Methods:
```javascript
"Hello".toUpperCase(); // "HELLO"
"Hello".toLowerCase(); // "hello"
"JavaScript".indexOf("Script"); // 4
"JavaScript".lastIndexOf("a"); // 3
"JavaScript".includes("Java"); // true
"JavaScript".startsWith("Java"); // true
"JavaScript".endsWith("Script"); // true
"Hello World".slice(6, 11); // "World"
"Hello World".substring(6, 11); // "World"
"Hello World".substr(6, 5); // "World" (deprecated)
"Hello World".charAt(1); // "e"
"Hello World".charCodeAt(1); // 101 (Unicode)
"   Hello   ".trim(); // "Hello"
"   Hello   ".trimStart(); // "Hello   "
"   Hello   ".trimEnd(); // "   Hello"
"Hello".repeat(3); // "HelloHelloHello"
"Hello".replace("e", "a"); // "Hallo"
"Hello World".split(" "); // ["Hello", "World"]
"5".padStart(3, "0"); // "005"
"Hi".padEnd(5, "!"); // "Hi!!!"
```

<h2 id="booleans"> ✔️ Booleans: </h2>

#### Falsy Values:
```javascript
false     // Boolean false
0         // Number zero
-0        // Negative zero
0n        // BigInt zero
""        // Empty string
null      // Null
undefined // Undefined
NaN       // Not a Number
```

<h2 id="numbers"> ✔️ Numbers: </h2>

### Conversion:
```javascript
Number("123")  // 123
parseFloat("123.45") // 123.45
parseInt("123px")    // 123
```

### Validations:
```javascript
function isNumber(value) {
  return typeof value === 'number' && !isNaN(value);
}
```

### Instance Methods:
```javascript
(123.456).toFixed(2)     // "123.46" (string)
(123.456).toPrecision(4) // "123.5" (string)
```

<h2 id="date"> ✔️ Date: </h2>

### Date Declaration:
```javascript
const now = new Date(); // Current date and time
const date = new Date("2023-10-05"); // ISO format (local time)
const date = new Date(1633036800000); // Milliseconds since Jan 1, 1970
const now = new Date(); // Current date and time
```

### Getter Methods:
```javascript
const date = new Date();
date.getFullYear()    // 2023 (4-digit year)
date.getMonth()       // 0-11 (0 = January)
date.getDate()        // 1-31 (day of month)
date.getDay()         // 0-6 (0 = Sunday, day of week)
date.getHours()       // 0-23
date.getMinutes()     // 0-59
date.getSeconds()     // 0-59
date.getMilliseconds()// 0-999
date.getTime()        // Milliseconds since epoch
date.getTimezoneOffset() // Timezone offset in minutes
```

### Setter Methods:
```javascript
date.setFullYear(year [, month, day])
date.setMonth(month [, day])
date.setDate(day)
date.setHours(hour [, min, sec, ms])
date.setMinutes(min [, sec, ms])
date.setSeconds(sec [, ms])
date.setMilliseconds(ms)
date.setTime(milliseconds)
```

### Conversion Methods:
```javascript
date.toString()       // "Thu Oct 05 2023 13:30:00 GMT+0200"
date.toDateString()   // "Thu Oct 05 2023"
date.toTimeString()   // "13:30:00 GMT+0200"
date.toISOString()    // "2023-10-05T11:30:00.000Z" (UTC)
date.toUTCString()    // "Thu, 05 Oct 2023 11:30:00 GMT"
date.toJSON()         // "2023-10-05T11:30:00.000Z" (for JSON)
date.toLocaleString() // "10/5/2023, 1:30:00 PM" (local format)
date.toLocaleDateString() // "10/5/2023"
date.toLocaleTimeString() // "1:30:00 PM"
```

<h2 id="arrays"> ✔️ Arrays: </h2>

### Length:
```javascript
const fruits = ['apple', 'banana'];
console.log(fruits.length); // 2
```

### Methods:
```javascript
// Add/Remove
fruits.push('orange');      // Add to end (returns new length)
fruits.pop();               // Remove from end (returns item)
fruits.unshift('strawberry'); // Add to start
fruits.shift();             // Remove from start

// Modify
fruits.splice(1, 0, 'mango'); // Add at index 1
fruits.reverse();            // Reverse array
fruits.sort();               // Sort alphabetically
// Search
fruits.includes('apple');    // true
fruits.indexOf('banana');    // 1
fruits.find(fruit => fruit.startsWith('b')); // 'banana'
fruits.findIndex(fruit => fruit.length > 5); // 1

// Transformation
fruits.map(fruit => fruit.toUpperCase()); // New array
fruits.filter(fruit => fruit.length > 5); // Filtered array
fruits.reduce((total, fruit) => total + fruit.length, 0); // Sum lengths

// Iteration
fruits.forEach(fruit => console.log(fruit));
fruits.every(fruit => fruit.length > 3); // All satisfy?
fruits.some(fruit => fruit === 'apple'); // Any satisfy?
```

### Validation:
```javascript
Array.isArray(fruits); // true (best way)
fruits instanceof Array; // true
```

### Destructuring:
```javascript
// Basic Destructuring
const [first, second] = fruits;
console.log(first); // 'apple'

// Skipping Items
const [first, , third] = ['a', 'b', 'c']; // first='a', third='c'

// Default Values
const [a=1, b=2] = []; // a=1, b=2

// Rest Pattern
const [head, ...tail] = [1, 2, 3]; // head=1, tail=[2, 3]
```

### Spread Operator:
```javasript
// Copying Arrays
const copy = [...fruits]; // Shallow copy

// Merging Arrays
const moreFruits = [...fruits, 'pear', ...['grape', 'melon']];
```

<h2 id="objects"> ✔️ Objects: </h2>

### Declaration:
```javascript
const person = {
  name: 'Alice',
  age: 30,
  isAdmin: false,
  greet() {
    console.log(`Hello, I'm ${this.name}`);
  }
};
```

### Object Destructuring:
```javascript
// Basic destructuring
const { name, age } = person;
console.log(name); // 'Alice'

// Renaming variables
const { name: personName, age: personAge } = person;

// Default values
const { isAdmin = true, country = 'USA' } = person;

// Nested destructuring
const user = {
  id: 1,
  profile: {
    email: 'alice@example.com',
    address: {
      city: 'New York'
    }
  }
};

const {
  profile: { 
    email,
    address: { city }
  }
} = user;
```

### Spread Operator:
```javascript
// Copying objects
const personCopy = { ...person };

// Merging objects
const details = { occupation: 'Developer', country: 'Canada' };
const completeProfile = { ...person, ...details };

// With overwriting
const updatedPerson = { ...person, age: 31 };
```

### Methods:
``` javascript
// Object.keys()
const keys = Object.keys(person); // ['name', 'age', 'isAdmin', 'greet']

// Object.values()
const values = Object.values(person); // ['Alice', 30, false, [Function: greet]]

// Object.entries()
const entries = Object.entries(person);
// Returns array of [key, value] pairs
```

<h2 id="functions"> ✔️ Functions: </h2>

### Traditional Functions:
```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
```

### Function Expressions:
```javascript
const greet = function(name) {
  return `Hello, ${name}!`;
};
```

### Arrow Functions:
```javascript
const greet = (name) => {
  return `Hello, ${name}!`;
};
```

### IIFE (Immediately Invoked Function Expression):
```javascript
// Traditional IIFE
(function() {
  console.log('Runs immediately');
})();

// Arrow function IIFE
(() => {
  console.log('Also runs immediately');
})();

// With parameters
((name) => {
  console.log(`Hello, ${name}`);
})('Alice');
```

### Closures:
```javascript
function createCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}

const counter = createCounter();
counter(); // 1
counter(); // 2
```

### Async Functions:
```javascript
// Async/await
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    return data;
  } catch (error) {
    console.error('Error:', error);
  }
}

// Arrow async function
const fetchData = async () => {
  // ...
};
```


<h2 id="math"> ✔️ Math Object: </h2>

```javascript
Math.PI        // π (3.141592653589793)
Math.abs(-5)      // 5 (absolute value)
Math.sign(-3)     // -1 (sign of number)
Math.sqrt(16)     // 4 (square root)
Math.pow(2, 3)    // 8 (2 to the power of 3)
Math.round(4.7)   // 5 (nearest integer)
Math.floor(4.9)   // 4 (round down)
Math.ceil(4.1)    // 5 (round up)
Math.trunc(4.9)   // 4 (remove decimal)
Math.min(1, 2, 3)     // 1 (smallest value)
Math.max(1, 2, 3)     // 3 (largest value)
Math.random()          // Random float between 0 (inclusive) and 1 (exclusive)
```

### Random Number in Range:
```javascript
function randomInRange(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
// randomInRange(5, 10) → random integer between 5-10 inclusive
```

<h2 id="promises"> ✔️ Promises: </h2>

### Create Promise:
```javascript
// Creating a promise
const myPromise = new Promise((resolve, reject) => {
  const success = true; // Simulate condition
  if (success) {
    resolve('Operation succeeded!');
  } else {
    reject('Operation failed!');
  }
});
```

### Then/ Catch Syntax:
```javascript
// Basic promise handling
myPromise
  .then(result => {
    console.log(result); // "Operation succeeded!"
  })
  .catch(error => {
    console.error(error); // "Operation failed!"
  });

// Chaining .then()
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error('Fetch error:', error);
  });

// Finally clause
somePromise
  .then(result => { /*...*/ })
  .catch(error => { /*...*/ })
  .finally(() => {
    console.log('This runs regardless of success/failure');
  });
```

### Async/Await Syntax:
```javascript
// Basic async function
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
    return data;
  } catch (error) {
    console.error('Error:', error);
    throw error; // Re-throw if you want calling code to handle it
  }
}

// Immediately-invoked async function
(async () => {
  const data = await fetchData();
  console.log('Data received:', data);
})();
```

<h2 id="errors"> ✔️ Error Handling: </h2>

```javascript
// Try-catch block
try {
  // Code that might throw an error
  const result = riskyOperation();
  console.log(result);
} catch (error) {
  console.error('Something went wrong:', error.message);
} finally {
  console.log('This always executes');
}

// Throwing custom errors
function validateInput(input) {
  if (!input) {
    throw new Error('Input cannot be empty');
  }
  if (input.length < 5) {
    throw new Error('Input must be at least 5 characters');
  }
}
```

### Error Types:
```javascript
// Built-in error types
try {
  // ...
} catch (error) {
  if (error instanceof TypeError) {
    console.error('Type error:', error.message);
  } else if (error instanceof ReferenceError) {
    console.error('Reference error:', error.message);
  } else if (error instanceof SyntaxError) {
    console.error('Syntax error:', error.message);
  } else {
    console.error('Unknown error:', error.message);
  }
}

// Creating custom error types
class ValidationError extends Error {
  constructor(message) {
    super(message);
    this.name = 'ValidationError';
    this.date = new Date();
  }
}

try {
  throw new ValidationError('Invalid input');
} catch (error) {
  if (error instanceof ValidationError) {
    console.error(`${error.name} at ${error.date}: ${error.message}`);
  }
}
```

<h2 id="storage"> ✔️ Local/ Session Storage: </h2>

```javascript
// Set item
localStorage.setItem('username', 'john_doe');
sessionStorage.setItem('token', 'abc123');

// Get item
const username = localStorage.getItem('username'); // 'john_doe'
const token = sessionStorage.getItem('token'); // 'abc123'

// Remove item
localStorage.removeItem('username');
sessionStorage.removeItem('token');

// Clear all
localStorage.clear();
sessionStorage.clear();

// Check length
const localStorageSize = localStorage.length;
const sessionStorageSize = sessionStorage.length;
```

<h2 id="json"> ✔️ JSON: </h2>

```javascript
// Stringify (Object → JSON string)
const obj = { name: "John", age: 30, city: "New York" };
const jsonString = JSON.stringify(obj);
// '{"name":"John","age":30,"city":"New York"}'

// Parse (JSON string → Object)
const parsedObj = JSON.parse(jsonString);
// { name: "John", age: 30, city: "New York" }
```

<h2 id="fetch"> ✔️ Fetch API: </h2>

### Basic Requests:
```javascript
// GET request
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));

// POST request with JSON
fetch('https://api.example.com/data', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({ key: 'value' })
})
.then(response => response.json())
.then(data => console.log('Success:', data))
.catch(error => console.error('Error:', error));
```

### Response Handling:
```javascript
fetch('https://api.example.com/data')
  .then(response => {
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    const contentType = response.headers.get('content-type');
    if (contentType.includes('application/json')) {
      return response.json();
    }
    return response.text();
  })
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

### Async/Await Syntax:
```javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    const data = await response.json();
    console.log(data);
    return data;
  } catch (error) {
    console.error('Fetch error:', error);
    throw error; // Re-throw if you want calling code to handle it
  }
}
```

### Error Handling Patterns:
```javascript
// Better error handling with status codes
async function fetchWithErrorHandling(url) {
  const response = await fetch(url);
  
  if (response.status === 404) {
    throw new Error('Resource not found');
  }
  if (response.status === 401) {
    throw new Error('Unauthorized');
  }
  if (response.status === 500) {
    throw new Error('Server error');
  }
  if (!response.ok) {
    throw new Error(`HTTP error! status: ${response.status}`);
  }
  
  return await response.json();
}

// Usage
fetchWithErrorHandling('https://api.example.com/data')
  .then(data => console.log(data))
  .catch(error => {
    console.error('Error:', error.message);
    // Show user-friendly message based on error type
  });
```




