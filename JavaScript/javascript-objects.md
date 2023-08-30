# Objects in JavaScript
Objects are collections of `key: value` pairs. These are also called properties.

JavaScript objects enable you to store, manipulate, and send data across a network. 

In objects, you can store in-depth, composite/complex data.

## Create objects
In JavaScript, creating an object is quite easy. To create an object, all you need is a set of curly braces `{ }` and within that, you have to write `key: value` pairs separated with a comma `,`. 

Here's an example to understand it better:

```javascript
let blogPost = {
    title: "Objects in JavaScript",
    author: "Jane Doe",
    date: "August 10, 2023",
    content: "Objects are collections of 'key: value' pairs...",
    tags: ["JavaScript", "Web Development"]
};

console.log(typeof blogPost); // Output: object
```

**Note:** You can also create an object using the `new` keyword. You need to have a constructor function to create an object using the `new` keyword.

To create an object, use the `new` keyword with `Object()` constructor, like this:
```
const person = new Object();
```

To add properties to this object, we can do the following:

```javascript
person.firstName = 'Jane';
person.lastName = 'Doe';
```

Objects can also be created with [Object.create()](https://medium.com/r/?url=https%3A%2F%2Fdeveloper.mozilla.org%2Fen-US%2Fdocs%2FWeb%2FJavaScript%2FReference%2FGlobal_Objects%2FObject%2Fcreate).

If you need to access any of the object's properties. The value of a property can be accessed by using its `key`. There are two methods to access the object's properties:

## The dot notation
This is the most commonly used method.

```javascript
console.log(blogPost.title); // Output: Objects in JavaScript
```

## The bracket notation
You can use bracket notation to replace the dot(`.`) with square brackets `[]` and then convert the `key` name to a `string`. 

**Example:**
```javascript
console.log(blogPost["title"]); // Output: Objects in JavaScript
```

## Nested objects
The object within an object is called a nested object.

Here's an example:

```javascript
let blogPost = {
    title: "Objects in JavaScript",
    author: "Jane Doe",
    date: "August 10, 2023",
    content: "Objects are collections of 'key: value' pairs....",
    tags: ["JavaScript", "Web Development"],
    details: {
        language: "English",
        platform: "Medium"
    }
};

// Access properties of the main object
console.log(blogPost.title); // Output: Objects in JavaScript
console.log(blogPost.details); // {language: English, platform: Medium}

// Access properties of the nested object
console.log(blogPost.details.language); // Output: English
console.log(blogPost.details.platform); // Output: Medium
```

## Object methods
In JavaScript, creating functions within objects is referred to as methods.

**Example:**
```javascript
let player = {
    name: "Joe",
    score: 200,
    greet: function() {
        console.log("Hey!");
    }
};
```

Here's how you can invoke this function:

```javascript
player.greet(); // Output: Hey!
// player is an object and greet is a function on that object, also called a method
```

## Shorthand(ES6)
When you want to create an object with properties directly from existing variables, you can use the property shorthand.

**Example:**
```javascript
const title = "Objects in JavaScript";
const date = "August 10, 2023";
const author = "Jane Doe";
const language = "English";
const platform = "Medium";

const blogPost = {
    title,
    date,
    author,
    details: {
        language,
        platform
    }
};

console.log(blogPost.title); // Output: Objects in JavaScript
console.log(blogPost.date); // Output: August 10, 2023
console.log(blogPost.author); // Output: Jane Doe
console.log(blogPost.details.language); // Output: English
console.log(blogPost.details.platform); // Output: Medium
```

## Object destructuring(ES6)
JavaScript has a nice feature called object destructuring that lets you extract properties from objects and bind them to variables. 
It is capable of extracting many properties in one statement, accessing properties from nested objects, and setting a default value in the absence of a property.
**Syntax:**
```javascript
const { property } = object;
```

**Example:**
```javascript
const blogPost = {
    title: "Objects in JavaScript",
    date: "August 10, 2023",
    author: "Jane Doe",
    details: {
        language: "English",
        platform: "Medium"
    }
};

const { title, date, author, details } = blogPost;

console.log(title);            // Output: Objects in JavaScript
console.log(date);             // Output: August 10, 2023
console.log(author);           // Output: Jane Doe
console.log(details.language); // Output: English
console.log(details.platform); // Output: Medium
```

**That's pretty much it for today! I really hope you find this helpful to better understand objects in JavaScript.**
