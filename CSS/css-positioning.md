# CSS Position Property

The position property specifies where an element should be placed on the page.Initially, it is static, you can use it 
on any element, but it cannot be animated.

## Syntax:
```
position: static | sticky | absolute | fixed | relative
```

## position: static;

✰ It defines the default position of the element. Positioned elements are elements whose placement has changed from being
static to one of the four possible positions: absolute, relative, fixed, and sticky.
![navbar animation](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/678e6a28-813e-4bff-84f4-e1151f451034)

## position: relative;

✰ In relative position, elements are positioned along with the normal flow of the page and offset based on values for top, right, 
bottom, and left. It occupies the same space on the page as if it were static since its offset does not affect other elements.
![20](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/3c7cfc06-42e3-4b72-ba86-baa9baea52ce)

## position: absolute;

✰Elements are positioned relative to their first positioned ancestor. Components with no descendants are positioned relative to
the first containing block. Ultimately, its position is defined by its top, right, bottom, and left values.
![21](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/7c03751a-6496-474e-b6ef-0435555e4425)

## position: fixed;

✰ Elements are positioned relative to the viewport. It behaves like an absolute positioned element in that it is detached from the
page's flow and no longer affects the layout. It won't scroll up when you scroll down. Fixed headers are one example.
![22](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/67eda3ff-7402-4e64-94e3-1ff7547b097a)

## position: sticky;

✰ It is a hybrid of a relative and a fixed positioned element.
✰ Sticky elements switch between fixed and relative positions based on scroll position. Its position is relative until the offset
position occurs in the viewport.
After the offset position comes into the viewport, it stays in place like a fixed positioned element.

![navbar animation](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/b76988cd-1171-47bb-98b1-232c99bb9841)

### That's all! I hope you find it helpful :))
