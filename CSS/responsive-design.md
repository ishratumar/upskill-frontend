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

---

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

**Demo:**
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
---

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
**Demo:**
![responsive-design (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/5bf302a6-d822-4699-ad2e-cec50d2d39b9)

2. Use `auto-fit` to create columns that automatically adjust their width.
```
.grid-container {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}
```
**Demo:**
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
---
## Viewport Units
With viewport units, you can specify sizes in relation to the viewport's dimensions in CSS. They can be used to design layouts that change according to the size of the screen. The difference between viewport units and percentage(`%`) units is that viewport units (`vw` and `vh`) are based on the entire window, whereas percentage units (`%`) are based on the local context.

**Examples:**

### Responsive Typography
```
.heading {
  font-size: 10vw; /* Responsive font size */
  margin-bottom: 2vh;
}
.description {
  font-size: 5vh; /* Responsive font size */
}
```

**Demo:**
![responsive-design](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/52ce5dc8-56f2-4e00-b6fc-4da100990cfa)

```
.hero {
  height: 100vh; 
}
.image {
  width: 50vw;
  }
```
In this example, the `vw` command sets the width of the image to 50% of the viewport width and the height of the hero section to 100% of the viewport height.

```
div {
height: 50vh;
}
```
The `vh` specifies the height of the `div` in this example to be 50% of the viewport height.

```
div {
height: 50svh; 
}
```
The `svh` command, in this case, adjusts the height of the `div` element to 50% of the viewport's shorter dimension (height or width).

```
div {
height: 50lvh; 
}
```
In this case, the `lvh` sets the viewport's height to 50% of its longer dimension.

```
div {
height: 50dvh; 
}
```
Sets the height to 50% of the viewport diagonal.

Viewport units provide an easy way to create responsive designs instead of solely using media queries.
Check browser support [here](https://caniuse.com/viewport-units).

---
## Flexbox
A quick and effective way to use Flexbox to implement responsive design is by using the `flex-wrap` property. Flex items will, by default, try to fit in a single line within the flex container. The `flex-wrap` property is set to `nowrap` by default. However, with the `flex-wrap` property set to `wrap`, the items will wrap to a new line when the container's width becomes too small to fit them all on a single line.

**Example:**
```
.container {
  display: flex;
  flex-wrap: nowrap;
 }
.item {
  flex: 1 0 200px;
}
```

**Demo:**
![nowrap flexbox](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/a45139ed-085b-4f32-9890-18564e2a37e9)


```
.container {
  display: flex;
  flex-wrap: wrap;
 }
.item {
  flex: 1 0 200px;
}
```

**Demo:**
![wrap flexbox](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/f445b753-a5d6-4f90-96d5-31bec2007c69)


In cases like the one above, where there is insufficient width, the flex container will wrap the items into a new line. Each item will have a minimum width of `200px (flex-basis: 200px)` and a flexible width that allows it to `grow (flex-grow: 1)` and `shrink(flex-shrink: 0)`.

## Responsive Typography with clamp( ) function
In CSS, you can specify a value that falls within a given range by using the `clamp()` function.

**Example:**
```
.text {
  font-size: clamp(14px, 3%, 24px);
}
```

**Demo:**
![clamp function](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/d91ac482-30a0-47e7-a8d7-787b601d4ae6)


This example demonstrates how to change the text element's font size using the `clamp()` function. The minimum font size is `14px`, the maximum font size is `24px`, and the preferred font size is `3%` of the viewport width (3vw).

The browser will automatically select the preferred font size to make sure that text is readable and responsive on screens of all sizes.

---
## The min() and max() functions
Using the `min()` function for *widths* and the `max()` function for *padding* and *margin*, you can create responsive designs with controlled *minimum* and *maximum* dimensions for elements that guarantee a constant and aesthetically pleasing layout across different screen sizes.

**The min() function example:**
```
.container {
  width: min(300px, 50%);
 }
```
The container in this example will have a *minimum* width of *300* pixels or *50%* of the width of its parent container, whichever is greater.

**The max() function example:**
```
.container {
   padding: max(20px, 5%);
   margin: max(10px, 2%);
 }
```

The *padding* and *margin* of the container are each limited to a *maximum* of 20px and 10px, respectively, or *5%* and *2%* of its *width*, in the `max()` function example. This ensures controlled spacing while upholding the established limits.
## Responsive Images
You can use `height`, `width`, and `object-fit` properties to resize an image so that it fits within a `div` container.

This can come in handy when you want to make sure that an image is a specific size or that it looks good on all devices.
![FfP53_0UUAAh_2C](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/98ab7fa7-f3b9-4a44-86af-39e7caea42f3)

---
## Resources 
- Responsive Design - [MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)
- Learn Responsive Design - [Freecodecamp YouTube Channel 4 hours Course](https://youtu.be/srvUrASNj0s)
- Learn Responsive Web Design(Intermediate level ) - [Free Course with Kevin Powell on Scrimba](https://scrimba.com/learn/responsive)
- Complete Web Developer in 2023: Zero to Mastery - [Paid Bootcamp](https://academy.zerotomastery.io/a/aff_r1613hhr/external?affcode=&affcode=441520_nmkbcy8m)


---
## Conclusion
That's pretty much it. I really hope it gives you a better understanding of Responsive Design.
Message me on [Twitter](https://twitter.com/ishratUmar18) if you have any questions.

## If you find it helpful, give it a ⭐ and share it with others.

