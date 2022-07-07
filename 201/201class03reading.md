[<=== Back](README.md)

# HTML & CSS by Jon Duckett
*Summarized*

## Chapter 3: Lists
p.62-73

### Ordered Lists
Ordered lists are created with the `<ol>` element. Each item is indicated with a `<li>` (list item) tag. It is best to use CSS to style the list's attributes (numbers, letters, roman numerals, etc.). Items are listed in a particular order.

### Unordered Lists
Unordered lists are created with the `<ul>` element. Each item is indicated with a `<li>` tag. Items are listed in no particular order.

### Definition Lists
Definition lists are created with the `<dl>` element, and usually consist of terms and their definitions. Terms are indicated with `<dt>`, definitions are indicated with `<dd>`.

Lists may also be nested inside of other lists.

## Chapter 13: Boxes
p.300-329

### Controlling size of boxes
By default boxes are sized just big enough to hold its contents. Height and width can be defined by pixels, or percentage of the browser window.

Some browser windows expand and shrink on different devices. The `min-width`, `max-width`, `min-height`, and `max-height` can be set so that boxes do not appear too wide, narrow, tall, or short.

> The `overflow` property tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values: `hidden` (hides any extra content) or `scroll` (adds a scrollbar to the box).

### Box Model (borders, margin, padding)
- Border: Separates the edge of one box from another
- Margin: Sit oustide the edge of the border, used to create a gap between the borders of two adjacent boxes.
- Padding: The space between the border of a box and any content contained within it.

### Displaying and Hiding Boxes
Elements default to *inline*. In order to change them to *box* elements, use `display: box`.

`display: none` hides the element from the page, and there will be no place for it on the page, but can still be viewed when viewing the source.

In order to hide the element, but leave a space for it, use `visibility: hidden`.

# JavaScript & JQUERY by Jon Duckett
*Summarized*

## Review of Chapter 2: Basic JavaScript Instructions
p.70-73

An **array** stores a list of values instead of just one. Arrays are declared the same way as a single variable, but placed inside a set of square brackets `[]`, and each item is separated by a comma. Values inside an array do not need to be the same data type.

Items in an array are assigned a number called an **index**. Index values start at 0.

## Chapter 4: Decisions and Loops
p.162-182

### Switch Statements
> A **switch** statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value.

The entire statement lives in one code block. A colon `:` separates the options from the statements that are to be run.

Example:

```
switch (level) {

  case 'One':
    title = 'Level 1';
    break;

  case 'Two':
    title = 'Level 2';
    break;

  default;
    title = 'Test';
    break;
}
```

### Type Coercion / Truthy & Falsy Values

Type coercion is when JavaScript converts data from one type to another, or tries to make sense of an operation by changing the data type.

Due to coercion, every value in JavaScript can e treated as if it were true or false.

### Checking Equality & Existence / Short Circuit Values

> Because the presence of an object or array can be considered truthy, it is often used to check for the existence of an element within a page.

Strict equality operators `===` and `!==` result in fewer unexpected values.

Logical operaters are processed left to right, and stop as soon as they have a result.

### Loops

> Loops check a condition. If it returns `true`, a code block will run.

The condition is checked a number of times and will run as long as it returns `true`. When it returns `false`, it will stop running.

#### For Loops

The most common type of loop. It is used to run code a specific number of times.

#### While Loops

When you do not know how many times the code should run, a `while` loop can be used. The code will run as long as the condition is true.

#### Do While Loops

Very similar to the `while` loop, but will always run the condition inside the curly braces at least once, even if the condition evaluates `false`.

