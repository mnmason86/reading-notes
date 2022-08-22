[<=== Back](//README.md)

# Inheritance

*from [Java Tutorials](https://docs.oracle.com/javase/tutorial/java/concepts/)*

## What is Inheritance?

Inheritance is when a subclass *inherits* commonly used state and behaviors from another class (its *superclass*). Each subclass may have only one superclass, but a superclass may have an unlimited number of subclasses.

> A subclass inherits all the *members* (fields, methods, and nested classes) from its superclass. Constructors are not members, so they are not inherited by subclasses, but the constructor of the superclass can be invoked from the subclass.

*Take care to properly document state and behavior of your superclass, as that code will not appear in the source file for its subclasses.*

## What is an Interface?

An interface is a programs interaction with the oustide world. 

In Java, an interface is a reference type that can only contain: constants, method signatures, default methods, static methods, and nested types.

In order to use an interface, you write a class that implements that interface. 

> Implementing an interface allows a class to become more formal about the behavior it promises to provide. Interfaces form a contract between the class and the outside world, and this contract is enforced at build time by the compiler. If your class claims to implement an interface, all methods defined by that interface must appear in its source code before the class will successfully compile.

Example code for an interface:

```
interface Bicycle {

    //  wheel revolutions per minute
    void changeCadence(int newValue);

    void changeGear(int newValue);

    void speedUp(int increment);

    void applyBrakes(int decrement);
}
```
Example code to implement an interface:

```
class ACMEBicycle implements Bicycle {

    int cadence = 0;
    int speed = 0;
    int gear = 1;

   // The compiler will now require that methods
   // changeCadence, changeGear, speedUp, and applyBrakes
   // all be implemented. Compilation will fail if those
   // methods are missing from this class.

    void changeCadence(int newValue) {
         cadence = newValue;
    }

    void changeGear(int newValue) {
         gear = newValue;
    }

    void speedUp(int increment) {
         speed = speed + increment;   
    }

    void applyBrakes(int decrement) {
         speed = speed - decrement;
    }

    void printStates() {
         System.out.println("cadence:" +
             cadence + " speed:" + 
             speed + " gear:" + gear);
    }
}
```

## What is a Package?

> A package is a namespace that organizes a set of related classes and interfaces. 

A package is similar to folders on a computer where related items are placed in a folder together. Importing packages allows the programmer to focus on the design of an application instead of the specific infrastructure required to make it work.