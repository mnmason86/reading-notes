[<=== Back](/README.md)

# Reading 05 Notes

## CSS

### What is CSS?
CSS stands for "Cascading Style Sheets", and is used to style websites with such functions as font sizing and coloring, backgrounds, color and sizing of headings and links, sidebars, and animations.

### CSS Syntax
CSS rules open with a **selector** from the HTML being styled. For example: headers, paragraphs, and images. The selector is followed by a set of curly braces `{ }`. Inside the braces there are one or more **declarations**. Declarations come as a pair - a **property** and a **value**, separated by a colon followed by a space. The declaration is closed with a semicolon.
> h1 {
    color: red;
    font-size: 5em;
}

### CSS Modules and Specifications
CSS has such a large variety of uses that the language is broken into *modules*. Find a list of modules [here](https://developer.mozilla.org/en-US/docs/Web/CSS).

Specifications for different versions of CSS are maintained by the CSS Working Group to ensure that while new features are added, older versions used on older websites still function.

## How to Add CSS
There are three ways of inserting a style sheet:
- External CSS
- Internal CSS
- Inline CSS

### External CSS
 External CSS allows the user to keep a separate file for styling which is referenced inside the HTML page in the head section, inside the `<link>` element.
An external style sheet can be created in any text editor, and must be saved with a .css extension.

### Internal CSS
Internal CSS is usually used if only one HTML page has a unique style. In this case, the style is defined inside the `<style>` element, inside the head section.

### Inline CSS
An inline style can be used to style a single element, and is added as an attribute to that element in the HTML page. It can contain any CSS property.

#### Cascading Order
What happens when there is more than one style specified for an HTML element?

Styles will "cascade" using the following rules, from highest priority to lowest
1. Inline style
2. External and internal style (in head section)
3. Browser default

## Color in CSS
Colors can be added to HTML elements in three different ways
- The color name, if it is a fairly common color name
- HTML color codes: [Color Picker](https://htmlcolorcodes.com/color-picker/)
- RGB values