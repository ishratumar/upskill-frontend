# Print Hello World
Here you will learn how to print 'Hello World' in JavaScript.
JavaScript allows you to either include your code internally in an HTML file or externally in a different JavaScript file.
## 1. Internal JavaScript 
In this method, using the `<script>` tags, you write your JavaScript code directly into the HTML document.
## 2. External JavaScript
With this technique, you create a separate JavaScript file with the `.js` extension and link it to the HTML file.
To add the path to the external JavaScript file, use the `<script>` tag with the `src` attribute.
## Steps to follow:
Open your preferred code editor, such as Visual Studio Code. Make a file with the extension `.html` such as `index.html`.

### HTML file:
1. The first step is to open the file.
2. Insert a `<script>` tag within the `<body>` tag.
3. In the `<script>` tag, write your JavaScript code using the `console.log` to observe the result.
Example:
```
<body>
<script>
  console.log("Hello, World!");
</script>
</body>
```
4. Save the file, then.
5. Open a web browser and view it. To see the result, open the browser's developer console (such as using the browser's developer tools).
### JavaScript file:
1. First of all, create a JavaScript file(script.js) and open it.
2. Write your JavaScript code directly in the file using `console.log` for output.
Example:
```
  console.log("Hello, World!");
```
3. Then save the JavaScript file.
4. Create a new HTML file(index.html) and open it.
5. Add a `<script>`` tag with the `src` attribute inside the `<body>` tag that points to the JavaScript file.

Example:
```
<body>
  <script src="script.js"></script>
</body>
```
6. Then save the file.
7. Open the HTML file in a web browser, or run the code by clicking the Live Server extension in Visual Studio Code. This will run the code in the browser. With this extension, you will not have to repeatedly refresh the page to see results. It syncs changes immediately after you save the file and displays them in the browser. To view the output, open the browser's developer console.

You can use `console.log` to see JavaScript output by following these simple steps either directly in an HTML file or using the external JavaScript file method.