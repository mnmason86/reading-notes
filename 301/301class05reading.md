[<=== Back](README.md)

## React Docs - [Thinking in React](https://reactjs.org/docs/thinking-in-react.html)

**What is the single responsibility principle and how does it apply to components?**

A component should, ideally, only do one thing. If it starts getting too large and doing multiple things, those should be broken down into sub-components.

**What does it mean to build a ‘static’ version of your application?**

A static version of an app that renders the UI, but has no interactivity. The code is all written in one file, and no *state* is defined

**Once you have a static application, what do you need to add?**

The ability to trigger changes in the underlying data - this is done with *state*.

**What are the three questions you can ask to determine if something is state?**

1. Is it passed in from a parent via props? If so, it probably isn't state.
2. Does it remain unchanged over time? If so, it probably isn't state.
3. Can you compute it based on any other state or props in your component? If so, it isn't state.

**How can you identify where state needs to live?**

- Identify components that render something based on that state.
- Find a common owner component
- Either the common owner or another component higher up in the hierarchy should own the state.
- If it isn't clear where to set the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.


## [Higher-Order Functions](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)

**What is a “higher-order function”?**

> "Functions that operate on other functions, either by taking them as arguments or by returning them, are called *higher-order functions*.

**Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?**

Line two of the greaterThan function returns a boolean after evaluating whether m is greater than n (which is passed into the function as an argument).

**Explain how either map or reduce operates, with regards to higher-order functions.**

Array.map() is a higher-order function because it takes in an array, and a callback function that is performed for every element of the passed-in array, and returns a new array accordingly.

