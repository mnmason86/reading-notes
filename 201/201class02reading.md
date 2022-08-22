[<=== Back](../README.md)

# HTML & CSS by Jon Duckett
*Summarized*

## Chapter 2: Text
p.40-61
- **Headings**: There are 6 levels of headings, `<h1>`-`<h6>`. `<h1>` is the largest.
- **Paragraphs**: Paragraphs are indicated with the `<p>` tag. Separate paragraphs with separate `<p>` tags. Do not indent.
- **Bold & Italic**: Surround text with a `<b>` tag to make it appear bold, and an `<i>` tag to make it appear italic.
- **Superscript & Subscript**: Use `<sup>` for superscript, and `<sub>` for subscript.
- **White Space**: Extra white space (2 or more spaces) are used to make code easier to read, but will be ignored by the browser
- **Line Breaks & Horizontal Rules**: To add a line break in the middle of a paragraph, use `<br />`. To add a horizontal rule between lines of text, use `<hr />`.

### Semantic Markup

- **Strong & Emphasis**: For strong emphasis in a text reader, use `<strong>`. For regular emphasis, use `<em>`.
- **Quotations**: Blockquotes(`<blockquote>`) is used for longer quotes that take up an entire paragraph. For shorter quotes that sit within a paragraph, use `<q>`.
- **Abbreviations & Acronyms**: For either abbreviations or acronyms, use `<abbr>`. A title attribute can be used to specify the full term.
- **Citations & Definitions**: To cite a source, use `<cite>` - the text will be italic. For a new term which is being defined, use `<dfn>`.
- **Author Details**: To contain contact details for the author of the page, use the `<address>` tag around the contact information.
- **Changes to Content**: The `<ins>` element can be used to show content that has been inserted into a document, while the `<del>` element can show text that has been deleted from it. The `<s>` element is used to display content that is no longer accurate, and will appear with a line through the text.

## Chapter 10: Introducing CSS
p.226-245
> "CSS allows you to create rules that control the way that each individual box (and the contents of that box) is presented."

CSS associates style rules with HTML elements. A rule contains a *selector* and a *declaration*. Declarations have two parts: a *property* and a *value*.

CSS may appear in the *head* of an HTML document, or in a separate document.

# JavaScript & JQUERY by Jon Duckett
*Summarized*

## Chapter 2: Basic JavaScript Instructions
p.53-84

> A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a **statement*.

When a script needs to temporarily store a bit of information, *variables* are used.

The three data types in JavaScript are **string**, **number**, and **boolean**.

An *array* store a list of values. Ex: 

> `var colors;`
> `colors = ['white', 'black', 'custom'];`

#### Expressions & Operators

> An **expression** evaluates into a single value. 
> Expressions rely on things called **operators**; they allow programmers to create a single value from one or more values.

## Chapter 4: Decisions and Loops
p.145-162

#### Decision Making

Decisions in script are places where a determination needs to be made about which script will run next. Using a flow chart will help to visualize what decisions need to be made.

#### Evaluating Conditions & Conditional Statements

> There are twocomponents to a decision. 1 - An expression is evaluated, which returns a value. 2. A conditional statement says what to do in a given situation.

### Comparison Operators: Evaluating Conditions

When a comparison operator is used, the result is rendered as *boolean* (true or false).

Some comparison operators:
- `==` Equal to
- `!=` Not equal to
- `>` Greater than
- `<` Less than
- `===` Strict equal to
- `!==` Strict not equal to
- `>=` Greater than or equal to
- `<=` Less than or equal to

In a comparison, the operand can be an expression containing more than one variable.

### Logical Operators

Allow you to compare results of more than one comparison operator.

Some logical operators:
- `&&` Logical 'and' (tests more than one condition)
- `||` Logical 'or' (tests at least one condition)
- `!` Logical 'not' (takes a single Boolean value and inverts it)

#### If Statements

**If Statements** evaluate a condition. If the statement is true, the subsequent code is executed. 

#### If-Else Statements

**If/Else Statements** evaluate a condition. If the statement is *true*, the first code block is executed. If the statement is *false*, the second code block is executed.

