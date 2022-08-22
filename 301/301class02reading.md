[<=== Back](../README.md)

# State and Props

## React Lifecycle
*Summarized from* [React:Component Lifecycle Events by: Joshua Blankenship](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

Methods that are able to be used on components are called **lifecycle events**. They allow updating of the UI and application states. 

Based off of the lifecycle image *React Lifecycle Events*, `render` happens before `componentDidMount`.

**Mounting** is the first thing to happen in the lifecycle of React. The three phases of a component's lifecycle are 1) Mounting 2) Updating 3) Unmounting.

> "The constructor for a React component is called before it is mounted."

Order of events: `constructor`, `render`, `componentDidMount`, `React updates`, `componentWillUnmount`

`componentDidMount()` is a method which is invoked immediately after a component is mounted, and allows the developer to add any additional effects that will be triggered inside the method, such as API calls.

## React State vs. Props
*Summarized from* [Web Dev Simplified](https://www.youtube.com/watch?v=IYvD9oBCuJI)

### What types of things can you pass in the props?

You can pass the same types of things into props that you would pass into a function, such as variables.

### What is the big difference between props and state?

Props are passed *into* a component, whereas state is handled *inside* the component. Props are handled *outside* the component, and *must* be updated outside of the component.

### When do we re-render our application?

Any time the state changes, the application is re-rendered. 

### What are some examples of things that we could store in state?

Some examples of things that could be stored in *state* are counters to be updated or information in a form (input, checkbox, select box), things that need to be updated and re-rendered.

#### More on State and Props
- [React Docs - State and Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)
- [React Docs - Handling Events](https://reactjs.org/docs/handling-events.html)
- [React Tutorial through 'Developer Tools'](https://reactjs.org/tutorial/tutorial.html)
- [React Bootstrap Documentation](https://react-bootstrap.github.io/)
- [Bootstrap Cheatsheet](https://getbootstrap.com/docs/5.0/examples/cheatsheet/)
- [Bootstrap Shuffle - a class 'sandbox'](https://bootstrapshuffle.com/classes)
- [Netlify](https://www.netlify.com/)

##### Things I want to know more about:

When you call `super(props)`, what props are we accessing? From where?
