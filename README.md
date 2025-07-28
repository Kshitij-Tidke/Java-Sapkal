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

# Why Develop 
- The Java TM programming language is designed to meet the challenges of application development in the context of heterogeneous, network-wide distributed environments. Paramount among these challenges is secure delivery of applications that consume the minimum of system resources, can run on any hardware and software platform, and can be extended dynamically.

- The Java programming language originated as part of a research project to develop advanced software for a wide variety of network devices and embedded systems. The goal was to develop a small, reliable, portable, distributed, real-time operating platform. When the project started, C++ was the language of choice. But over time the difficulties encountered with C++ grew to the point where the problems could best be addressed by creating an entirely new language platform. 

# Hello World!

## Code
```
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
## Explanation:
**public class HelloWorld { ... }:**  
This defines a class named HelloWorld. In Java, all code resides within classes. The public keyword means the class is accessible from anywhere.

**public static void main(String[] args) { ... }:**      
This is the main method, which serves as the entry point for Java applications. 
- **public:** The method is accessible from anywhere.
- **static:** The method belongs to the class itself, not to an instance of the class. This allows the Java Virtual Machine (JVM) to call main without creating an object of HelloWorld.
- **void:** The method does not return any value.
- **main:** This is the standard name for the entry point method.
- **String[] args:** This declares an array of String objects named args, which can be used to receive command-line arguments when the program is executed.

**System.out.println("Hello, World!");:**      
This statement prints the string "Hello, World!" to the console.
- **System:** A class in the java.lang package that provides access to system resources.
- **out:** A static member of the System class, representing the standard output stream.
- **println():** A method of the PrintStream class (which out is an instance of) that prints a line of text to the console and then moves the cursor to the next line.

<br/>

# Basic of programming language

## Literal 
- A literal is a notation representing a fixed, constant value directly within the source code of a program. 
- Unlike variables, which are symbols that can hold different values during program execution, literals represent the value itself. 

```
int numberLiteral = 10;
String stringLiteral = "Hello World!";
char charaterLiteral = 'A';
boolean booleanLiteral = true;
```

## Variables(Fields)
- Variables are containers used to store data values.
- They are fundamental building blocks for any program, allowing you to manipulate and reference information during execution. 

### (Naming)  Rules while declaring/ initializing variables:
- Names are case-sensitive (speed ≠ Speed).
- Must start with a letter, _, or $ (but avoid _ and $ by convention).
- Cannot start with a digit or contain whitespace.
- Cannot be a Java keyword (e.g., class, int, for).

### Best Practices must be follow:
- Use meaningful names (speed, not s).
- Use lowerCamelCase for variables (e.g., gearRatio, currentGear).
- Use UPPER_SNAKE_CASE for constants (e.g., MAX_SPEED).

# Types of Variables:
### Instance Variables (Non-static fields):
- Belong to an object (each object gets its own copy).
- Declared inside the class, but outside methods.
- No static keyword.
```
class Bicycle {
    int currentSpeed;  // Instance variable
}
```

### Class Variables (Static fields)
- Belong to the class, not individual objects.
- Only one copy exists for all objects.
- Declared with the static keyword.
```
class Bicycle {
    static int numGears = 6;  // Class variable
    // All bicycles share the same value of numGears.
}

```

### Local Variables
- Declared inside methods, used for temporary tasks.
- Only exist while the method is running.
- Cannot be static.
```
void ride() {
    int speedIncrease = 5;  // Local variable
}
```

### Parameters:
- Variables passed into methods or constructors.
- Used to send data to a method.
```
void setSpeed(int newSpeed) {  // Parameter
    currentSpeed = newSpeed;
}
```

# Data Types:
## Primitive Data Types: 
These are fundamental, pre-defined data types built directly into the Java language. They store raw values directly in memory and have fixed sizes.
```
Integers:
- byte      (8-bit)         -128 to 127                         Saves memory in large arrays; good for small numbers
- short     (16-bit)        -32,768 to 32,767                   Saves memory when int is too big   
- int       (32-bit)        -2,147,483,648 to 2,147,483,647     Default for whole numbers; can be unsigned (Java 8+)
- long      (64-bit)        -2⁶³ to 2⁶³-1                       For large integers; supports unsigned (Java 8+)

Floating-point numbers:
- float     (32-bit)        7 decimal digits precision          For decimal numbers where memory is limited
- double    (64-bit)        15 decimal digits                   Default for decimal numbers

Characters:
- char      (16-bit)        Unicode: \u0000 to \uffff (0 to 65,535)

Boolean:
- boolean   (1-bit)         true or false
```

### Additional 
An integer literal is of type long if it ends with the letter L or l; otherwise it is of type int. It is recommended that you use the upper case letter L because the lower case letter l is hard to distinguish from the digit 1.

### Underscores in Number Literal
- Java allows you to use underscores (_) in numbers to make them more readable, like separating thousands — but there are rules.

- You can use underscores:
    - Between digits
    - To make long numbers easier to read
    - Valid (Allowed)
```
int x = 1_000_000;        // OK: looks like 1,000,000
float pi = 3.14_15F;      // OK: between digits after the decimal
int hex = 0x5_2;          // OK: in hexadecimal, between digits
int bin = 0b1010_0101;    // OK: in binary numbers
```
## Invalid (Not Allowed)
### Float 
```
float pi1 = 3_.1415F;     // ❌ Wrong: underscore before dot
float pi2 = 3._1415F;     // ❌ Wrong: underscore after dot
```

### Int 
```
int x = _1000;     // ❌ Wrong: starts with _
int y = 1000_;     // ❌ Wrong: ends with _
```

### Long
```
long ssn = 123_45_6789_L;   // ❌ Wrong: underscore before L
```

### Hexadecimal Value
```
int hex = 0_x52;    // ❌ Wrong: underscore in 0x
int hex2 = 0x_52;   // ❌ Wrong: underscore right after 0x
int hex3 = 0x5_2;   // ✔️ OK
```