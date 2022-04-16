[<=== Back](README.md)

# JavaScript
Summarized from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

> JavaScript is a lightweight, interpreted, compiled programming language with first-class functions. While it is most well-known as the scripting language for Web pages, many non-browser environments also use it, such as Node.js, Apache CouchDB, and Adobe Acrobat.

*Java* is a very different programming language.

## Input and Output in JavaScript

## JavaScript Variables
Variables  are "containers for storing data", and are declared in four ways:
- `var`
- `let`
- `const`
- using nothing

For older browsers, the `var` option should be used. Keywords `let` and `const` were added to JS in 2015.

For general rules, use `const`. If the variable can change, use `let`.

Example:
> `const price1 = 5;`
`const price2 = 6;`
`let total = price1 + price2;`

### JavaScript Identifiers
All **variables** bust be identified with unique names called **identifiers**. 

Some general rules for variable names:
> -Names can contain letters, digits, underscores, and dollar signs.
- Names must begin with a letter
- Names can also begin with $ and _ 
- Names are case sensitive (y and Y are different variables)
- Reserved words (like JavaScript keywords) cannot be used as names

For more rules on variables, visit [W3Schools](https://www.w3schools.com/js/js_variables.asp)