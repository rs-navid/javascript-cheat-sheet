# JavaScript Cheat Sheet

## Table of Contents:
- [Comment Types](#comment-types)
  - [Single-Line Comments](#single-line-comments)
  - [Multi-Line Comments](#multi-line-comments)
- [Console Methods](#console-methods)
  - [Log](#log)
  - [Info](#info)
  - [Warn](#warn)
  - [Error](#error)
  - [Clear](#clear)
- [Browser Interaction Methods](#browser-interaction-ethods)
  - [Alert](#alert)
  - [Prompt](#prompt)
  - [Confirm](#confirm)
- [JavaScript Variable Declarations](#javascript-variable-declarations)
  - [Const](#const)
  - [Let](#let)
  - [Var](#var)
- [JavaScript Timing Functions](#javascript-timin-functions)
  - [Timeout](#timeout)
  - [Interval](#interval)

## 🔘 Comment Types:

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

## 🔘 Console Methods:

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
console.clear();      // Clear messages
```

## 🔘 Browser Interaction Methods:

### Alert:
```javascript
alert('This is an alert message!');
```

### Prompt:
```javascript
const name = prompt('Please enter your name:');
```

### Confirm:
```javascript
const isConfirmed = confirm('Are you sure?');
if (isConfirmed) {
  // Proceed
} else {
  // Cancel
}
```

## 🔘 JavaScript Variable Declarations:

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

## 🔘 JavaScript Timing Functions:

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

## 🔘 Data Types:

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

## 🔘 Strings:

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

## 🔘 Booleans:

### Falsy Values:
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

## 🔘 Numbers:

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

### 🔘 Math Object: Properties and Methods
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

## Random Number in Range:
```javascript
function randomInRange(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
// randomInRange(5, 10) → random integer between 5-10 inclusive
```





