# Design Patterns in Java by Hasan Qarmash

## Introduction
Software design patterns are essential tools for developers, encountered during software development.
By understanding and applying these patterns, developers can create more robust, maintainable, and scalable software systems.. Design patterns can be categorized into three main types: Creational, Structural, and Behavioral patterns.

> [!IMPORTANT]
>  providing proven solutions to common problems

## Table of Contents
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

## Creational Patterns
Creational design patterns provide solutions to instantiate an object in the best possible way for specific situations.

### Singleton Pattern
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
