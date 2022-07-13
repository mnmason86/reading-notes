[<=== Back](README.md)

# Passing Functions as Props

## React Docs - [Lists and Keys](https://reactjs.org/docs/lists-and-keys.html)

**What does .map() return?**
`.map()` returns a new array that is the same length as the one it is called on, but with different value which may or may not be related to the original array.

**If I want to loop through an array and display each value in JSX, how do I do that in React?**
You can use the map() function to loop through the array, and return an html element for each item in the new array. 

**Each list item needs a unique ____.**
Key. 
**What is the purpose of a key?**
> "Keys help react identify which items have changed, are added, or are removed."

They should be given to elements inside the array. It is not recommended to use indexes as keys if the order of the items may change.

example:
```
const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li key={number.toString()}>
    {number}
  </li>
);
```

## The Spread Operator
*Summarized from* [How to Use the Spread Operator(...) in JavaScript by: Dr. Derek Austin](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

**What is the spread operator?**
> "The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function's arguments"

It 'spreads' the array into separate arguments.

**List 4 things that the spread operator can do.**
- Copy an array
- Combine arrays / objects
- Add to state in React
- Use Math functions

**Give an example of using the spread operator to combine two arrays.**
```
let cars = ['camry', 'sentra'];
let trucks = ['tundra', 'titan'];

let vehicles = [...cars,...trucks];

vehicles = ['camry','sentra','tundra','titan'];
```

**Give an example of using the spread operator to add a new item to an array.**
```
let numbers = [2,3];
let moreNumbers = [0,1,...numbers];

moreNumbers = [0,1,2,3];
```

**Give an example of using the spread operator to combine two objects into one.**
```
let animalOne = {dog: 'woof'}
let animalTwo = {cat: 'meow'}
let animals = {...animalOne, ...animalTwo}

animals = {dog: 'woof', cat: 'meow'}
```

## How to Pass Functions Between Components

**In the video, what is the first step that the developer does to pass functions between components?**
**In your own words, what does the increment function do?**
**How can you pass a method from a parent component into a child component?**
**How does the child component invoke a method that was passed to it from a parent component?**


#### More on Passing Functions as Props

- [React Tutorial through ‘Declaring a Winner’](https://reactjs.org/tutorial/tutorial.html)
- [React Docs - Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)
