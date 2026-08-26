# Working With APIs in JavaScript

Modern web apps rarely work alone. Your frontend might need to:

- Load user data
- Create accounts
- Submit forms
- Fetch products
- Send payments
- Update information
- Talk to third-party services

This is where APIs come in. An API gives your JavaScript application a way to communicate with a remote server.

But how do you actually make those requests? JavaScript gives you two native ways:

- `XMLHttpRequest`
- `fetch()`

Let's break down how they work.

## What an API Request Actually Does

Imagine your JavaScript app needs a list of users. Your app sends an HTTP request to an API endpoint:

```text
GET /api/users
```

The server receives the request, processes it, and sends something back. Usually, that response is JSON:

```json
[
  {
    "id": 1,
    "name": "Alex"
  }
]
```

Your JavaScript can then use that data to update the page.

## The Four Pieces of an API Request

There are usually four important pieces to an API request.

**1. URL** — Where you're sending the request.

```text
https://api.example.com/users
```

**2. HTTP method** — What you want to do. Common methods include:

- `GET` → retrieve data
- `POST` → create data
- `PUT` → replace data
- `PATCH` → update data
- `DELETE` → remove data

**3. Headers** — Additional information about the request.

**4. Body** — The data you're sending to the server.

## The Older Approach: `XMLHttpRequest`

`XMLHttpRequest` has been part of browsers for a long time and is still supported. A basic GET request looks like this:

```js
const xhr = new XMLHttpRequest();

xhr.open(
  "GET",
  "https://api.example.com/users"
);

xhr.onload = () => {
  console.log(xhr.responseText);
};

xhr.send();
```

It works. But there's quite a bit happening here.

You first create an `XMLHttpRequest` object. Then you call `xhr.open()`, which configures the request. You provide:

- HTTP method
- API URL

Then you define what should happen when the request finishes. Finally, `xhr.send()` actually sends the request.

`XMLHttpRequest` can also handle errors and different request states. For example:

```js
xhr.onerror = () => {
  console.log("Network error");
};
```

You can also listen for changes in the request's state. This flexibility is one reason XHR became so widely used. But modern JavaScript introduced a much cleaner alternative.

## The Modern Approach: `fetch()`

Fetch provides a modern interface for making HTTP requests. A simple GET request looks like this:

```js
fetch("https://api.example.com/users")
  .then(response => response.json())
  .then(data => {
    console.log(data);
  });
```

Notice how much simpler this feels. You provide the URL, Fetch sends the request, then you handle the response.

### Fetch Returns a Promise

That means you can use `.then()` and `.catch()`.

```js
fetch("/api/users")
  .then(response => response.json())
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error(error);
  });
```

The first `.then()` receives the response. The second receives the parsed JSON data.

## Using `async/await`

This is probably the syntax you'll see most often in modern JavaScript. Instead of chaining multiple `.then()` calls, you can write:

```js
async function getUsers() {
  const response = await fetch(
    "/api/users"
  );

  const data = await response.json();

  console.log(data);
}
```

This reads almost like normal synchronous code.

There are two important things to notice here:

- `await fetch("/api/users")` waits for the HTTP response and gives you a `Response` object.
- `await response.json()` parses the response body as JSON and gives you the actual data.

These are separate operations.

## Sending Data With `POST`

Suppose you want to create a new user. You'd normally use a `POST` request. With Fetch:

```js
const response = await fetch("/api/users", {
  method: "POST",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    name: "Alex",
    email: "alex@example.com"
  })
});
```

A few important details:

- The `method` tells the server what you're doing (`method: "POST"`).
- The `Content-Type` header tells the server what format you're sending (`"Content-Type": "application/json"`).
- `JSON.stringify()` converts your JavaScript object into a JSON string, which is what gets sent in the request body.

## Adding Authentication Headers

For example:

```js
const response = await fetch("/api/users", {
  headers: {
    Authorization: `Bearer ${token}`
  }
});
```

This is common when APIs require authentication. The exact system depends on the API. It might use:

- Bearer tokens
- API keys
- Cookies
- OAuth

Always follow the API's documentation.

## Handling Errors

Here's something beginners often miss. `fetch()` does **not** automatically throw an error when the server returns `404` or `500`. The request itself may have completed successfully from Fetch's perspective.

So you should check `response.ok`:

```js
if (!response.ok) {
  throw new Error("Request failed");
}
```

A more complete function looks like:

```js
async function getUsers() {
  const response = await fetch("/api/users");

  if (!response.ok) {
    throw new Error(
      `HTTP error: ${response.status}`
    );
  }

  return response.json();
}
```

### Inspecting Status Codes

You can also inspect the status code directly:

```js
console.log(response.status);
```

Common status codes:

```text
200 → Success
201 → Created
400 → Bad request
401 → Unauthorized
403 → Forbidden
404 → Not found
500 → Server error
```

Understanding status codes makes debugging API problems much easier.

## `DELETE` and `PATCH`

`DELETE` is straightforward:

```js
await fetch("/api/users/123", {
  method: "DELETE"
});
```

You're telling the server: "Delete the resource with ID 123."

For updates, you might use `PATCH`:

```js
await fetch("/api/users/123", {
  method: "PATCH",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    name: "Sam"
  })
});
```

## CORS

Sometimes your frontend and API are running on different origins. For example:

```text
Frontend:
https://myapp.com

API:
https://api.example.com
```

The browser may enforce Cross-Origin Resource Sharing rules. The API server needs to allow your frontend's origin when appropriate. This isn't something you can simply fix by changing your JavaScript request.

## Loading States

An API request isn't instant. Your UI shouldn't just sit there looking broken. You might show:

```text
Loading...
```

Then:

```text
Users loaded
```

Or:

```text
Something went wrong
```

A good API integration handles three states: 

**Loading → Success → Error**. 

This pattern appears everywhere in frontend development.

## Reusable Functions

You don't want to repeat API logic throughout your application. Instead of writing `fetch("/api/users")` everywhere, you can create reusable functions:

```js
async function getUsers() {
  const response = await fetch("/api/users");

  if (!response.ok) {
    throw new Error("Failed to fetch users");
  }

  return response.json();
}
```

Then your components can simply call:

```js
const users = await getUsers();
```

Cleaner code.

## `XMLHttpRequest` vs `fetch()`

Both can communicate with remote APIs. But for most modern JavaScript applications, `fetch()` is the natural choice:

- It's built into modern environments.
- It works with Promises.
- It works nicely with `async/await`.
- Its API is much easier to work with.

## The Bigger Idea

The bigger idea is more important than memorizing syntax. When your application works with an API, think about the complete flow:



That's the basic request-response cycle behind countless web applications.

## Learn the Fundamentals

You don't need to memorize every endpoint or HTTP method. Learn the fundamentals:

- HTTP methods
- URLs
- Headers
- Request bodies
- JSON
- Promises
- `async/await`
- Response status codes
- Error handling
- CORS
- Authentication

Then start calling real APIs.

## Start Small

Build a tiny app that:

- Fetches a list of users
- Displays them
- Adds a new user
- Updates a user
- Deletes a user
- Handles loading
- Handles errors

You'll learn far more by making those requests yourself than by only reading about them.

APIs are one of the core building blocks of modern web development. And `fetch()` is one of the most useful JavaScript tools to know.
