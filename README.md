# Basic

## What is program
- It is a set of instructions that tells a computer what to do.
- These instructions, written in a programming language, are used to perform specific tasks, from simple calculations to complex operations like online banking or data analysis.

## What is programming language
- It is a set of rules, symbols, and syntax used to write instructions that a computer can understand and execute

## Types of programming language
###    1. Statically Typed Languages:
    - Variable data types are checked during **compile-time**, before the program is executed.
    - Java, C++, C.

    ```
    #include <stdio.h>

    int main() {
        int num = 10;         // 'num' is statically typed as an integer

        // we can't do this
        // int num = "10"       // Error: invalid conversion from 'char*' to 'int'
        printf("Number: %d\n", num);

        return 0;
    }
    ```

### 2.  Dynamically Typed Languages:
    - Variable data types are checked at **runtime**, while the program is executing.
    - Python, JavaScript, PHP.

    ```
    num = 10          # num is an integer
    print("Number:", num)

    num = "Ten"       # num is now a string
    print("Now num is:", num)
    ```

<br/>

# Java 

### Simple: 
Java was designed to be easy to learn and use. It removes complex features like pointers, operator overloading, and multiple inheritance (found in C++), making code easier to read and maintain.

### Object-Oriented:
Java is built around the concept of objects and classes. Everything in Java is part of a class, which makes it easy to build modular, reusable, and maintainable code. Concepts like inheritance, encapsulation, and polymorphism are central.

### Multithreaded

Java allows programs to perform several tasks simultaneously using multithreading. This is crucial for applications that require real-time interaction, like games or servers.

### Dynamic

Java is designed to adapt to an evolving environment. Classes are loaded into memory dynamically at runtime, meaning new code can be loaded and executed without recompiling the whole application.

### Architecture Neutral

Java code is compiled into an intermediate form known as bytecode, which can be executed on any platform with a Java Virtual Machine (JVM). This means Java code isn't tied to a specific hardware or OS architecture.

### Portable

Because Java is architecture-neutral and the JVM handles platform-specific tasks, Java programs can run on any device that has a JVM. This portability makes Java ideal for cross-platform development.

### High Performance

While Java is not as fast as languages like C or C++, its performance is quite good due to Just-In-Time (JIT) compilers, optimized memory management, and efficient bytecode execution by the JVM.

### Robust

Java is designed to eliminate error-prone situations. It has strong memory management, exception handling, and type-checking mechanisms, which make applications more stable and reliable.

### Secure

Java provides a secure execution environment through features like:

    - No direct memory access (no pointers),
    - A bytecode verifier to check code before execution,
    - The security manager to control access to system resources, making it ideal for networked and web applications.