# Reading 05 Notes

## CSS

### What is CSS?
CSS stands for "Cascading Style Sheets", and is used to style websites with such functions as font sizing and coloring, backgrounds, color and sizing of headings and links, sidebars, and animations.

### CSS Syntax
CSS rules open with a **selector** from the HTML being styled. For example: headers, paragraphs, and images. The selector is followed by a set of curly braces "{ }". Inside the braces there are one or more **declarations**. Declarations come as a pair - a **property** and a **value**, separated by a colon followed by a space. The declaration is closed with a semicolon.
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

**External CSS** allows the user to keep a separate file for styling which is referenced inside the HTML page in the head section, inside the "<link>" element.