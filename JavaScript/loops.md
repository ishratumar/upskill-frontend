# Loops in JvaScript
Loops in any programming language are used to run a piece of code repeatedly. Using loops, you can run the same code with different values repeatedly without writing the instructions again and again.

Types of loops in JvaScript:
✧ for loop
✧ while loop
✧ do while loop
✧ for...of loop
✧ for...in loop


## for loop
For loop, it works best when you know how many iterations will be required in advance.

There are three parts of for-loop:
1. initialization to declare or initialize a variable.
2. condition to determine whether the loop will keep executing; if the condition is false, the loop will be terminated.
3. increment and decrement refer to the change in the value of a variable.

When a condition is true, the code inside the loop will execute.

**Syntax:**
```javascript
for (initialization; condition; increment/decrement) {
// Code to be executed in each iteration
}
```

**Example:**
Here's an example of for loop to print even numbers from 0 to 20
```javascript
for (let i = 2; i <= 20; i += 2) {
console.log(i);
}
```
# while loop
In  a `while loop``, you execute a block of code repeatedly as long as a certain condition is true.

The `while loop`` works well when the number of iterations is unknown.

It starts by checking whether the condition is true; if it is, the while loop's code block is then executed, and the process is repeated until the condition is true.

**Example:**
```javascript
let i = 0;
while (i < 5) {
// Code to be executed in each iteration
i++;
}
```
## for-loop vs. while-loop
One key difference between `for-loop` and `while-loop` is that `while-loop` is used when you do not know how many iterations are required. 

On the other hand, `for-loop` works best when you know how many iterations will be required in advance.

# do while loop
If you want to run the code block at least once before checking the condition, use `do-while`` loop.

After the first iteration, if the condition is true, the loop continues to iterate until the condition is false, at which point it terminates.

**Example:**
```javascript
let i = 0;
do {
// Code to be executed in each iteration
i++;
} while (i < 5);
```
# for...of loop
The `for...of` loop is used to repeatedly iterate over and perform some action on each value of an iterable object, such as an array, a string, or a NodeList.

**Syntax:**
```javascript
for (variable of iterable) {	
// block of code to be executed
}
```
**Example:**
Hera's an example how you can use it.

If you were a chef, you might have a variety of ingredients for a special recipe. You must make a list of every ingredient you will need to purchase and include it in your shopping list.

```javascript
const ingredients = ["flour", "eggs", "milk", "sugar"];
console.log("Shopping List:");
for (const ingredient of ingredients) {
console.log(`- ${ingredient}`);
}
```

# for...in loop
The `for...in` loop is used to iterate through all of an object's enumerable property keys.

**Syntax:**
```javascript
for ( variable in object ){
// block of code to be executed
}
```
**Example:**
Hera's an example how you can use it.
If you are a developer working on a project, you might have an object that lists different tasks and their current states.
```javascript
const tasks = {
"task1": "completed",
"task2": "in progress",
"task3": "not started",
};
for (const taskName in tasks) {
const status = tasks[taskName];
console.log(`Task ${taskName} is ${status}.`);
}
```
**Key points:**
- for...of is for objects and it returns values
- for...in is for iterables and it returns object indices

That's pretty much it for today. I really hope you find this helpful. 

Needs some improvements? Feel free to contribute to this repository.