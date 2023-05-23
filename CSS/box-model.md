# The Box Model in CSS 🎨

✧ In HTML, all elements are considered as a box. A box comprises padding, border, and margin in addition to its actual content.

![1](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/33b63721-e534-4153-a359-e9ffc3dadd38)
✧ Content refers to the actual data text and images, etc.

✧ Padding is transparent. It adds space around the content.

✧ Border surrounds padding and content.

✧ Margin is also transparent. It clears areas outside the Border.

## Reset Browser Style Defaults

✧ I think this is a great way to ensure that your project looks its best and is consistent across all platforms.

Take a look at the image below 👇🏻
![2](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/4efd35c5-8d66-494a-a487-7943d0fdd091)

## Box Sizing

There are two ways to specify box-sizing: 

   1. By default or content-box 
   2. border-box 

They automatically adjust the width based on the content size when we set the width.

### 1. box-sizing: content-box

✧ The default box type is content-box. It sets the width of the content only, not the entire box. 

✧ Even though we set the padding to 300px, the width may alter depending on padding and border size.

See the example👇🏻
![CONTENT (1)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/6a12b16a-72be-46db-bcc3-474437d75708)

### 2. box-sizing: border-box;

✧ box-sizing property was first introduced in CSS3. 

✧ Specifying the box-sizing property to border-box sets the width of the entire box, not just the content.

For a better understanding look at the image below👇🏻
![4](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/ab83792e-5585-4f45-8a26-4c04dc557258)

### Margin Types
There are two types of margin:
  1. Cumulative Margin
  2. Colapsing Margin

For better understanding see the illustration below 👇
![5](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/5c9fbbc9-71e8-401d-98e3-5292622be2ec)


✧ All modern frameworks use the border-box approach, and box-sizing with the border-box setting can be really helpful.

✧ To avoid writing this property in every element, you can specify it once in a universal `*` selector and it will apply to every HTML element.
![FZpXbcbVUAADuTU](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/ad05abd3-76d9-4bfc-a100-31b749bb3137)

### Overflow Property
✧ If we try to put too much text into an element that its height is not enough to hold it, the extra text will overflow outside of the element. 

✧ We can use the `overflow` property to specify what happens in this case.
![6](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/f470eaae-5315-4d23-8cc0-eca3bb071329)

✧ Depending on what we need, we can set overflow to auto, hidden, inherit, scroll, or visible.

✧ In this example, we have the overflow set to auto. This will add a scroll bar to help us better view the content within the given height.

Look how it works 👇🏻
![7](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/76719897-c130-4654-92e7-cdb820da846a)

## Resources: 
- [Learn Box Model by Web Dev Simplified - YouTube](https://youtu.be/rIO5326FgPE)
- [Box Model by web.dev](https://web.dev/learn/css/box-model/)
- [The box model by MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
## That's all! I really hope you find it helpful. If so, give it a ⭐.
