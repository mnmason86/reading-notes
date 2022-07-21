[<=== Back](README.md)

# Functional Programming

## [Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

**What is functional programming?**

Functional programming is "a style of building the structure and elements of computer programs that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data"

**What is a pure function and how do we know if something is a pure function?**

Pure functions return the same result if given the same arguments, and does not cause any observable side effects.

**What are the benefits of a pure function?**

Pure functions are stable, consistent, and predictable

**What is immutability?**

> Unchanging over time, or unable to be changed.

The state of the data cannot change after it is created.

**What is Referential transparency?**

In a program, an expression may be replaced by its value without changing the result of the program

example:

`x = 2 + (3 * 4)`   

The subexpression (3*4) can be replaced with any other expression having the same outcome


[Node JS Tutorial for Beginners #6 - Modules and require()](https://www.youtube.com/watch?v=xHLd36QoS4k)

**What is a module?**

Logical sections of code that can be separated into their own files and called upon to perform tasks. 

**What does the word ‘require’ do?**

Takes in a path to a module that allows use of that module's exported code in other files.

**How do we bring another module into the file the we are working in?**

`let potato = require ('./file_name')`

What do we have to do to make a module available?

Use `module.exports = ` with whatever part of the code you want to be available in other files.