# Functions in JavaScript

A `function` is a block of code you can use to create reusable code. Functions are referred to as first-class data types in JavaScript. This implies that anything you could do with variables and objects, you could also accomplish with functions. You may pass that around, assign it to a variable, and use it as an argument when calling another function.  In addition, a function can return it as a result.

Functions can also be called objects. In other words, they are regular objects with special properties.

## Function definition and invoke a function
Defining a function starts with the `function` keyword, followed by a `name (greet)`, parentheses `(list of parameters)`, and `curly brackets`, where all of the action takes place. 

A function can be used by referring to it with `parentheses ()` immediately after its name and by giving any necessary arguments. This is referred to as invoking a function.

Here's an example to elaborate on all this:
```javascript
function greet(name) {
 console.log('Hello, ${name}!')
}
greet("John"); // Output: Hello, John!
```
It is not necessary to have parameters for a function; the parentheses can simply be left empty:

**Example:**
```javascript
function greet() {
  console.log(Hello World!)
}
greet() // Output: Hello World!

```

A function with parameters, however, requires the parameters' values to be entered in parentheses:

**Example:**
```javascript
function greet(name) {
 console.log('Hello, ${name}!')
}
greet("John"); // Output: Hello, John!
```
If your function accepts more than one argument, separate them with a comma inside the parentheses.

## return statement
In functions `return` statements are used to return values. This is crucial if you plan to use computation results elsewhere in your code.

```javascript
function multiply(x, y) {
  return x * y;
}
const result = multiply(4, 4);
console.log(result); // Output: 16
```
## Function Expressions
You can create function expressions in JavaScript by assigning a function to a variable.

They are flexible constructs for creating higher-order and anonymous functions.

**Example:**
```javascript
const multiply = function(x, y) { 
    return x * y; 
};
```
## Arrow functions
The arrow function is introduced in ES6. It is an efficient method of writing JavaScript functions. When writing short, one-line functions, they come in very handy. 

**Example:**
```javascript
const add = (a, b) => a + b;
```

## Scope and Encapsulation
The term `scope` describes the visibility of variables throughout different parts of your code. 
Function-specific variables have a local scope and can only be used within that function. 
This concept prevents unintended interference and promotes encapsulation.

**Example:**
```javascript
function calculateTotalPrice(price) {
  const taxRate = 0.08;
  const totalPrice = price + price * taxRate;
  return totalPrice;
}
```

`let`` and `const` variables, introduced in ES6, have a block scope. Which means that you can only access them within the given block. This stops scope leakage and enables more exact handling of data. 

## Closures
In JavaScript, closures act as a sort of lexical scoping by preserving variables from a function's external scope in its inner scope. 
In functions, closures allow the creation of `private` variables. 

**Example:**
```javascript
function outer() {
  const message = "Hello from outer!";
  function inner() {
    console.log(message);
  }
  return inner;
}
const innerFunction = outer();
innerFunction(); // Output: Hello from outside!
```
## Key takeaways
- Functions are great for efficiency because you just need to define them once to use them as many times as you require. 
- You don't have to keep writing the same or substantially similar code. 
- You can use JavaScript functions to give it different inputs or arguments to get different results depending on the data you are dealing with.
- JavaScript functions make it easier and faster to build programs.
  

**⭐ That's pretty much it for today. I really hope you find it helpful! If you have any questions DM me on Twitter/X at
@ishrratumar.**
