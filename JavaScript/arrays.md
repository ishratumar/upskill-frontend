# Arrays in JavaScript

In JavaScript, arrays are ordered lists. A single variable called an array is used to hold various elements. It is frequently used if we need to store a list of elements and access them using a single variable.

## Create an Array
The simplest way to create an Array is to use an Array literal.

**Example:**
```javascript
let arr = [10, 20, 30] ;
```

## Accessing Array Elements
The values in an array are referred to as elements. Utilizing the index number, you can get to a specific array element. Arrays are 0 indexed. In other words, you would use the 0 index to access the first item in the list. 

See the illustration below:
![javascript-arrays](/assets/javascript-arrays.png)

**Example:**
```javascript
let arr = [10, 20, 30];
console.log(arr[0]); // Output: 10
```
You can access the whole array by referring to the array name:
**Example:**
```javascript
let arr = [10, 20, 30];
console.log(arr); // Output: [10, 20, 30 ]
```

There are several built-in methods that make arrays in JavaScript real strong.
## .length property
To find out how many elements are in an array, you can use the .length property.

**Example:**
```javascript
let arr = [10, 20, 30];
console.log(arr.length); // Output: 3
```

Using the .length property, you can find out the index of the last element of the array.
**Example:**
```javascript
let arr = [10, 20, 30];
console.log(arr.length-1); // Output: 2
```
Here's how to find out what the last element of the array is using the .length property.
```javascript
console.log(arr[arr.length - 1]); // Output: 30
```
## Arrays with multiple datatypes 
There is no limit to what data types you can use and how much you can mix. Arrays are composed of different data types and their values. An array is a list of ordered items that consist of composite and complex data types.

**Example:**
```javascript
const mixedArray = [42, 'hello', true, [1, 2, 3], { name: 'John', age: 30 }];

console.log(mixedArray[0]); // Output: 42 (number)
console.log(mixedArray[1]); // Output: hello (string)
console.log(mixedArray[2]); // Output: true (boolean)
console.log(mixedArray[3]); // Output: [1, 2, 3] (array)
console.log(mixedArray[4]); // Output: { name: 'John', age: 30 } (object)

```

## List of JavaScript Array Methods
Here's a list of array methods in JavaScript:
How to add and remove elements from an Array?
You can use push to add an element and pop method to remove an element.

`push`: adds an element at the end of the array of elements.
```javascript
let arr = [10, 20, 30];
console.log(arr.push(40)); 
console.log(arr); // Output: [10, 20, 30, 40]
```
`pop`: is the opposite of push. It removes the last element in the array. 
```javascript
let arr = [10, 20, 30];
console.log(arr.pop()); // Output: 30
console.log(arr); // Output: [10, 20]
```
`concat`: combines the elements of two arrays and returns a new array.
**Example:**
```javascript 
const blogPosts1 = [
  { title: 'Intro to JS', author: 'Alice' },
  { title: 'CSS Styling', author: 'Bob' }
];

const blogPosts2 = [
  { title: 'APIs in JS', author: 'Charlie' },
  { title: 'Web Dev Best Practices', author: 'David' }
];

const allBlogPosts = blogPosts1.concat(blogPosts2);

console.log(allBlogPosts);
```
**Output:**

```
// [object Array] (4)
[// [object Object] 
{
  "title": "Intro to JS",
  "author": "Alice"
},// [object Object] 
{
  "title": "CSS Styling",
  "author": "Bob"
},// [object Object] 
{
  "title": "APIs in JS",
  "author": "Charlie"
},// [object Object] 
{
  "title": "Web Dev Best Practices",
  "author": "David"
}] */
```

**Note:** Another option for concatenating arrays is to use the spread operator, which is a more convenient and simple method. 

```javascript
const allBlogPosts = [...blogPosts1, ...blogPosts2];
```

**reverse:** returns a copy of an array in the opposite order.

**Example:**
```javascript
let arr = [10, 20, 30];
console.log(arr.reverse()); // Output: [30, 20, 10]
```


Although it isn't very common method to use, I just wanted to give you a sneak peek in case you run into it during your web development journey.
![javascript-arrays-methods-cheatsheet](/assets/javascriparray-methods.png)

I really hope you find this short tutorial helpful for understanding arrays in JavaScript! 

#### If you like it, give it a ⭐!


