[<=== Back](/README.md)

# HTML & CSS by Jon Duckett
*Summarized*

## Chapter 6: Tables
p.126-145

### Table Structure and Headings
`<table>` is used to create a table, with contents written out row by row.
`<tr>` is used for each row of a table, and `<td>` is for each cell.
`<th>` is used for the table heading. Adding multiple heading elements inside of a row creates columns.

Even if cells are empty, `<td>` or `<th>` should still be used to represent the empty cell.

### Spanning

To span a cell across multiple columns, use the `colspan` attribute with `="number of rows to span"`.

To span a cell across multiple rows, use the `rowspan` attribute with `="number of rows to span"`.

For long tables, use `<thead>` to indicate the 'head' of the table, `<tbody>` for the main body of the table, and `<tfoot>`for the 'footer' of the table.


# JavaScript & JQUERY by Jon Duckett
*Summarized*

## Chapter 3: Functions, Methods, and Objects
p. 106-144 

### Creating An Object: Constructor Notation

> The **new** keyword and the object constuctor create a blank object. You can then add properties and methods to the object. 

` let newObject = new Object();`

Properties and methods can be added using dot notation or square brackets.

To delete a property: `delete object.property;`
To clear a property:  `object.property = '':`

### Creating Many Objects: Constructor Notation

> Sometimes you will want several objects to represent similar things. Object constructors can use a function as a template for creating objects. First, create the template with the object's properties and methods.

Example:

```
  function Hotel (name, rooms, booked){
    this.name = name;
    this.rooms = rooms;
    this.booked = booked;

    this. checkAvailability = functions (){
      return this.rooms - this.booked;
    };
  }
  ```

  ### This (It Is A Keyword)

> The keyword **this** is commonly used inside functions and objects. Where the function is declared alters what `this` means. ***It always refers to one object, usually the object in which the function operates.***

### Arrays Are Objects

> Arrays are actually a special type of object. The hold a related set of key/value pairs(like all objects), but the key for each value is its index number.


### Arrays Of Objects & Objects In Arrays

> You can combine arrays and objects to create complex data structures: Arrays can store a series of objects (and remember their order). Objects can also hold arrays (as values of their properties).

There are three grups of built-in objects:

**Browser Object Model**: Creates a model of the browser tab or window.
**Document Object Model**: Creates a model of the current web page.
**Global JavaScript Objects**: Do not form a single model. They are a group of individual objects that relate to different parts of the JavaScript language, and usually start with a capital letter.

A list of Global JavaScript Objects can be found on p.137