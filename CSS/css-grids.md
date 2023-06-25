## From zero to grid hero: An illustrated guide to CSS Grid essentials
### Mastering CSS Grid with illustrations

#### Table of contents:
1. What is the grid 
2. Grid terminology
3. Grid container properties
4. Grid items properties
5. Responsive grids
6. Shorthand properties

---

## What is the grid in CSS?
If we compare CSS Grid to any previous web layout system, it is a two-dimensional grid-based layout system that completely changes how we create user 
interfaces. We've been using CSS to design the layout of our web pages, but it hasn't always worked out well.
In the early days, we used tables and later floats, positioning, and inline blocks, which were necessary workarounds for layouts lacking in some key aspects.

The CSS Grid is the first CSS module built expressly to address the layout issues we’ve all been 
playing with. [Flexbox](https://ishratumar.medium.com/css-flexbox-eb9dc69c4a6a) is also a popular one-dimensional layout tool. These two tools work well together.

Designing web pages without floats or positioning is made easy with grids. It can have items placed on it vertically, horizontally, or both at once. You can arrange
items however you want, even stacked.

## Grid terminology
Before learning the properties of Grid, it is important to comprehend the terminologies 
used in Grid. If you have a solid grasp of these concepts, mastering Grid will go a lot easier for you.

Let's jump right in.

## Grid container
The grid container is the parent element in a grid layout with one or more child elements.

**Example:**

```
<div class="grid-container">
  <div class="grid-item">Item 1</div>
  <div class="grid-item">Item 2</div>
  <div class="grid-item">Item 3</div>
</div>
```
In the above example, the div with class `grid-container` is the parent element, and the divs with class `grid-item` are the child elements.

## Grid item
A grid item is an element that is an immediate descendant of the grid container.
```
<div class="grid-container">
  <div class="grid-item">Item 1</div>
  <div class="grid-item">Item 2</div>
  <div class="grid-item">Item 3</div>
</div>
```
The Grid items (contents) are distributed along the main axis and cross axes. You can build a website layout by modifying the components and using 
different grid properties.

## Grid Architecture
Illustration ↝
![grid-container](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/267c8212-9663-4387-9263-4f3e9c62fa7a)

## Grid lines

Grid elements are composed of grid lines, which are horizontal and vertical. If your grid has three rows and three columns, 
it will have four column lines and four row lines, including the one final line.

Illustration ↝
![grid-linesss](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/5e971ce6-a596-423c-83a7-fef4939a0dbe)


## Grid cell
A single unit within a grid layout is referred to as a grid cell. It is the intersection of a row and a column in the grid. Each cell can contain content 
or other elements.

In the illustration below, each square(item) in the grid represents a cell.

Illustration ↝
![grid-cell (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/b494b021-3fd8-484f-b4c7-1725bd1f4575)

## Gaps
In a grid layout, the gap is used to indicate the size of the gutter or space between columns and rows. It determines the gap between adjacent grid tracks.

**Gap properties:**
- `column-gap` - sets the gap between columns.
- `row-gap` - sets the gap between rows.
- `gap` - It's a shorthand. You can use it to set the `column-gap` and `row-gap` in a single line.

**Example:**
```
.grid-container {
  display: grid;
  gap: 20px;
}
```
Illustration ↝
![grid-gap (3)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/db903b85-3a1f-4680-98f0-218530ee8b21)

## Grid tracks
The space between two grid lines is referred to as a track. A row track is a space between two row lines, and a column track is a space between two column lines. These tracks are created when we give a size to our grid.
See the illustration below to better understand:

Illustration↝
![grid-track (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/5b10f5d9-23fd-40b6-a3d2-cb0b94f24311)


## Grid Area
The grid area consists of several grid cells. It allows items to span a specified number of rows and columns within a grid layout.

12 row X 12 column layout

Illustration ↝
![grid-template-area](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/8de186cd-87f6-4b32-bb50-ce27f34fe55b)


---

## Grid Properties
In terms of grid properties, there are two types. As following:
1. Parent Properties(Grid Container)
2. Children Properties(Grid Items)

## Grid container properties

### display
When the `display` property of an HTML element is set to `grid` or `inline-grid`, the element becomes a container for a grid.
The `grid` creates a *block-level* container that enables flexible and grid-like layouts by placing items in both columns and rows.

**Example:**
```
.grid-container {
  display: grid;
}
```
Output ↝
![image](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/43622c98-555b-45d0-b37f-279e60623a27)

The `inline-grid` container, on the other hand, creates an *inline-level* container that enables items to be positioned horizontally, 
making it suitable for inline layouts.

**Example:**
```
.grid-container {
  display: inline-grid;
}
```

Output ↝
![image](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/8b20bf79-d1cb-4b0a-b6b6-824df145cfd3)

Have you noticed the text **before** and **after**?

Those are two span elements that I added before and after the containers. So you can better understand the concept of *block-level* 
and *inline-level* grid containers.

## Rows and Columns
Rows and columns are made up of grid lines. Properties you can use to define rows and columns in a grid:

**grid-template-columns** - determines both the width and the number of columns in a grid. You can use several length units, 
including px, em, %, min-content, max-content, fr, and auto, to measure that.

Use `auto` if you want columns to have the same width or an element to take all the available space. The `fr` is basically a fraction; it is a *grid-only* unit. 
The keywords `min-content` and `max-content` denote the *minimum* and *maximum* sizes, respectively, that the content can occupy.

You have two options for setting column widths: either individually for each column or collectively for all columns using the `repeat()` function.

Illustration ↝
![grit-template-column-sprt (2)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/770faf4c-98e6-4639-8ba6-795fcc8bec3c)

There will be precision in the pixel measurements. Any space available will be filled with the keyword auto.

Graphic↝
![grit-template-column-1fr (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/6748eced-1851-4118-9e48-6f30b74e511e)

There will be no difference in size between the boxes as they are measured in fractions (1fr).

`grid-template-rows` - determines the height and the number of rows in a grid. The height and number of rows can also be specified using different length units.

You have two options for setting rows height: either individually for each row or collectively for all rows using the `repeat()` function.

Illustration ↝
![differnt-units-unit](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/e2ceb6b4-cf66-4a99-86e1-63d2630556d1)

The height of each row is specified separately 👆.

Illustration ↝
![fr-unit](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/715474cc-2119-48d9-9851-9a8ad8c55e8b)

The height of each row using `repeat()` function 👆.


Here's an example code to create a grid with 3 columns and 3 rows using different sizing units.
```
.grid-container {
  display: grid;
  grid-template-columns: 7em 200px 20%;
  grid-template-rows: 100px 80px auto;
}
```
---

### Justify items
Using the `justify-items` property, you can position the grid items inside the grid container along the main axis (x-axis). It may include one of the 
following four values:

```justify-items: start | end | center | stretch;```

justify-items: start;
![justify-items-start (4)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/664e4728-9d75-4a34-ac2a-f494c8657908)



justify-items: end;
![justify-items-end (2)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/89e0de76-f4ea-4baa-8907-0e948052e56e)


justify-items: center;
![justify-items-center (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/e3ad19af-0f69-46f2-9228-2968453d4fdd)


justify-items: stretch;
![justify-items-stretch (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/f28a38d1-a2e9-4348-a3da-ff3c0164e591)

---

### Align Items
Using the `align-items` property, you can position the grid items inside the grid container along the cross-axis (y-axis). It may include one of the 
following four values:

```align-items: start | end | center | stretch;```

align-items: start;
![align-items-start (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/8541f4f4-b27c-4709-9a4d-901667f7395d)


align-items: end;
![align-items-end (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/f98c2b50-f87e-4e8c-94a0-d5c73cd0db69)


align-items: center;
![align-items-center (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/d8351084-b072-48ea-83f9-5e42d381ffce)


align-items: stretch;
![align-items-stretch (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/e0338e92-4a25-45fb-9336-d1be37a6c3e4)


---

### Justify content
Using the `justify-content` property, you can position the grid(all items) inside the grid container along the *main-axis (x-axis)*. 
It may include one of the following seven values:

```justify-content: start | end | center | stretch | space-between | space-around | space-evenly; ```

justify-content: start;
![justify-content-start (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/2043c257-b43b-4b68-95d7-7b0920d1c5c3)


justify-content: end;
![justify-content-end (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/686bc820-f631-4a3d-9b89-ef2ea09076ab)


justify-content: center;
![justify-content-center (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/b0c4e8a0-4c39-4bd6-8710-c3219ad37fd1)


justify-content: stretch;
![justify-content-stretch (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/0a63105e-9f7d-4cc8-9761-1fb7f78d3a23)


justify-content: space-around;
![justify-content-space-around (2)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/173c6f54-7898-4b66-9227-394f8bc52217)


*Note:* There is an equal amount of space between each grid item, with half-size spaces at the ends.

justify-content: space-between;
![justify-content-space-between (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/934546a7-6a67-480e-9d2a-7a7bab20c0ed)

Grid items are separated with equal space between them.

justify-content: space-evenly;
![justify-content-space-evenly (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/9508e16a-845b-4ef9-901a-f809023072eb)

Grid items are separated with even space between grid items also at ends.

---

### Align Content
Using the `align-content` property, you can position the grid(all items) inside the grid container along the *cross-axis (y-axis)*. It may include one 
of the following seven values:

```align-content: start | end | center | stretch | space-between | space-around | space-evenly;```

align-content: start;
![align-content-start (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/7f41193d-b807-4b96-b0a8-cf729a5af773)


align-content: end;
![align-content-end (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/86ec5bb8-50b0-40e4-96ee-1c0b526a0d67)

align-content: center;
![align-content-center (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/b144cebe-5894-4093-8f8f-f0ca3cec1fa1)


align-content: stretch;
![align-content-stretch (2)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/e0de1076-18e0-4dde-b568-87e037c2003e)


align-content: space-around;
![align-content-space-around (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/0592d070-ea96-4782-a579-09237e8efec2)


align-content: space-between;
![align-content-space-between (4)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/8450820f-079e-46a5-a95b-39a53e584c0e)


align-content: space-evenly;
![align-content-space-evenlyplus1 (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/40ff8385-9e11-4dc4-8c20-398e7229baf9)


---

## CSS Grid items properties
The grid items are contained in a grid container. First, let's take a look at the grid rows and column start and end points. To better understand the concept, 
look at the illustration below.

Illustration ↝
![grid-row-cols](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/ef87ec0e-3cc1-424d-9ccc-46900ad5ebe7)


### column-start & column-end

#### The grid-column & grid-row properties
The `grid-column` property determines which column(s) an item should appear on. The `grid-row` property determines which row(s) an item should be placed on.
The `grid-column` is shorthand for `grid-column-start` and `grid-column-end` properties. 

**Example:**
```
grid-column-start : 2;
grid-column-end : 4;

/* shorthand */
grid-column : 2 / 4;
```

The `grid-row` is shorthand for `grid-row-start` and `grid-row-end` properties.

Example:
```
grid-row-start : 2;
grid-row-end : 4;

/* shorthand */
grid-row : 2 / 4;
```

##### The grid-column example:

Here's an example of a grid container with six items(divs):

*HTML*
```
<div class="grid-container">
  <div class="grid-item1">Item 1</div>
  <div class="grid-item2">Item 2</div>
  <div class="grid-item3">Item 3</div>
  <div class="grid-item4">Item 4</div>
  <div class="grid-item5">Item 5</div>
  <div class="grid-item6">Item 6</div>
</div>
```

*CSS:*

**Syntax:** grid-column: start-line / end-line;

```
.grid-item1 {
  grid-column: 1 / 3;
}

.grid-item2 {
  grid-column: 3 / 5;
}

.grid-item3 {
  grid-column: 1 / 4;
}
.grid-item4 {
  grid-column: 4;
}
.grid-item5 {
  grid-column: 1;
}
.grid-item6 {
  grid-column: 2 / 5;
}
```

This example uses the `grid-column` property to style 6 items in a grid layout.

The `.grid-item1` takes up two columns, extending from the first to the third. The `.grid-item2` takes up two columns and extends from the third to the fifth.

The `.grid-item3` occupies three columns, extending from the first to the fourth. Only the fourth column is occupied by the `.grid-item4`.

The `.grid-item5` takes up one column from the first column to the second column, while the `.grid-item6` takes up three columns, spanning from the second 
column to the fifth column.

With the help of these `grid-column` values specify each item's position and width within the grid structure, so you can arrange elements precisely and flexibly.

Illustration↝
![image](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/875f9fde-0b89-44c0-9174-340bc9aad376)


##### The grid-row example

Here's an example of a grid container with six items(divs):

*HTML*

```
<div class="grid-container">
  <div class="grid-item1">Item 1</div>
  <div class="grid-item2">Item 2</div>
  <div class="grid-item3">Item 3</div>
  <div class="grid-item4">Item 4</div>
  <div class="grid-item5">Item 5</div>
  <div class="grid-item6">Item 6</div>
</div>
```

*CSS:*

**Syntax :** grid-row: start-line / end-line;

```
.grid-item1 {
  grid-row: 1 / 3;
}

.grid-item2 {
  grid-row: 3 / 5;
}

.grid-item3 {
  grid-row: 1 / 4;
}
.grid-item4 {
  grid-row: 4;
}
.grid-item5 {
  grid-row: 1 / 2;
}
.grid-item6 {
  grid-row: 2 / 5;
}
```

This example uses the `grid-row` property to style 6 items in a grid layout.

The `.grid-item1` takes up two rows, extending from the first to the third. The `.grid-item2` also takes up two rows and extends from the third to the fifth.

The `.grid-item3` occupies three rows, extending from the first to the fourth. The `.grid-item4` takes one row.

The `.grid-item5` takes up one row from the first row, while the `.grid-item6` takes up three rows, spanning from the second row to the fifth row.

With the help of these `grid-row` values, you can specify each item's position and height within the grid layout, so you can arrange elements precisely 
and flexibly.

Illustration ↝
![image](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/77c05bc8-4f18-4fa4-882a-72056d32efb4)


You can also do this using the `span` keyword, which is the same thing but easier to read and understand. 

So, what `span` does, specify the number of columns/rows each item should span/expand.

Here is an example of how you can use span in `items.grid-item1` and `.grid-item2` mentioned above:
```
.grid-item1 {
  grid-row: 1 / span 2;
  grid-column: 1 / span 2;
}

.grid-item2 {
  grid-row: 3 / span 2;
  grid-column: 3 / span 2;
}
```

### Grid area
The `grid-row` and `grid-column` are excellent properties, but `grid-area` is even greater. The `grid-area` property is the shorthand for four values it 
requires:

- grid-row-start
- grid-column-start 
- grid-row-end
- grid-column-end 

If you want *.item1* to span over 2 rows and 2 columns. You can give it the `grid-area` with the starting line of row 1(1), the starting line of column 1(1),
the ending line of row 2(3), and the ending line of column 2(3). You can also use negative values.

**Syntax:** grid-area: row-start / column-start / row-end / column-end;
*CSS*

```
.grid-item:nth-child(1) {
  grid-area: 1 / 1 / 3 / 3;
}
```

Here's the illustration:
![image](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/94be43ab-377b-4330-900b-9dd19e24788f)


To define these values, you may also use the `span` keyword. Here is an example of how to use `span` to create the same layout:

```
.grid-item:nth-child(1) {
  grid-area: 1 / 1 / span 2 / span 2;
  }
```
The `grid-area` property can also be used to give names to grid items. It is more useful when you dealing with more complex layouts. Though to work with this 
first you must set up `grid-template-areas`. Once finished, you must include the names from the parent class inside the children(items) classes.

To begin with, define the `grid-template-areas` inside of your grid(parent) container like this:
```
.grid-container {
  display: grid;
  grid-template-columns: 1fr 3fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
  gap: 10px;
  height: 100vh;
}
```
Now, use the grid-area to specify the names used in the grid container inside the item classes as follows:

```
.header {
  grid-area: header;
}

.main {
  grid-area: main;
}

.sidebar {
  grid-area: sidebar;
}

.footer {
  grid-area: footer;
}
```

Output ↝
![image](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/f602d8d3-f897-45ca-b464-93e565a6ca4d)


### Responsive Grids
#### Media Queries
Having a responsive website is way more important than it was before. 

"Mobile devices, excluding tablets, contributed 58.33% of all website traffic worldwide in the first quarter of 2023." - [Tiago Bianchi](https://medium.com/r/?url=https%3A%2F%2Fwww.statista.com%2Fstatistics%2F277125%2Fshare-of-website-traffic-coming-from-mobile-devices%2F)

You cannot simply take the risk of missing an audience this large that browses on their smartphones.

You can use media queries to make the example above responsive. Before that, take a look at how it looks in responsive mode before 
applying any media queries:

Illustration ↝
![image](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/fc837dc5-369a-4897-ba1d-60472fcaaa62)


Before Applying Media Queries👆

Notice that it has the exact same layout as the desktop version. However, it does not look good. In order to make it look better on 
mobile mode, we need these items to stack on top of one another. To do this, we may use media queries.

Here's how to use media queries to accomplish that:
```
.grid-container {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas:
    "header"
    "sidebar"
    "main"
    "footer";
  gap: 10px;
  height: 100vh;
}

.
.
.

@media (min-width: 50em) {
  .grid-container {
    grid-template-columns: 1fr 3fr;
    grid-template-rows: auto 1fr auto;
    grid-template-areas:
      "header header"
      "sidebar main"
      "footer footer";
  }
}
```
You may notice, we only updated only one `.grid-container` class in the responsive design code and added media queries for the desktop 
version. When `grid-template-columns: 1fr` is set, the header, sidebar, main content area, and footer will stack vertically on mobile 
devices. 

Result ↝
![image](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/9bc397a4-1ce0-44d8-a742-fae40e970aa1)

After Applying Media Queries 👆

### Minmax() Function
The `minmax()`function helps you set the *minimum* and *maximum* grid 
track sizes. Using this method, you can give grid objects a *minimum* width and let them expand to a *maximum* width if there is 
extra space.

*For example:*
```
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}
```
The `auto-fit` keyword allows the columns to adjust and fill available space while respecting their *minimum* and *maximum* sizes. On the other
hand, the `auto-fill` keyword ensures that the grid is always filled by adding empty tracks to fill in additional
space. Both `auto-fill` and `auto-fit` are used in conjunction with the `repeat()` function in CSS Grid.

In addition, there is another sizing function called `fit-content()`. The `fit-content()` function in CSS Grid makes that grid tracks or items never go smaller than the *minimum (min-content)* size or bigger than the *maximum(max-content)* size  based on the content. You can make your designs more responsive and flexible by using `fit-content()` to create dynamic, flexible grid layouts.
```
.grid-container {
  display: grid;
  grid-template-columns: fit-content(200px) 1fr;
}
```
### Change elements order
CSS Grid Layout allows you to position elements anywhere within the grid, regardless of their order in the HTML code. This functionality
is especially helpful when designing alternate layouts for various screen sizes. By combining media queries and CSS Grid Layout, which
provides a powerful toolkit for precise designs, you can easily achieve precise designs that meet your needs.

*For example:*
```
.grid-item1 { grid-area: 1 / 2 / 1 / 3; }
.grid-item2 { grid-area: 1 / 4 / 1 / 3; }
.grid-item3 { grid-area: 1 / 1 / 2 / 2; }
```

Output ↝
![image](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/a77256c3-0729-44cb-bd99-6e6a1a04b8cf)

### The justify-self property
Using the `justify-self` property, you can position an item inside the grid container along the *main axis(x-axis)*. It may include
one of the following four values:

```justify-self: start | end | center | stretch;```

Illustration ↝
![align-self (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/5b94c5b1-596b-4e3d-8a55-77b05924038f)


### The align-self property 
Using the `align-self` property, you can position an item inside the grid container along the *cross-axis(y-axis)*. It may include one 
of the following four values:

`align-self: start | end | center | stretch;`

Illustration ↝
![justify-self (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/b087ebc2-d6e3-488b-94ae-e9b78ff45b9a)

## Shorthand Properties
Shorthand properties in CSS allow you to declare and set a number of related properties in one line. It will 
reduce the code you write and make your stylesheet smaller. Shorthand properties are usually used for properties with multiple values.

1. `gap / grid-gap`: Determine the space between tracks and grid items. The gap is a shorthand property for setting both row and column 
gaps, while `grid-gap` specifically sets the gap between grid items.
2. `grid-template`: Define the structure of the grid by specifying rows, columns, and areas. It is shorthand for `grid-template-rows`, 
`grid-template-columns`, and `grid-template-areas` properties.

3. `place-content`: It is shorthand for `align-content` and `justify-content` properties.
4. `place-items`: Set the alignment and positioning of individual grid items within the grid. It is shorthand for `align-items` and `justify-items` properties.
5. `place-self`: Control the alignment and positioning of a single grid item within its grid cell. It is shorthand for `align-self` and `justify-self` properties.
6. `repeat()`: Specify a pattern of repeating grid track sizes within the `grid-template-columns` or `grid-template-rows` properties.


## Resources
Interested in learning more? These are some of the best CSS Grid resources:

- [A Complete Guide to CSS Grid](https://medium.com/r/?url=https%3A%2F%2Fcss-tricks.com%2Fsnippets%2Fcss%2Fcomplete-guide-grid%2F) - CSS Tricks
- [CSS Grid](https://medium.com/r/?url=https%3A%2F%2Fweb.dev%2Flearn%2Fcss%2Fgrid%2F)- WEB.DEV
- [CSS Grid Layout](https://medium.com/r/?url=https%3A%2F%2Fdeveloper.mozilla.org%2Fen-US%2Fdocs%2FWeb%2FCSS%2FCSS_Grid_Layout) - MDN
- [CSS Grid Cheatsheet](https://medium.com/r/?url=https%3A%2F%2Fdev.to%2Fjoyshaheb%2Fcss-grid-cheat-sheet-illustrated-in-2021-1a3)
- [Grid by Example](https://medium.com/r/?url=https%3A%2F%2Fgridbyexample.com%2F) by Rachel Andrew
- Free course - [LEARN CSS GRID WITH WES BOS](https://medium.com/r/?url=https%3A%2F%2Fcssgrid.io%2F)
- [Learn CSS Grid by playing game - Grid Garden](https://medium.com/r/?url=https%3A%2F%2Fcssgridgarden.com%2F)
- [CSS Grid Generator](https://medium.com/r/?url=https%3A%2F%2Fcssgrid-generator.netlify.app%2F)

---
 
=> [Read it on Medium](https://ishratumar.medium.com/from-zero-to-grid-hero-illustrated-guide-to-css-grid-essentials-cd1531b56431)

## Conclusion
That's pretty much it. I really hope it gives you a better understanding of CSS Grids.
Message me on [Twitter](https://twitter.com/ishratUmar18) if you have any questions.

## If you find it helpful, give it a ⭐ and share it with others.
