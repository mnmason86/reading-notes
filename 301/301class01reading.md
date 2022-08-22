[<=== Back](/README.md)

# Component-Based Architecture

*Summarized from* [Tutorials Point](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm)

### What is a 'component'?

> A component is "a unit of composition with a contractually specified intervace and explicit context dependencies only."

It is a small piece of code that fills a certain part of the UI.

### What are the characteristics of a component?

- Reusable: May be designed for a specific task, but are usually designed to be used in different situations.
- Replaceable: May be substituted with similar components.
- Not context-specific: Designed to operate in different environments and/or contexts.
- Extensible: Can be extended for new behavior
- Encapsulated: Do not expose details of the internal processes, variables, or state.
- Independent: Designed to have minimal dependencies on other components.

### What are the advantages of using component-based architecture?

Component-based architectures are easy to deploy and develop, reduce cost, are reusable, enhance system reliability, system maintenance, and evolution, and are independent and flexible.

# What is Props and How to Use it in React
*Summarized from* [ITNEXT](https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0)

### What is 'props' short for?

> 'Props' is short for 'properties', and is used for "passing data from one component to another".

### How are props used in React?

Props are arguments passed into React components, similar to they way that arguments are passed into a function. 

#### Arguments passed into a function:

```
const addition = (firstNum, secondNum) => {  
  return firstNum + secondNum; 
};
```

#### Arguments passed into a React component:

```
const ChildComponent = (props) => {  
  return <p>I'm the 1st child!</p>; 
};
```

### What is the flow of props?

Props can only be passed one way - from parent to child, and are 'read-only'.


#### More on Components and Props

- [React Tutorial through ‘Passing Data Through Props’](https://reactjs.org/tutorial/tutorial.html)
- [React Docs - Hello world](https://reactjs.org/docs/hello-world.html)
- [React Docs - Introducing JSX](https://reactjs.org/docs/introducing-jsx.html)
- [React Docs - Rendering elements](https://reactjs.org/docs/rendering-elements.html)
- [React Docs - Components and props](https://reactjs.org/docs/components-and-props.html)