[<=== Back](../README.md)

# JavaScript & JQUERY by Jon Duckett
*Summarized*

p.449-486

## Chapter 10 - Error Handling and Debugging

### Order Of Execution

> To find the source of an error, it helps to know how scripts are processed. The order in which statements are executed can be complex; some tasks cannot complete until another statement or function has been run.

### Execution Contexts

> The JavaScript interpreter uses the concept of **execution contexts**. There is one global execution context; plus, each function creates a new execution context. They correspond to variable scope.

Global scope: variables declared outside a function can be used anywhere. Variables not declared with `let` or `const` are placed in the global scope.

Function-Level scope: Variables declared within a function can only be used in that function.

### The Stack

> The JavaScript interpreter processes one line of code at a time. When a statement needs data from another function, it stacks (or piles) the new function on top of the current task. (similar to the stack in MTG!)

### A Debugging Workflow

> Debugging is about deduction: eliminating potential causes of an error. 

1. Where is the problem?
- Look at the error message, check how far the script is running, use breakpoints where things are going wrong.
2. What exactly is the problem?
- When you set breakpoints you can see if the variables around them have the values you would expect them to, break down/break out parts of the code to test smaller pieces of the functionality, check the number of parameters for a function, or the number of items in an array.

### Debugger Keyword

> You can create a breakpoint in your code using just the `debugger` keyword. When the developer tools are open, this will automatically create a breakpoint. The `debugger` keyword can also be placed within a conditional statement so that it only triggers the breakpoint if the condition is met.


> If you know that you may get an error, you can handle it gracefully using the `try, catch, finally` statements. Found on p. 481
