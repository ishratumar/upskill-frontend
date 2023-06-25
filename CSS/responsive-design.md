# Responsive Design: Meta Tags, Media Queries, Flexbox, CSS Grid, and Viewport Units

In today's digital world, responsive design is crucial. It guarantees that webpages and apps will run smoothly across different devices.
With responsive design, you can increase your customer base, improve the user experience, and foster success. 

There are some amazing techniques available that can help you make your website responsive. Here we will concentrate on viewport units, 
media queries, meta tags, Flexbox, and the CSS Grid. 

You want to know more about those methods, right?

Let's get going!

## Viewport Meta Tag
Meta tags are placed inside the `<head>` section of the HTML document and are not displayed on the page itself. 

With the viewport meta tag in the HTML code of a webpage, you can control how the webpage looks on different devices with varying screen sizes.

How the webpage displays without a Viewport Meta Tag:
![without-meta-tag](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/84c66375-7dd4-436f-981d-d4bb1ae71cd8)

**Example:**
```
<head>
<meta name="viewport" content="width=device-width", initial-scale=1.0" >
</head>
```

How the webpage displays with Viewport Meta Tag:
![with-media-tag](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/af7c81a9-35a7-43e0-872f-d6069a7c9e4c)


## Media Queries
Media queries are essential for responsive web design. You can apply different styles using media queries depending on factors like screen size, device orientation, and aspect ratio.

**Examples:**
Here are some examples that you can use in your projects:

1. Write a media query to apply styles when the viewport width is 340px or less.
```
@media (max-width: 340px) {
.item {
    font-size: 20px;
    background-color: lightgreen;
  }
}
```
In the media query above, the styles will be applied when the viewport width is 340px pixels or less.

**Demo**
![media-query-responsive-design](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/4ee27220-3452-4ee3-9223-891ed483d170)

2. Write a media query to apply styles when the device is in landscape mode.
```
@media (orientation: landscape) {
/* Styles */
}
```
*Note that you can also style 'portrait' mode using a media query. Change "landscape" to "portrait" and add styles.*

3. Write a media query to apply styles when the aspect ratio is 1:1 or larger.
```
@media (min-aspect-ratio: 1 / 1) {
/* Styles */
}
```

4. Write a media query to apply styles when the aspect ratio is 16:9 or larger.
```
@media (min-aspect-ratio: 16 / 9) {
/* Styles */
}
```

5. Write a media query to apply styles when the viewport width is between 200px and 300px.
```
@media (min-width: 200px) and (max-width: 300px) {
/* Styles */
}
```
Media queries give you a lot of flexibility when it comes to customizing your website's layout and design for different devices and screen sizes.


### Media Queries breakpoints
![FEDzQAwX0AICK_4](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/e28dc6dd-da4d-4bbf-aa38-72770120184d)

## CSS Grid
CSS Grid is a powerful layout framework that allows you to create intricate and responsive grid-based layouts. It offers a versatile replacement for traditional float-based layouts and makes creating multi-column designs easier.

### minmax()
The `minmax()`function helps you set the *minimum* and *maximum* grid 
track sizes. Using this method, you can give grid objects a *minimum* width and let them expand to a *maximum* width if there is 
extra space.

### auto-fit & auto-fill
The `auto-fit` keyword allows the columns to adjust and fill available space while respecting their *minimum* and *maximum* sizes. On the other hand, the `auto-fill` keyword ensures that the grid is always filled by adding empty tracks to fill in additional
space.

**Examples**
Here are some examples that you can use:
1. Use `auto-fill` to create columns that automatically fill the available space.

```
.grid-container {
display: grid;
grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
}
```
**Demo**
![responsive-design (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/5bf302a6-d822-4699-ad2e-cec50d2d39b9)

2. Use `auto-fit` to create columns that automatically adjust their width.
```
.grid-container {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}
```
**Demo**
![autofit](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/7dbd5707-b47a-461f-b2fd-d437beca37b1)

3. Use `minmax` to create columns with a minimum width of 300px.
```
.grid-container {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); 
}
```

4. Use `grid-auto-rows` property to sets the height of automatically generated rows to 50px.
```
.grid-container {
display: grid;
grid-auto-rows: 50px;
}
```

In addition, there is another sizing function called `fit-content()`. The `fit-content()` function in CSS Grid makes that grid tracks or items never go smaller than the *minimum (min-content)* size or bigger than the *maximum(max-content)* size  based on the content. You can make your designs more responsive and flexible by using `fit-content()` to create dynamic, flexible grid layouts.
```
.grid-container {
  display: grid;
  grid-template-columns: fit-content(200px) 1fr;
}
```

## Viewport units

## Flexbox

## The clamp( ) function
## The min() and max() functions
## Responsive Images
You can use height, width, and object-fit properties to resize an image so that it fits within a div container.

This can come in handy when you want to make sure that an image is a specific size or that it looks good on all devices.
![FfP53_0UUAAh_2C](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/98ab7fa7-f3b9-4a44-86af-39e7caea42f3)




