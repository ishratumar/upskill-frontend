# HTML Best Practices

This document contains some HTML best practices that you should follow while 
writing HTML to keep your HTML documents organized and consistent.

## 1. Document Structure
It's important to follow the proper document structure, even though your code will still work even without it. 
But in some browsers, the pages will not render correctly.

Best Practice:
```
<!DOCTYPE html>
<html>
    <head>
        <title>Page title</title>
    </head>
    <body>
        <!-- page content -->
    </body>
</html>
```
## 2. Correct DOCTYPE
When writing HTML, the first thing you have to write is the doctype. This will tell the browser the standards you are using to 
render your markup correctly. The doctype goes before the <html> tag at the top of the page.
If you are unsure about what declaration to use, W3.org provides information on choosing the right doctype.
  
```
<!DOCTYPE html>
<html>
    <head>
        <title>Page title</title>
    </head>
    <body>
        <!-- page content -->
    </body>
</html>
```
  ## 3. Page language
Specifying the language of your site will help screen readers pick the right language to announce. Browsers also use 
it to determine if they should auto-translate your site or not.
The lang attribute should describe the language used by the majority of the content of the site.
  
  ```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Page title</title>
    </head>
    <body>
        <!-- page content -->
    </body>
</html>
```
  ## 4. Always close or self-close the tags
    To avoid encountering validation errors, always remember to have a closing tag for every tag you create.
  ```
  <h1>Heading 1</h1>
  <p>Paragraph Text</p>
  <img src="example.jpg" alt="Example Image" />
  ```
  ## 5. Don't use inline styles
It may seem like an easy route to place styling in line with the code instead of creating an external style sheet. However, inline styles are not a good coding practice because it makes it harder to update and maintain a website.
Instead, keep your styles separate from your HTML mark-up.

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page title</title>
        <link rel="stylesheet" href="styles.css">
    </head>
    <body>
        <!-- page content -->
    </body>
</html>
  ```
## 6. Always Specify alt, width, and height for Images
It is not required to have an alt attribute with images, which makes it easy to ignore. However, it is important to have a 
  meaningful alt attribute for validation and accessibility reasons.
The alt attribute provides context to screen readers so it should be descriptive as to what the image contains.

```
<img src="image.jpg" alt="a descriptive text">
  ```
## 7. Validate frequently
Instead of waiting until you are finished with your HTML document, validate your code multiple times as you work. This will help 
save some time in the end by identifying errors early on, especially if your document is lengthy.
One popular HTML validator to use is W3C’s markup validation service.

## 8. Place external style sheets within the <head> tag
Although external style sheets can be placed anywhere in the HTML document, it is best practice to place them within the <head> tag. 
  This will allow your page to load faster.  
```
<!DOCTYPE html>
<html>
    <head>
        <title>Page title</title>
        <link rel="stylesheet" href="styles.css">
    </head>
    <body>
        <!-- page content -->
    </body>
</html>
  ```
  ## 9. Avoid Excessive Comments
  ```
  <!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>Heading 1</h1>
    <!-- This is a comment that is not needed -->
    <p>Paragraph Text</p>
  </body>
</html>
```
  ## 10. Use Fieldset and Labels in Web Forms
  ```
  <form>
  <fieldset>
    <legend>Personal Details</legend>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
    <label for="message">Message:</label>
    <textarea id="message" name="message"></textarea>
  </fieldset>
</form>
```
  ## 11. Use lowercase markup
  ```
  <h1>Heading 1</h1>
  <p>Paragraph Text</p>
  <img src="example.jpg" alt="Example Image">
```
  ## 12. HTML5 Semantic Elements
The term refers to elements with meanings. 100s of semantic elements are available. When written in semantic tags, your content will
  be considered important by search engines, which will boost your SEO.
  
  ![FUE0KjXUEAALMtd](https://user-images.githubusercontent.com/47534248/236609875-6028ef12-e378-4e6c-a853-77ea5cbfbbc3.jpg)

  ## 13. Use meaningful tags
  ```
  <header>
  <h1>Page Title</h1>
</header>
<nav>
  <ul>
    <li><a href="#">Link 1</a></li>
    <li><a href="#">Link 2</a></li>
    <li><a href="#">Link 3</a></li>
  </ul>
</nav>
<main>
  <article>
    <h2>Article Title</h2>
    <p>Article Text</p>
  </article>
  <section>
    <h2>Section Title</h2>
    <p>Section Text</p>
  </section>
</main>
<footer>
  <p>Footer Text</p>
</footer>
```
  ## 14. Keep SEO in mind
  Read this detailed thread on [SEO tags for HTML](https://twitter.com/ishratUmar18/status/1531562660357021696?s=20).
  
  ## 15. Always use responsive meta tags
  You should always make your site responsive. Now people can request a desktop or mobile experience through the browser and the
  minimum you can do is make your site fluid but, responsiveness is a must.
    
```
    <meta name="viewport" content="width=device-width, initial-scale=1">
```
  ## 16. Lazy load Images 
  Lazy loading images make them load faster, as only the images within the viewport are initially loaded.
 ```
    <img src="image.jpg" loading="lazy">
 ```
    
   ## 17. Put social links inside the ```<address>```
    
  
  Use the [address](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/address) tag to include any information about how people     can contact you, such as your mailing address, phone number, email address, website, and social network links (if applicable).
    
    ## 18. Add captions to images
  Use <figcaption> along with <figure> element to add captions to your images.
    
    
```<figure>
     <img src="image.jpg" alt="A beautiful landscape">
      <figcaption>A beautiful landscape</figcaption>
    </figure>```
    

    
  
   
