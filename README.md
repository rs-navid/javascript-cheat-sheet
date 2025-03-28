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

## Comment Types:

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

## Console Methods:

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

## Browser Interaction Methods:

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

## JavaScript Variable Declarations:

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

## JavaScript Timing Functions:

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





