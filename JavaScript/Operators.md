# Operators in JavaScript
An operator in JavaScript is a unique symbol used to perform operations on operands. Values and variables are the operands.
![operator-operands](javascript-operators.png)
Here you will learn about all the operators in JavaScript.

## Types of operators
There are different types of JavaScript operators, as follows:
- Arithmetic Operators
- Assignment Operators
- Logical Operators
- Comparison Operators
- typeof Operator
- Bitwise Operators
- Conditional Operator (Ternary Operator)
- String Operators

JavaScript Operators Cheatsheet:
![JavasriptOperators](javaScript-operators-cheatsheet.png)
## Arithmetic Operators
Arithmetic Operators are used to perform arithmetic operations on the numbers.

Here's a list of all arithmetic operators in JavaScript:
| Operator | Description                 | Example    |
|----------|-----------------------------|------------|
| +        | Addition                    | 5 + 3      |
| -        | Subtraction                 | 7 - 2      |
| *        | Multiplication              | 4 * 6      |
| **	   | Exponentiation              | x **= y    |
| /        | Division                    | 10 / 2     |
| %        | Modulus (Remainder)         | 10 % 3     |
| ++       | Increment                   | let x = 5; x++; // x will be 6 |
| --       | Decrement                   | let y = 8; y--; // y will be 7 |

## Assignment Operators
Assignment operators are used to assign values to variables. The following operators are known as assignment operators:

| Operator | Description                | Example         |
|----------|----------------------------|-----------------|
| =        | Assign                     | let x = 10;     |
| +=       | Add and assign             | x += 5;         |
| -=       | Subtract and assign        | x -= 3;         |
| *=       | Multiply and assign        | x *= 2;         |
| /=       | Divide and assign          | x /= 4;         |
| %=       | Modulus and assign         | x %= 3;         |
| <<=      | Left shift and assign      | x <<= 2;        |
| >>=      | Right shift and assign     | x >>= 1;        |
| &=       | Bitwise AND and assign     | x &= 3;         |
| \|=       | Bitwise OR and assign      | x \|= 5;        |
| ^=       | Bitwise XOR and assign     | x ^= 7;        |

## Logical Operators
JavaScript uses logical operators to determine if a value is true or false. Logical operators help determine the logic between variables and values.

Here's a list of logical operators:

| Operator | Description            | Example                |
|----------|------------------------|------------------------|
| &&       | Logical AND            | true && false          |
| \|\|      | Logical OR             | true \|\| false        |
| !        | Logical NOT            | !true                  |

## Comparison Operators
A comparison operator also enables you to test whether a value is true or false, in conditional statements.

Here's a list of comparison operators:

| Operator | Description                | Example            |
|----------|----------------------------|--------------------|
| ==       | Equal to                   | 5 == '5'           |
| ===      | Strict equal to            | 5 === 5            |
| !=       | Not equal to               | 10 != '10'         |
| !==      | Strict not equal to        | 10 !== 10          |
| >        | Greater than               | 7 > 3              |
| <        | Less than                  | 2 < 4              |
| >=       | Greater than or equal to   | 5 >= 5             |
| <=       | Less than or equal to      | 10 <= '10'         |
| ?        | Ternary operator           | 10 % 2 === 0 ? true : false|

## typeof Operator
In JavaScript, the `typeof` operator is used to find the data type of a variable or expression.

Example 1: Basic Usage: 
```javascript
const num = 60;
const str = "Hello, world!";
const bool = false;
const obj = { name: "Dani", age: 36 };
const arr = [4, 6, 8];

console.log(typeof num);  // "number"
console.log(typeof str);  // "string"
console.log(typeof bool); // "boolean"
console.log(typeof obj);  // "object"
console.log(typeof arr);  // "object" 
```
**Example 2: Function and undefined:**
```javascript
// 
function name() {
  console.log("Ishrat");
}
console.log(typeof name); // "function"

let someVar;
console.log(typeof someVar); // "undefined"
```

## Bitwise Operators
Bit operators operate on 32-bit numbers.

Any numeric value first gets converted into a 32-bit number. Then the output is converted back into a JavaScript number.

| Operator | Description                   | Example        |
|----------|-------------------------------|----------------|
| &        | Bitwise AND                   | 5 & 3          |
| \|       | Bitwise OR                    | 5 \| 3         |
| ^        | Bitwise XOR                   | 5 ^ 3          |
| ~        | Bitwise NOT (Complement)      | ~5             |
| <<       | Left shift                    | 5 << 2         |
| >>       | Right shift                   | 5 >> 1         |
| >>>      | Zero-fill right shift         | -5 >>> 1       |

## Conditional Operator (Ternary Operator)
✧ Use the ternary operator instead of if-else statements when dealing with simple conditional expressions.

✧ It streamlines your code by evaluating a condition and returning one of two values.

| Operator | Description                   | Example                   |
|----------|-------------------------------|---------------------------|
| ? :      | Ternary (conditional)         | condition ? expr1 : expr2 |

## String Operators
You can use all the Comparison operators listed above on strings. The comparison of strings is done alphabetically. 

| Operator | Description                   | Example        |
|----------|-------------------------------|----------------|
| +        | Concatenation                 | 'Hello, ' + 'World!'  |
| +=       | Concatenate and assign        | let str = 'Hello'; str += ' World!';  |

I really hope you find this short tutorial helpful for understanding different types of JavaScript operators!