# HTML Best Practices

This document contains some HTML best practices that you should follow while 
writing HTML to keep your HTML documents organized and consistent.

## 1. Document Structure
The proper document structure should be used, even if your code would still work without it. But some browsers might not display the pages properly.

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
When writing HTML, the doctype is the first thing you have to write. This will let the browser know what standards you're using to render markup correctly. The doctype tag precedes the `<html>` tag at the top of the page.
  
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
Screen readers will be able to select the appropriate language to announce if you specify the language of your website. Additionally, it helps browsers decide whether or not to translate your website automatically.
  
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
   To avoid validation errors, always remember that every tag you write needs a closing tag.
  ```
  <h1>Heading 1</h1>
  <p>Paragraph Text</p>
  <img src="example.jpg" alt="Example Image" />
  ```
  ## 5. Don't use inline styles
It might seem easier to style with the inline code rather than creating an external style file. Inline styles are not a suggested coding technique, though, as they make websites more challenging to manage and update.

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
Since an alt attribute is not required for images, it is easy to ignore it. But, it's important to have a meaningful alt attribute for accessibility and validation reasons. Screen readers rely on the alt element for context, therefore it ought to explain what the image contains..

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
  Use `<figcaption>` along with `<figure>` element to add captions to your images.   
    
```<figure>
     <img src="image.jpg" alt="A beautiful landscape">
      <figcaption>A beautiful landscape</figcaption>
    </figure>
```
    
   ## 19. Images Captions
   Use `<figcaption>` along with `<figure>` element to add captions to images. As, this is important for accessibility and search engine optimization.
    
```
    <figure>
     <img src="example-image.jpg" alt="Example image">
     <figcaption>This is an example image</figcaption>
    </figure>
```
   ## 20. Avoid using `<b>` and `<i>`
   To add emphasis to text in HTML, it is discouraged to use the `<b>` and `<i>` tags as they lack semantic meaning. Instead, the    recommended practice is to utilize the font-weight CSS property, or employ the `<strong>` and `<em>` tags which have a semantic significance.
    
```
    <p>Did you <em>really</em> think that was a good idea? You <strong>shouldn't</strong> have done that.</p>
```

    
  
   
