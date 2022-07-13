[<=== Back](README.md)

# React and Forms

## [React Docs - Forms](https://reactjs.org/docs/forms.html)

**What is a ‘Controlled Component’?**

> "An input form element whose value is controlled by React"

**Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why?**

By making the React state the 'source of truth' for the input, the event handler will run on every key stroke to update the React state, not only when the form is submitted. 

**How do we target what the user is entering if we have an event handler on an input field?**

By setting the value of the input field to `this.state.value` 


## [The Conditional (Ternary) Operator Explained](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)

The Ternary operator is a shorthand replacement for an 'if' statement, and can be executed in one line of code.

Syntax: `condition ? value if true : value if false`

example:
```
if(x===y){
  console.log(true);
} else {
  console.log(false);
}
```

**BECOMES**

```
(x===y) ? console.log(true) : console.log(false)
```

#### Bookmark and Review
- [React Bootstrap - Forms](https://react-bootstrap.github.io/forms/overview/)
- [React Docs - conditional rendering](https://reactjs.org/docs/conditional-rendering.html)