[<=== Back](../README.md)

# HTML & CSS by Jon Duckett
*Summarized*

# Chapter 7: Forms
p.144-175

To collect information from a user, a form can be used. Forms are created using the `<form>` element.
Information is sent in name/value pairs. The name is a property of the input, and the value is the user's response.

> Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server.

Some types of form control:

- Pre-determined options: Radio Button, Checkbox, Drop Down List Box, Multiple Select Box
- Input options with buttons: File input, Submit button, Image button
- Added options with HTML5: Form validation, date input, email and url input, search input

# Chapter 14: Lists, Tables, and Forms
p.330-357

There are some CSS properties that are specifically used to control the appearance of lists, tables, and forms.

### Lists

List markers can be given different appearances using the `list-style-type` and `list-style` image properties.

`list-style-image` is used to change bullet points to an image instead.

`list-style-position` indicates whether the marker should appear on the inside of the outside of the box containing the main points.

`list-style` acts like a shorthand for list styles. You can express the marker's style, image, and position properties in any order.

### Tables

Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent.

`empty-cells` can be used to specify whether or not an empty cell's borders should be shown.

`border-spacing` is used to control the distance between adjacent cells

### Forms

Forms work best with styles that make them feel more interactive, and are easier to use if the form controls are vertically aligned using CSS

# JavaScript & JQUERY by Jon Duckett
*Summarized*

# Chapter 6: Events
p.243-292

> When you browse the web, your browser registers different types of events. It's the browser's way of saying, "Hey, this just happened." Your script can then respond to these events

- Interactions create events
- Events trigger code
- Code responds to users

There are many types of events. A list of different types can be found on p.246-247

## How Events Trigger JavaScript Code

1. Select the element note(s) you want the script to respond to.
2. Indicate which event on the selected node(s) will trigger the response.
3. State the code you want to run when the even occurs.

## Event Handlers

> Event handlers let you indicate which event you are waiting for on any particular element. There are three types of event handlers.

1. HTML Event Handlers (*bad practice, but may be seen in older code*)
2. Traditional DOM event handlers
  - `*element*.on*event* = *functionName*;`
3. DOM level 2 event listeners
  - `*element*.addEventListener(*'event', functionName [, Boolean]*);`

  ***Question: Can you explain more about 'anonymous functions'?***


