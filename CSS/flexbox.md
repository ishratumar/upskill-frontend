# CSS FlexBox

## What is Flexbox?

⇢ Flexbox is a one-dimensional layout model. Before flexbox, there were four layout modes. The Flexbox provides a lot of flexibility.

It has two entities:
✧ flex-container
✧ flex-items
![CONTENT (11)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/5a541459-9499-4d9e-be7a-c3f3631c7c08)

### Example:

![CONTENT (12)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/926a4cd2-725f-4e57-ae04-c384645044fa)

### Flex Container Properties

![CONTENT (13)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/5c422618-ef6f-45dd-b320-f8a3de6ab753)

### Flex Item Properties
![CONTENT (15)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/329734e8-cd3f-4a27-8c82-d4f4078c027c)

## display

⇢It is important to note that in order to use Flexbox properties, the display property must be set to "flex" or
"inline-flex" on the parent container of the flex items. Without this, the Flexbox properties will not have any effect.

## 1. Container Properties

✧ flex-direction: row & row-reverse.
![CONTENT (17)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/d83c44dc-a1da-4097-8c3f-c37164144d61)

✧ flex-direction: column & column-reverse.
![CONTENT (18)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/e863caba-6ea0-4e31-8aae-20828005c70a)

### Flex Wrap
![CONTENT (22)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/3094df5c-3e45-4173-865e-632eca69b44c)

### flex-wrap

![CONTENT (23)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/e5addbbf-2848-4f84-99a9-fe6e41a97cb2)

There is another shorthand property, `flex-flow`, which allows setting both the `flex-direction` and `flex-wrap` properties in one line.

### Example:

![FoGrMCfaAAAAtwk](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/51d58d3e-0f7e-4240-85b7-da65dbbde2ad)

###  justify-content

![CONTENT (26)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/1066703f-d62c-4c93-9412-551d467cdb76)

### align-items

![CONTENT (27)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/36c60ea4-aecc-4321-89db-1e0cf5ef7980)

### align-content

![CONTENT (28)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/95484b41-ddc5-4396-be8d-6ee12afabada)

## Flex items
### order property

![CONTENT (30)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/a49c9b33-cb31-429b-95fd-b954dbff8c22)

### Flex Items Properties

![CONTENT (31)](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/65d95d57-48c6-4c99-b75b-ad9bc4e6810a)

### Shorthand
The `flex` property is a shorthand for the `flex-grow`, `flex-shrink`, and `flex-basis` properties.

### Example:
The element with the class "item2" will have a starting width of 100 pixels, and it will not grow or shrink in size
relative to the other flex items in its container.

![FoGrPKbacAEQB6R](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/fbeabab3-4ff6-4116-abd3-d39146fdb72f)


## align-self
The `align-self` property is similar to the `align-items` property that is used for Flex Containers, but it is 
applied to individual Flex Elements. It overrides the default alignment set by the `align-items` property.

It can take the following values:
![FoGrPljaYAQmP4C](https://github.com/ishratUmar18/upskill-frontend/assets/47534248/736d4a79-2cff-4805-9f8a-9c2c182a3846)

## Resources
- [Flexbox by CSS Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Flexbox Series by Wes Bos](https://flexbox.io/)
- [Flexbox by MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)
- Ebook - [Master Flexbox and Grid](https://utsavmeena.com/?wpam_id=33)



### That's all! For more read this blog post on Medium. [All you need to learn about CSS FlexBox](https://ishratumar.medium.com/css-flexbox-eb9dc69c4a6a).
