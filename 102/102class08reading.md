[<=== Back](../README.md)

# Operators and Loops
## Operators
Summarized from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators) 
### Comparison Operators
> A comparison operator compares its operands and returns a logical value based on whether the camparison is true. 

Operands can be numerical, string, logical, or object values.

### Types of Comparison Operators

- `==` Equal
- `!=` Not equal
- `===` Strict equal
- `!==` Strict not equal
- `>` Greater than
- `>=` Greater than or equal to
- `<` Less than
- `<=` Less than or equal to

### Assignment Operators
> An assignment operator assigns a value to its left operand based on the value of its right operand. The simple assignment operator is `=`, which assigns the value of its right operand to its left operand. 
`x = f()` is an assignment expression that assigns the falue of `f()` to `x`.

## Loops
Summarized from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)

### For Statements
> A `for` loop repeats until a specified condition evaluates to false.

> `for` `([initialExpression]; [conditionExpression]; [incrementExpression])`
  `statement` 

### While Statements

> A `while` statement executes its statements as long as a specified condition evaluates to `true`. A `while` statement looks as follows:

`while` (condition)  
    statement

> If the `condition` becomes `false`, statement within the loop stops executing and control passes to the statement following the loop.

> The condition test occurs *before* `statement` in the loop is executed. If the condition returns `true`, statement is executed and the condition is tested again. If the condition returns `false`, execution stops, and control is passed to the statement following `while`.