# Floats in CSS

## What is float?

Floats are used to alter the default flow of elements. It specifies how elements should float and position themselves
to the right or left of their containers.

It is usually applied to layouts and images. Multi-column layouts were commonly built with the float property before Flexbox and Grid. The main purpose of this was to float images within text blocks.

Float has two properties: clear and float. 

Float determines whether or not the box should float.

### Syntax
```
float: none | inherit | left | right | initial;
```
By using the clear, elements after floating elements are avoided.

### Syntax:
```
clear: none | both | left | right | inherit;
```
In CSS, some rules work in conjunction with others.

Most of the time, when you reach for one, you reach for the other as well. Float and Clear work well together.

In general, if you're using float, you might want to consider using clear. Otherwise, your design might break.

Without `float` property Example:
![css important topics (5)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/fe0455d2-8e55-4d5e-86af-ae0f8e423076)

## How does float work?

Elements are only floated horizontally. Elements can therefore only float left or right; they cannot float up or down. 

A floated element can be moved as far to the left or right as it can go.

It simply indicates that a floating element could show up on the screen's extreme left or right. 

The elements that come after it will move around the floating element. 

The floating element won't affect elements that come before it.

When an image floats to the right, the surrounding text moves to the left, and when it floats to the left, the surrounding text moves to the right.

Now let's apply float to an example. See the code below:
```
.align-left {
  float: left;
  margin-right: 20px;
}

.align-right {
  float: right;
  margin-left: 20px;
}
```
Example with `float` property:
![css important topics (4)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/bde03d87-d57f-4959-9f7d-6c4ca3a40a80)

- Here's the complete code for the example mentioned above, available at [floats.html](CSS/floats.html).
## Resources 
Check out these links to learn more:

- [MDN - Floats](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Floats)  

- [CSS Tricks - All About Floats](https://css-tricks.com/all-about-floats/)

## That's all! I really hope you find it helpful!
