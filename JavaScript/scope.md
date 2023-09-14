# JavaScript Scope

## Introduction
Let's dive into the world of JavaScript scope, a fundamental concept that greatly affects how variables and functions are seen and accessed in your code. Here you'll learn about the four primary JavaScript scopes: global scope, function scope, block scope, and the more advanced lexical scope.

## Scope
In JavaScript, scope is a concept that dictates how code executes within specific rules, determining its access and interaction with the rest of the code. Each function or variable lives within a particular scope.

```javascript
var a = 10; // Global variable

function f() {
  var b = 20; // Local variable
  console.log(a); // Prints 10
}

f();
```

This code demonstrates the concept of scope in JavaScript by allowing variable `a` to be accessible from anywhere in the program and variable `b` to be accessible only from within the function `f()`. This helps ensure proper variable usage, prevents naming conflicts, and enhances code readability and management.

## Module Scope
Module scope variables are limited to the file in which they are defined. You cannot use them in other files. To establish module scope, you must use `type="module"` in your script tags.

### Example
```javascript
function myFunction() {
 var x = 10;
}
```

Variable `x` in this code can only be used within `myFunction()` and nowhere else. Attempting to access it from outside will result in an error.

## Global Scope
When a variable is declared outside of a function, it becomes global. In simple terms, global scope refers to a shared space where any part of your code can access a variable. You can access the variable from anywhere in your program, just like a common area.

### Example
```javascript
var globalVariable = 42;

function myFunction() {
 console.log(globalVariable);
}

myFunction();
```

In this case, `globalVariable` is declared outside the function, making it a global variable. Because it exists in the global scope, it can be accessed and used in `myFunction()`.

## Block Scope
The concept of block scope was introduced in JavaScript ES6. Block scope is easy to understand because it is based on curly braces. Essentially, curly brackets define a block scope for code. This includes functions, if statements, for loops, and other constructs, each creating its own block scope.

### Example
```javascript
{
 var z = 30;
}
```

You can use variable `z` within these curly braces, but it cannot be used outside of them because it only exists within this block.

## Lexical Scope (Function Scope)
Variables and functions defined in lexical scope are available within the function. Variables declared with `var` have function scope, 
while variables declared with `let` and `const` have block scope when declared within a function.

### Example
```javascript
function outerFunction() {
 var a = 40;
function innerFunction() {
 console.log(a); // 40
 }
}
```

In this example, the variable `a` defined in `outerFunction()` is accessible within `innerFunction()`. Understanding JavaScript scope is crucial in web development, as it helps you craft efficient, bug-free code.

That's all for today! We hope you find this information useful.
