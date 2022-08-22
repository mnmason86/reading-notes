[<=== Back](/README.md)

# HTML & CSS by Jon Duckett
*Summarized*

## Chapter 15: Layout
p.358-404

### Positioning Elements

> CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. Specify using the `position` property.

#### Normal Flow

> In normal flow, each block-level element sits on top of the next one. Since this is the default, you do not need a CSS property to indicate that elements should appear in normal flow.

#### Relative Positioning
`position : relative`

> Relative positioning moves an element in relation to where it would have been in normal flow.

#### Absolute Positioning
`position : absolute`

> When the position property is given a value of absolute, the box is taken out of normal flow and no longer affects the position of other elements on the page (they act like it is not there).

#### Fixed Positioning
`position : fixed`

> Fixed positioning is a type of absolute positioning that requires the position property to have a value of `fixed`. It positions the element in relation to the browser window. Therefore, when a user scrolls down the page, it stays in the exact same place.

Designs need to be able to work on a range of different screen sizes, take screen resolution into consideration, generally be around 960-1000 pixels wide, and account for fixed width and liquid layouts.


#### More on CSS Layout!

[CSS Layout](https://web.dev/learn/css/layout/)