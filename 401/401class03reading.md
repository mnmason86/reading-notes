[<=== Back](../README.md)

# Java Basics

## [Primitives vs. Objects](https://www.baeldung.com/java-primitives-vs-objects)
*from Baeldung.com*

> Java has a two-fold type system consisting of primitives such as *int*, *boolean*, and reference types such as *Integer*, *Boolean*. Every primitive type corresponds to a reference type.

Each primitive type corresponds to a reference type (object), and each object contains a single value of the corresponding primitive type.

Primitive type variable memory:
- boolean: 1 bit
- byte: 8 bits
- short, char: 16 bits
- int, float: 32 bits
- long, double: 64 bits

Reference type memory:
- Boolean: 128 bits
- Byte: 128 bits
- Short, Char: 128 bits
- Integer, Float: 128 bits
- Long, Double: 192 bits

## [Exceptions in Java](https://docs.oracle.com/javase/tutorial/essential/exceptions/index.html)
*from Oracle Java Documentation*

> An exception is an event that occurs during the execution of a program that disrupts the normal flow of instructions.

When an error occurs, an object is created and given to the runtime system. The object contains information about the error.
When an error occurs, the runtime system searches the call stack to find a method that can handle the exception, then the error is thrown at that place in the call stack.

> Valid Java programming language code must honor the *Catch or Specify Requirement*. This means that code that might throw certain exceptions must be enclosed by either of the following:
  - A `try` statement
  - A method that specifies that it can throw the exception. Provides a `throws` cause that lists the exception

  **Types of Exceptions**

  - Checked Exception: Exceptional conditions that a well-written application should anticipate and recover from. All exceptions are *checked exceptions*, except for those indicated by `Error, RuntimeException`, and their subclasses.
  - Error: External errors that the application usually cannot anticipate or recover from. Errors are *not subject* to the `catch` or `specify requirement`.
  - Runtime Exception: Internal exceptions that the application usually cannot anticipate or recover from. Usually indicate programming bugs. Runtime exceptions are *not subject* to the `catch` or `specify requirement`
  *Errors and runtime exceptions are collectively known as **unchecked exceptions***

  **How to Throw Exceptions**

  > Before you can catch an exception, some code somewhere must throw one.

  Exceptions are always thrown with the `throw` statement. The `throw` statement requires a single argument: a throwable object. Example:

```
  public Object pop() {   
    Object obj;   
    
    if (size == 0) {   
        throw new EmptyStackException();   
    }   
   
    obj = objectAt(size - 1);   
    setObjectAt(size - 1, null);   
    size--;   
    return obj;   
  }   
```

You can only throw objects that inherit from the `java.lang.Throwable` class.

## [Scanning](https://docs.oracle.com/javase/tutorial/essential/io/scanning.html)
*from Oracle Java Documentation*

> Objects of type `Scanner` are useful for breaking down formatted input into tokens and translating individual tokens according to their data type.

A Scanner is a simple text scanner which can parse primitive types and strings using regular expressions - uses white space to separate tokens.

Example:

input:
```
String input = "1 fish 2 fish red fish blue fish";
     Scanner s = new Scanner(input).useDelimiter("\\s*fish\\s*");
     System.out.println(s.nextInt());
     System.out.println(s.nextInt());
     System.out.println(s.next());
     System.out.println(s.next());
     s.close();
```
output:

1   
2   
red   
blue   