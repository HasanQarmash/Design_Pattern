# Design Patterns in Java by Hasan Qarmash

# Introduction
Software design patterns are essential tools for developers, encountered during software development.
By understanding and applying these patterns, developers can create more robust, maintainable, and scalable software systems.. Design patterns can be categorized into three main types: Creational, Structural, and Behavioral patterns.



![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://s3.amazonaws.com/media-p.slid.es/uploads/2772005/images/11497649/pasted-from-clipboard.png)

> [!NOTE]
> - Design pattern providing proven solutions to common problems
> - Using design patterns too frequently can lead to several disadvantages like  Reduced Readability ,  patterns that involve multiple classes or interfaces can increase memory usage and processing time and antoher disadvantegs.

# Table of Contents
1. [Creational Patterns](#creational-patterns)
    - [Singleton Pattern](#singleton-pattern)
    - [Factory Method Pattern](#factory-method-pattern)
    - [Abstract Factory Pattern](#abstract-factory-pattern)
    - [Builder Pattern](#builder-pattern)
    - [Prototype Pattern](#prototype-pattern)
2. [Structural Patterns](#structural-patterns)
    - [Adapter Pattern](#adapter-pattern)
    - [Bridge Pattern](#bridge-pattern)
    - [Composite Pattern](#composite-pattern)
    - [Decorator Pattern](#decorator-pattern)
    - [Facade Pattern](#facade-pattern)
    - [Flyweight Pattern](#flyweight-pattern)
    - [Proxy Pattern](#proxy-pattern)
3. [Behavioral Patterns](#behavioral-patterns)
    - [Chain of Responsibility Pattern](#chain-of-responsibility-pattern)
    - [Command Pattern](#command-pattern)
    - [Interpreter Pattern](#interpreter-pattern)
    - [Iterator Pattern](#iterator-pattern)
    - [Mediator Pattern](#mediator-pattern)
    - [Memento Pattern](#memento-pattern)
    - [Observer Pattern](#observer-pattern)
    - [State Pattern](#state-pattern)
    - [Strategy Pattern](#strategy-pattern)
    - [Template Method Pattern](#template-method-pattern)
    - [Visitor Pattern](#visitor-pattern)

# Creational Patterns
Creational design patterns provide solutions to instantiate an object in the best possible way for specific situations.

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://s3.amazonaws.com/media-p.slid.es/uploads/2772005/images/11497754/pasted-from-clipboard.png)

## Singleton Pattern
Ensure a class has only one instance and provide a global point of access to it.
```java
public class Singleton {
    private static Singleton instance;

    private Singleton() {}

    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}
```
## Builder Pattern 
Builder is a creational design pattern that lets you construct complex objects step by step. The pattern allows you to produce different types and representations of an object using the same construction code.

If you are not using multiple threads and only the main thread is involved in creating objects, the primary benefit of the Builder Pattern shifts from avoiding inconsistent state due to concurrent modifications to providing a clean and flexible way to construct complex objects. The Builder Pattern helps in managing the construction process of objects with many optional parameters, making the code more readable, maintainable, and scalable.
### Problem  

``` java 
// Creating a house with all attributes
//without builder design pattern
        House house = new House(4, 2, "Gable", true, false);
//with builder design pattern
   // Creating a house with all attributes using builder pattern
        House house = new House.HouseBuilder()
                .setWindows(4)
                .setDoors(2)
                .setRoof("Gable")
                .setGarage(true)
                .setSwimmingPool(false)
                .build();
        System.out.println(house);

        // Creating a house with only some attributes using builder pattern
        House simpleHouse = new House.HouseBuilder()
                .setWindows(2)
                .setRoof("Flat")
                .build();
        System.out.println(simpleHouse);
    }
}

```
 new House(4, 2, "Gable", true, false);
 This constructer is not clear if I want to modify it I cannot do so easily because I do not understand what these values ​​return to such as 2 and 4, but when I used builder  I became able to understand what these values ​​return to because I entered them via set/get methods 
 ### another problem 
   When constructing complex objects that require step-by-step initialization of many fields and nested objects, the initialization code often becomes cumbersome and difficult to manage. There are two common approaches to handle this:

1. Subclass Proliferation: Creating numerous subclasses to represent different combinations of parameters. This leads to:

 * A large number of subclasses.
 * Difficulty in maintaining and extending the class hierarchy.
2. Monstrous Constructor: Using a single, giant constructor in the base class with all possible parameters. This results in:

 * Constructor calls becoming unwieldy and hard to read.
 * Most parameters being unused in many cases, making the code less clean and maintainable.
These approaches can lead to significant issues in terms of code readability, maintainability, and scalability.

 # Structural Patterns 

 ## Adapter Pattern




