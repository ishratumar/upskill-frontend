# Responsive Design: Meta Tags, Media Queries, Flexbox, CSS Grid, and Viewport Units

In today's digital world, responsive design is crucial. It guarantees that webpages and apps will run smoothly across different devices.
With responsive design, you can increase your customer base, improve the user experience, and foster success. 

There are some amazing techniques available that can help you make your website responsive. Here we will concentrate on viewport units, 
media queries, meta tags, Flexbox, and the CSS Grid. 

You want to know more about those methods, right?

Let's get going!

## Meta Tags
Meta tags are placed inside the `<head>` section of the HTML document and are not displayed on the page itself. 

With the viewport meta tag in the HTML code of a webpage, you can control how the webpage looks on different devices with varying screen sizes.

**Example:**
```
<head>
<meta name="viewport" content="width=device-width", initial-scale=1.0" >
</head>
```
## Media Queries
Media queries are essential for responsive web design. You can apply different styles using media queries depending on factors like screen size, device orientation, and aspect ratio.

**Examples:**
Here are some examples that you can use in your projects:

1. Write a media query to apply styles when the viewport width is 200px or larger.
```
@media (min-width: 200px) {
.element {
    font-size: 20px;
    background-color: green;
  }
}
```
In the media query above, the styles will be applied when the viewport width is 200 pixels or larger.


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
Media queries give you a lot of flexibility when it comes to adjusting your website's layout and design for different devices and screen sizes.


### Media Queries breakpoints
![FEDzQAwX0AICK_4](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/e28dc6dd-da4d-4bbf-aa38-72770120184d)

## CSS Grid
## Flexbox
## The clamp( ) function
## The min() and max() functions
## Responsive Images
You can use height, width, and object-fit properties to resize an image so that it fits within a div container.

This can come in handy when you want to make sure that an image is a specific size or that it looks good on all devices.
![FfP53_0UUAAh_2C](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/98ab7fa7-f3b9-4a44-86af-39e7caea42f3)




