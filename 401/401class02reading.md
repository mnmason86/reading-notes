[<=== Back](README.md)

# More Java Basics

## [A Guide to Java Loops](https://www.baeldung.com/java-loops)

> Looping is a feature which facilitates the execution of a set of instructions until the controlling *Boolean-expression* evaluates to *false*

**[FOR loop](https://www.baeldung.com/java-for-loop) & [WHILE loop](https://www.baeldung.com/java-while-loop)**

For loops & while loops work the same as they do in JavaScript, with a slightly different syntax:
```
for (int i = 0; i < array.length; i++){
  //do something here
}

while (Boolean-expression) {
  //do something here
}
```

**[DO-WHILE loop](https://www.baeldung.com/java-do-while-loop)**

Do While loops work the same as while loops, except that the condition evaluation happens after the first iteration of the loop
```
do {
  statement;
} while (Boolean-expression);
```

## [Arrays](https://www.tutorialspoint.com/java/java_arrays.htm)

In Java, an array stores a collection of elements of the same type. Arrays must be given a data type (int, char, String, etc.)

To create an array in Java, the following syntax is used:

`dataType[] newArray = {value0, value1, value2,...}` 
OR 
`dataType [] newArray = new dataType[arraySize]` 
OR 
`newArray = new dataType[arraySize]`

FOR loops and FOR EACH loops are often used to traverse arrays. Arrays may be passed into or returned from methods.