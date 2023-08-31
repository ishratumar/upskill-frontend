# Template Literals: A More Readable Way to Create Strings

When it comes to writing strings or embedding expressions in JavaScript, template literals offer an elegant alternative that enhances both conciseness and readability.

## Utilizing Template Literals
When creating a template literal in JavaScript, replace the single **(' ')** or double quotes **(" ")** with backticks **(` `)**. These backticks allow you to use `${}`—a handy syntax for embedding variables and expressions within your string.

**Example:**
```javascript
const name = 'Joe';
const job = 'Software Developer';
const age = 25;
const intro = `My name is ${name}, I'm ${age} years old, and I'm a ${job}.`;

console.log(intro); 
// Output: My name is Joe, I'm 25 years old, and I'm a Software Developer.
```

As demonstrated, the `${}` syntax allows you to neatly insert variables like name, job, and age into the string. When compared to the traditional concatenation of strings using the `+` operator, this approach improves code readability and conciseness.

## String Interpolation
Interpolation is the technique of interpolating variables and expressions into strings. 

Prior to JavaScript ES6, the `+` operator was the go-to for string concatenation involving variables and expressions.

**Example:**
```javascript
const name = 'Joe';
console.log('Hey' + name);
```

With template literals, however, interpolating variables and expressions into strings becomes significantly easier.

**Example:**
```javascript
const name = 'Joe';
console.log(`Hello ${name}`);
```

## Handling Multiple Strings
Another advantage of using JavaScript Template Literals is that you can create multiline strings without using escape characters. To achieve this effect, insert line breaks directly within the backticks.

**Example using escape characters:**
```javascript
// Combining strings using the + operator
const introduction = "Hello there! My name is\n" +
  "John, and I wanted to share a little bit\n " +
  "about myself with you. I enjoy coding.";

console.log(introduction);
```

**Example using template literals:**

```javascript
// Combining strings using template literals
const introduction = `
Hello there! My name is 
John, and I wanted to share a little bit
about myself with you. I enjoy coding.
`;

console.log(introduction);
```

## Template Literals with Functions
JavaScript Template Literals can also be used with functions to create dynamic strings based on function parameters. Typically, a function accepts arguments as input.

**Example:**
```javascript
function greet(name){
  return name;
}

// pass arguments
const result = greet('Joe');

console.log(result);
```

## Tagged Templates
Template literals can be used to create tagged templates that work as functions. Use these tags to parse template literals into functions.

**Example:**
```javascript
const greet = (name) => `Hello ${name}, How are you doing?`;

const taggedGreet = greet`Joe`;

console.log(taggedGreet); // Output: Hello Joe, How are you doing?
```
In the above example, the `taggedGreet` variable is a `tagged template` that calls the `greet` function with the name "Joe" as an argument.

That's a wrap! I really hope you find it helpful. If you have any question message me on [Twitter](https://twitter.com/ishrratumar). If you find a typo or want to improve this topic feel free to contribute to this repository.

