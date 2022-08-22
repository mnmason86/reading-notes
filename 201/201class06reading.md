[<=== Back](../README.md)

# JavaScript & JQUERY by Jon Duckett
*Summarized*

## Chapter 3: Object Literals
p. 100-105

> Objects group together a set of variables and functions to create a model of something you would recognize from the real world. In an object, variables and functions take on new names.

>> If a variable is part of an object, it is called a **property**.

>> If a function is parto of an object, it is called a **method**.

> Like variables and named functions, properties and methods have a name and a value. In an object, that name is called a **key**. Objects cannot have two keys with the same name.

### Literal Notation

Literal notation is the easiest and most popular way to create objects.

```
var hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,

  checkAvailability: function() {
    return this.rooms - this.booked;
  }
};
```

In the above example, the **this** keyword is used to indicate that it is using the **rooms** and **booked** properties of *this* object. 

### Accessing an Object and Dot Notation

> You access the properties or methods of an object using dot notation. You can also access properties using square brackets. The period is known as the **member operator**. The property or method on its right is a member of the object on its left. 

`var hotelName = hotel.name;`

OR

`var hotelName = hotel['name'];`


## Chapter 5: Document Object Models
p. 183-242

> The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and hos JavaScript can access and update the contents of a web page while it is in the browser window.

> The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules. It is implemented by all major browswer makers, and covers two primary areas:

1. Making a model of the HTML page
* When the browser loads a web page, it creates a model of the page in memory. The DOM specifies the way in which the browser should structure this model using a **DOM tree**. The DOM is called an object model because the model (the DOM tree) is made of objects. Each object represents a different part of the page loaded in the browser window. (Example of DOM tree on p. 187).
2. Accessing and changing the HTML page.
* The DOM also defines methods and properties to access and update each object in this model, which in turn updates what the user sees in the browser. You will hear people call the DOM an *8Application Programming Interface (API)**. User interfaces let humans interact with programs; API's let programs (and scripts) talk to each other. The DOM states what your script can ask the browser about the current page, and how to tell the browser to update what is being shown to the user.

### Working with the DOM Tree

Three common ways to select an individual element:
1. `getElementById()`
* Uses the value of an element's `id` attribute.
2. `querySelector()`
* Uses a CSS selector, and returns the first matching element.
3. Individual elements can also be selected by traversing from one element to another within the DOM tree.

Three common ways to select multiple elements:
1. `getElementsByClass()`
*  Selects all elements that have a specific value for their class attribute.
2. `getElementsByTagName()`
* Selects all elements that have the specified tag name.
3. `querySelectorAll()`
* Uses a CSS selector to select all matching elements.

Traversing between element nodes
1. `parentNode`
* Selects the parent of the current element notes (which will return just one element).
2. `previousSibling / nextSibling`
* Selects the previous or next sibling from the DOM tree.
3. `firstChild / lastChild`
* Select the first or last child of the current element.

### Caching DOM Queries

> Methods that find elements in the DOM tree are called DOM queries. When you need to work with an element more than once, you should use a variable to store the result of this query.

### NodeLists: DOM Queries That Return More Than One Element

> When a DOM method *can* return more than one element, it returns a NodeList - even if it only finds one matching element.

> A NodeList is a collection of element nodes. Each node is given an index number, like an array.

While NodeLists look like arrays and are numbered the same way, they *are not* arrays. They are a type of object called a **collection**.

> When you have a NodeList, you can loop through each node in the collection and apply the same statements to each.
