# Technical Interview Questions in Java

This document contains a collection of frequently asked questions commonly posed in technical interviews for software developers using Java. The questions are organized by topic to facilitate preparation.

## Table of Contents

1. [Java Fundamentals](#java-fundamentals)
2. [Java 17](#java-17)
3. [Object-Oriented Programming (OOP)](#object-oriented-programming)
4. [Data Structures](#data-structures)
5. [Concurrency and Multithreading](#concurrency-and-multithreading)
6. [Exception Handling](#exception-handling)
7. [Streams and Lambdas](#streams-and-lambdas)
8. [JDBC and Databases](#jdbc-and-databases)
9. [Spring Framework](#spring-framework)
10. [Spring Boot](#spring-boot)
11. [Spring WebFlux](#spring-webflux)
12. [Spring Data](#spring-data)
13. [Apache Kafka](#apache-kafka)
14. [Best Practices and SOLID Principles](#best-practices-and-solid-principles)

---

## Java Fundamentals

1. **What is the JVM and how does it work?**
    - The Java Virtual Machine (JVM) is an abstract machine that enables the execution of Java code. It converts bytecode into instructions that can be executed by the underlying hardware.

2. **What is the difference between `==` and `equals()` in Java?**
    - `==` compares object references, while `equals()` compares object values.

---

## Java 17

1. **What are `sealed classes` in Java 17 and how are they used?**
    - `Sealed classes` allow a class or interface to control which other classes or interfaces may extend it. They are used to restrict the set of derived classes, providing a more secure and explicit way to handle class hierarchies.

2. **What are `record types` in Java 17 and what are their main advantages?**
    - `Record types` are a new feature for defining immutable classes concisely. They provide a simple way to create classes that only store data, reducing boilerplate code for methods like `equals`, `hashCode`, and `toString`.

3. **How does the new `Pattern Matching` API work in Java 17?**
    - `Pattern Matching` simplifies working with data types by combining pattern matching with `instanceof` and value unpacking. It allows for more readable and less error-prone code.

---

## Object-Oriented Programming

1. **What are the four pillars of object-oriented programming?**
    - Encapsulation, inheritance, polymorphism, and abstraction.

2. **How is inheritance implemented in Java?**
    - By using the `extends` keyword for classes and `implements` for interfaces.

---

## Data Structures

1. **What is an `ArrayList` and how does it differ from a `LinkedList`?**
    - `ArrayList` is a list based on a dynamic array, while `LinkedList` is a list based on linked nodes.

2. **How does a `HashMap` work in Java?**
    - `HashMap` stores key-value pairs and uses a hash table to optimize access.

---

## Concurrency and Multithreading

1. **What is a `Thread` in Java and how is one created?**
    - A `Thread` is an independent unit of execution. It can be created by extending the `Thread` class or implementing the `Runnable` interface.

2. **What is `synchronized` and when is it used?**
    - The `synchronized` keyword is used to prevent multiple threads from accessing a shared resource simultaneously.

---

## Exception Handling

1. **What is the difference between `Exception` and `Error` in Java?**
    - `Exception` is a condition that can be handled, whereas `Error` represents a serious problem that should not be handled.

2. **What is a `try-catch-finally` block and how does it work?**
    - Blocks of code used to handle exceptions, where `finally` is always executed regardless of whether an exception is thrown or not.

---

## Streams and Lambdas

1. **What is a lambda expression in Java?**
    - A lambda expression is an anonymous function that can be used to implement methods defined in functional interfaces.

2. **What is a `Stream` in Java and how is it used?**
    - A `Stream` is a sequence of elements that supports aggregate operations such as filtering and mapping.

---

## JDBC and Databases

1. **How does a Java application connect to a database using JDBC?**
    - By using the `DriverManager` class to obtain a connection and execute SQL queries.

2. **What is a `PreparedStatement` and why is it preferable to use it?**
    - It is a class that allows for the execution of parameterized SQL queries in a more secure and efficient manner.

---

## Spring Framework

1. **What is Spring Framework and what are its main modules?**
    - A framework for Java application development. Its main modules include Core, MVC, AOP, and Data Access.

2. **What is dependency injection (DI) in Spring?**
    - A design pattern that allows for automatic management of object dependencies.

---

## Spring Boot

1. **What are `Spring Boot Starters` and how do they facilitate development?**
    - `Spring Boot Starters` are pre-configured dependency sets that simplify the integration of common technologies into an application. Each starter provides basic configuration for a specific technology, such as `spring-boot-starter-web` for web applications.

2. **How is external configuration managed in Spring Boot?**
    - External configuration can be managed through `application.properties` or `application.yml` files, environment variables, and command-line arguments. Spring Boot supports profiles (`@Profile`) to handle environment-specific configurations.

---

## Spring WebFlux

1. **How does Spring WebFlux differ from Spring MVC?**
    - Spring WebFlux is designed for reactive, non-blocking applications using the reactive programming model with `Flux` and `Mono`. Spring MVC, on the other hand, is synchronous and blocking, based on the traditional request-response model.

2. **What are `Mono` and `Flux` in the context of Spring WebFlux?**
    - `Mono` and `Flux` are types provided by the Reactor project for handling asynchronous data streams. `Mono` represents a data stream that can emit 0 or 1 item, while `Flux` can emit 0 to N items.

3. **How are errors handled in a Spring WebFlux application?**
    - Errors in Spring WebFlux can be handled using `onErrorResume`, `onErrorReturn`, or `doOnError` to intercept and manage exceptions reactively.

---

## Spring Data

1. **What is Spring Data JPA and how does it simplify data access?**
    - Spring Data JPA is a part of Spring Data that provides a simplified implementation of the data access layer using JPA (Java Persistence API). It offers an API for creating repositories that eliminate the need for repetitive data access code.

2. **How is the `@Query` annotation used in Spring Data JPA?**
    - The `@Query` annotation allows for defining JPQL or native SQL queries in repository methods, providing finer control over query execution and database operation customization.

3. **What are `Specifications` and how are they used in Spring Data JPA?**
    - `Specifications` provide a flexible way to build dynamic queries in JPA using the specification pattern. They are used to create queries based on search criteria that can be combined and reused.

---

## Apache Kafka

1. **How does Spring Boot integrate with Apache Kafka for message handling?**
    - Spring Boot provides support for Kafka through the `spring-kafka` dependency. It offers automatic configuration for Kafka consumers and producers, as well as annotations like `@KafkaListener` for consuming messages.

2. **What are `Kafka Streams` and how are they used in data processing?**
    - `Kafka Streams` is a stream processing library that allows for the creation of real-time data processing applications using Kafka. It provides APIs for building stream processing applications easily.

3. **How is partition and replica management configured in a Kafka cluster?**
    - Partitions and replicas are configured at the topic level in Kafka. Partitions allow parallel processing and scalability, while replicas provide fault tolerance. Configuration is done through Kafka's configuration file properties or Kafka's management interface.

---

## Best Practices and SOLID Principles

1. **What is the Single Responsibility Principle (SRP)?**
    - The Single Responsibility Principle states that a component (such as a class) should have only one reason to change. In other words, it should have a single responsibility or function within the system. This enhances modularity and facilitates code maintainability.

2. **What is the Open/Closed Principle (OCP)?**
    - The Open/Closed Principle indicates that software entities (such as classes, modules, and functions) should be open for extension but closed for modification. This means you can add new functionality without changing existing code, which helps to prevent introducing errors into tested code.

3. **What is the Liskov Substitution Principle (LSP)?**
    - The Liskov Substitution Principle states that objects of a derived class should be able to replace objects of the base class without altering the correctness of the program. In other words, subclasses should be able to function in place of their superclasses without causing errors or unexpected behavior.

4. **What is the Interface Segregation Principle (ISP)?**
    - The Interface Segregation Principle states that an interface should be specific to a particular client, rather than a general interface that covers all functionalities. Clients should not be forced to depend on interfaces they do not use, which makes the system easier to implement and maintain.

5. **What is the Dependency Inversion Principle (DIP)?**
    - The Dependency Inversion Principle states that high-level modules should not depend on low-level modules, but both should depend on abstractions. Additionally, abstractions should not depend on details; details should depend on abstractions. This promotes flexibility and code reuse by decoupling dependencies.
