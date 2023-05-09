# HTML Form Validations

A valid HTML form ensures that the user's input meets the required criteria and is correct. Using HTML attributes for form validation or JavaScript for more complex logic will let you implement more sophisticated validation logic. It is also important to provide meaningful error messages to the user and perform server-side validation. You can create secure and user-friendly web forms using these techniques.

## HTML Input Attributes: 
     -> required
     -> type
     -> pattern
     -> max & min
     -> maximum & minimum

### required attribute
It is a boolean attribute that assures that an input field must be filled out before submitting the form. It supports text, password, radio, checkbox, date pickers, number, file, email, tel, URL, and search input types.

Example:

```
<form>
Username: <input type="text" name="username" required />
<input type="submit" />
</form>
```

### type attribute
This attribute specifies the type of input expected from the user. You can use the 'type' attribute for many kinds of input fields, including text, password, email, number, checkbox, radio, date, file, submit, reset, button, etc. The example below shows how to specify a type attribute that ensures that the user enters the right email address in the specific input field.

Example:
```
<input type="email" name="email" />
```

### pattern attribute
You can specify a regular expression that the user's input must match using this attribute.

Example:
```
Email:<input type="email" name="email" required pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$" />
```

### max & min attribute
You can use these attributes to specify the maximum and minimum values that can be entered in a numeric input field.

Example:
```
Age:<input type="number" name="age" id="age" min="18" max="99" required />
```

### maximum & minimum
These attributes work similarly to `max` and `min`, but are used for date and time input fields.

Example: 
```
<label for="birthdate">Birthdate:</label>
<input type="date" name="birthdate" id="birthdate" minimum="2001-01-01" maximum="2023-05-09" required />
```

## CSS Pseudo Selectors
CSS pseudo-selectors make it possible to select elements and style them based on their state or attributes. Following is a list of frequently used CSS form input pseudo-selectors:

       -> :required
       -> :valid
       -> :invalid 
       -> :disable
       -> :optional

### :required selector
This pseudo-selector is used to select and style form elements that have the required attribute, such as input fields. The code given below will set the border color of all required input fields to red.

Example:
```
input:required {
  border-color: red;
}
```

### :valid selector
This pseudo-selector is used to select and style form elements that are valid, such as input fields with valid values. The code given below will set the border color of all valid input fields to green.

Example:

```
input:valid {
  border-color: green;
}
```

### :invalid selector
This pseudo-selector is used to select and style form elements that are invalid, such as input fields with invalid values. The code given below will set the border color of all invalid input fields to red.

Example:
```
input:invalid {
  border-color: red;
}
```

### :disable selector
This pseudo-selector is used to select and style form elements that are disabled, such as input fields with disabled attributes. The code given below will set the opacity of all disabled input fields to 0.5.

Example:
```
input:disabled {
  opacity: 0.5;
}
```

### :optional selector
This pseudo-selector is used to select and style form elements without required attribute. The code given below will set the background color of all optional input fields to light gray.

Example:
```
input:optional {
  background-color: lightgray;
}
```
## Form
### HTML

```
<!DOCTYPE html>
<html>
<head>
  <title>Example Form</title>
</head>
<body>
  <form>
  <h1>Contact Form</h1>
    <label for="username">Username:</label>
    <input type="text" name="username" required pattern="[a-zA-Z0-9]{5,}" />
    <br />
    
    <label for="email">Email:</label>
    <input type="email" name="email" required />
    <br />
    
    <label for="password">Password:</label>
    <input type="password" name="password" required pattern="^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{8,}$" />
    <br />
    
    <label for="age">Age:</label>
    <input type="number" name="age" min="18" max="99" />
    <br />
    
    <label for="color">Favorite color:</label>
    <input type="color" name="color" />
    <br />
    
    <label for="comments">Comments:</label>
    <textarea name="comments" rows="4" cols="40"></textarea>
    <br />
    
    <input type="submit" />
  </form>
</body>
</html>
```

### CSS

```
form {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
  max-width: 400px;
  margin: 0 auto;
  padding: 1rem;
  border: 1px solid #ccc;
  border-radius: 8px;
}
h1 {
    text-align: center;
}

label {
  font-weight: bold;
}

input[type="text"],
input[type="email"],
input[type="password"],
select {
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
  font-size: 1rem;
}

input[type="text"]:focus,
input[type="email"]:focus,
input[type="password"]:focus,
select:focus {
  outline: none;
  border-color: blue;
}

input[type="submit"] {
  padding: 0.5rem 1rem;
  background-color: blue;
  color: white;
  border: none;
  border-radius: 4px;
  font-size: 1rem;
  cursor: pointer;
}

input[type="submit"]:hover {
  background-color: darkblue;
}

input:required:invalid,
select:required:invalid {
  border-color: red;
}

input:required:valid,
select:required:valid {
  border-color: green;
}

input:disabled,
select:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
```

⭐ Check out these resources if want to learn more: [W3Schools](https://www.w3schools.com/js/js_validation.asp)
, [WEBDEV](https://web.dev/learn/forms/)
and [MDN](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)

