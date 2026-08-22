# What is the purpose of `this` in JavaScript?

The `this` keyword is one of those JavaScript concepts that looks simple but often causes confusion.

At its core, `this` refers to the context in which a function is called.

The important part is:

> `this` is determined by how a function is called, not where it is defined.



Here are the common cases:

## 1. Inside an object method

```js
const user = {
  name: "Ishrat",
  greet() {
    console.log(this.name);
  }
};

user.greet(); // Ishrat
```

Here, `this` refers to the `user` object.

## 2. Inside a regular function

In non-strict mode, `this` can refer to the global object.

In strict mode:

```js
"use strict";

function greet() {
  console.log(this);
}

greet(); // undefined
```

## 3. Inside an event handler

```js
button.addEventListener("click", function () {
  console.log(this);
});
```

Here, `this` refers to the element that triggered the event.

## 4. Arrow functions are different

Arrow functions don't have their own `this`.

They inherit `this` from their surrounding scope.

```js
const user = {
  name: "Ishrat",
  greet: () => {
    console.log(this.name);
  }
};

user.greet(); // undefined
```

This is one reason you should be careful when using arrow functions as object methods.

## The key takeaway

Don't memorize "`this` always means the current object."

Instead, ask:

> "How was this function called?"

That usually tells you what `this` refers to.

Understanding `this` makes objects, event handlers, classes, callbacks, and frameworks like React much easier to reason about.
