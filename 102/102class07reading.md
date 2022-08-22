[<=== Back](../README.md)

# Programming with JavaScript

## Control Flow
Summarized from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Glossary/Control_flow)

>The *control flow* is the order in which the computer executes statememts in a script.

Generally, code executes from top to bottom unless the code encounters a structure that changes the control flow, such as a conditional or a loop.

**Reminder**: conditional structures include `if`...`else`

## JavaScript Functions
Summarized from [W3Schools](https://www.w3schools.com/js/js_functions.asp)

>A function is a block of code designed to perform a particular task. A JS function is executed when "something" calls it.

For example:

> `function myFunction(p1, p2) {`
  `return p1 * p2;   // The function returns the product of p1 and p2`
`}`

## JavaScript Function Syntax
JS functions are defined with the `function` keyword, followed by a name (you choose the name), followed by parentheses `()`. Function names can contain letters, digits, underscores, and `$` signs. Parentheses *may* include parameter names separated by commas:
`(parameter1,parameter2)`. The code to be executed by the function is placed inside curly brackets.

Function **arguments** are the values received by the function when it is invoked.

In other programming languages, **function** is much the same as **procedure** or **subroutine**

### Function Invocation
> The code inside the function will execute when "something" **invokes** the function:
- When an event occurs (user clicks a button)
- When it is invoked from JS code
- Automatically (self-invoked)

### Function Return
>When JS reaches a `return` statement, the function will stop executing. If the function was invoked from a statement, JS will "return" to execute the code after the invoking statement. Functions often compute a **return value**. The return value is "returned" back to the caller

> `let x = myFunction(4, 3);   // Function is called, return value will end up in x`

`function myFunction(a, b) {`
  `return a * b;             // Function returns the product of a and b`
`}`

#### The `()` Operator
Accessing a function without () will return the function definition (object) instead of the function result.

#### Local Variables
Variables declared within a JS function become **local** to the function, and can only be accessed from within the function. Since local variables are only recognized inside their functions, variables with the same name can be used in different functions. They are created when a function starts, and deleted when the function is complete.

## JavaScript Operators
`=` is the **assignment** operator - it assignes a value to a variable.

`+` is the **addition** operator - adds numbers

`*` is the **multiplication** operator - multiplies numbers

The `+` operator can also be used to add or "concatenate" strings.

> `let text1 = "John";  let text2 = "Doe";  let text3 = text1 " " + text 2;`
> Result will be `John Doe`

More on operators at [W3Schools](https://www.w3schools.com/js/js_operators.asp)