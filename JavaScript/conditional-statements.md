# Conditional Statements in JavaScript
Sometimes, depending on the condition, you might want to perform different actions. To do this, you can use conditional statements in JavaScript.

The following are different of conditional statements:

- if
- else
- else-if
- switch
- ternary operator

## if
The `if` statement is used to write a block of code that will run only if a certain condition is true.

**Syntax:**
```javascript
if (condition) {
  // block of code
}
```
**Example**
```javascript
let result;
if (50 > 5) {
  result = "Yes, 50 is greater than 5!";
}
console.log(result); // Output: "Yes, 50 is greater than 5!"
```

## else
The `else` statement is used to write a second block of code that will run if the condition is false.

**Syntax:**
```javascript
if (condition) {
  // execute if the condition is true
} else {
  // execute if the condition is false
}
```
**Example:**
```javascript
let result;
if (5 > 50) {
  result = "Yes, 5 is greater than 50!";
} else {
  result = "No, 5 is less than 50!";
}
console.log(result); // Output: "No, 5 is less than 50!"
```
## else-if
The `else-if` statement is used to test a different condition if the first condition is false.

**Syntax:**
```javascript
if (condition-01) {
  // execute if the condition-01 is true
} else if (condition-02) {
  // execute if the condition-01 is false and condition-02 is true
} else {
  // execute if the condition-01 and condition-02 are false
}
```
**Example:**
```javascript
let score = 95;

if (score >= 95) {
  console.log("Excellent! You got an A.");
} else if (score >= 85) {
  console.log("Good job! You got a B.");
} else if (score >= 75) {
  console.log("Not bad! You got a C.");
} else {
  console.log("You need to study harder.");
}
```
Since we have a variable called `score` with a value of 95, the condition `score >= 95` is true, and the output will be "Excellent! You got an A.". 

If that isn't the case, it will continue to check until it finds a true condition and then execute it. The `else` statement will be executed if there are no true conditions.
## switch
The `switch` statement compares an expression against a set of different cases and executes code based on the matching cases.

**Syntax:**
```javascript
switch (expression) {
    case value1:
        // execute if expression matches value1
        break;
    case value2:
        // execute if expression matches value2
        break;
    // ... more cases ...
    default:
        // execute if none of the cases match the expression
}
```
**Example:**
```javascript
let favLanguage = 3;
let langName;

switch (favLanguage) {
  case 1: langName = "Java"; break;
  case 2: langName = "C++"; break;
  case 3: langName = "JavaScript"; break;
  case 4: langName = "Swift"; break;
  case 5: langName = "PHP"; break;
  case 6: langName = "Go"; break;
  case 7: langName = "Python"; break;
  default: langName = "Unknown"; break;
}
console.log("Your favorite language is " + langName);
```
The given JavaScript code uses a switch statement to determine the language name based on the value of the favLanguage variable. When favLanguage equals 3, it sets "JavaScript" to langName and stops using the break statement. When no case matches, "Unknown" is assigned as a default. 

In this example, the output will be "Your favorite language is JavaScript.".
## Conditional Operator (Ternary Operator)
The `ternary operator` is shorthand for writing if-else statements.

✧ Use the ternary operator instead of `if-else` statements when dealing with simple conditional expressions. 

✧ It streamlines your code by evaluating a condition and returning one of two values.

**Syntax:**
```condition ? expr1 : expr2```

**Example:**
```javascript
const isGoingOut = true;

let answer = isGoingOut ? "Yes" : "No";
```

That's pretty much it for today. I really hope you find this helpful. Thank you for reading!