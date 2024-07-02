# 100 Important Java Interview Questions

<div>
<p align="center">
<a href="https://devinterview.io/questions/web-and-mobile-development/">
<img src="https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/github-blog-img%2Fweb-and-mobile-development-github-img.jpg?alt=media&token=1b5eeecc-c9fb-49f5-9e03-50cf2e309555" alt="web-and-mobile-development" width="100%">
</a>
</p>

#### You can also find all 100 answers here 👉 [Devinterview.io - Java](https://devinterview.io/questions/web-and-mobile-development/java-interview-questions)

<br>

## 1. Explain the main idea behind _Java_ and the concept of _Write Once, Run Anywhere_.

**Java** is a high-level, object-oriented programming language designed to be **platform-independent**. Its core philosophy is encapsulated in the concept of "**Write Once, Run Anywhere**" (WORA), which revolutionized software development by enabling cross-platform compatibility.

### Write Once, Run Anywhere (WORA)

WORA is a principle that allows Java code to be written once and run on any device or operating system without modification. This is achieved through several key components:

#### 1. Java Virtual Machine (JVM)

The **JVM** acts as an abstraction layer between Java code and the underlying hardware or operating system. It interprets and executes Java bytecode, ensuring consistent behavior across different platforms.

#### 2. Bytecode

Java source code is compiled into platform-independent **bytecode**, which can be executed by any JVM, regardless of the underlying system architecture.

#### 3. Standard Library

Java provides a comprehensive **standard library** that offers cross-platform capabilities for common tasks like file handling and networking.

### How Java Achieves WORA

1. **Platform Independence**: Java bytecode can run on any device with a compatible JVM, from smartphones to supercomputers.

2. **JVM Customization**: Each operating system has a tailored JVM version, ensuring WORA functionality across diverse environments.

3. **Garbage Collection**: Automatic memory management reduces the risk of memory leaks and simplifies development across platforms.

4. **Security**: Java's design excludes direct memory manipulation through pointers, enhancing security across different systems.

### Code Example: "Hello, World!" in Java

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

This simple program demonstrates Java's WORA principle. It can be compiled and run on any system with a JVM, producing the same output:

1. Compile: `javac HelloWorld.java`
2. Run: `java HelloWorld`
3. Output: `Hello, World!`

The same bytecode can be executed on Windows, Linux, macOS, or any other platform with a compatible JVM, showcasing the practical implementation of "Write Once, Run Anywhere" in Java.
<br>

## 2. What are the _main features_ of _Java_?

Java's robustness makes it stand out with its powerful features.

### Core Features of Java

1. **Platform Independence**: Write once, run anywhere (WORA) through Java Virtual Machine (JVM).

2. **Object-Oriented**: Emphasizes objects and classes, promoting `encapsulation`, `inheritance`, and `polymorphism`.

3. **Strong Typing**: Variables are strongly typed, reducing ambiguity and potential for errors.

4. **Security**: Offers a secure platform with features such as a `bytecode verifier` and a `security manager`.

5. **Automatic Memory Management**: Centralized memory allocation and automatic `garbage collection`, reducing the risk of memory leaks.

6. **Concurrency**: Supports `multi-threading`, enabling concurrent execution and efficient multitasking.

7. **Architecture-Neutral**: Promotes scalability across different hardware and software configurations.

8. **Dynamic**: Supports dynamic loading of classes and dynamic compilation.

9. **Simplicity**: Easy-to-learn syntax and standard libraries simplify software development.

10. **Portability**: Java's "compile once, run anywhere" philosophy enables it to function across diverse platforms.

11. **High Performance**: Utilizes `Just-In-Time (JIT)` compilation, combining the flexibility of bytecode with the performance of machine code.

### Additional Java Features

#### Exception Handling
Java provides a robust system to capture and handle runtime errors:

```java
try {
    // Code that may throw an exception
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero");
}
```

#### Rich Standard Library
Java offers a comprehensive set of APIs for common tasks:

```java
import java.util.ArrayList;
import java.util.List;

List<String> list = new ArrayList<>();
list.add("Java");
list.add("is");
list.add("powerful");
```

#### Networking Capabilities
Java simplifies network programming:

```java
import java.net.URL;
import java.net.HttpURLConnection;

URL url = new URL("https://api.example.com/data");
HttpURLConnection conn = (HttpURLConnection) url.openConnection();
conn.setRequestMethod("GET");
// ... handle the connection
```

#### Integration with Other Languages
Java leverages the Java Native Interface (JNI) to support native code:

```java
public class NativeMethodExample {
    native void nativeMethod();

    static {
        System.loadLibrary("native");
    }

    public static void main(String[] args) {
        new NativeMethodExample().nativeMethod();
    }
}
```

#### Advanced Concurrency Utilities
Java provides high-level concurrency APIs:

```java
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

ExecutorService executor = Executors.newFixedThreadPool(5);
executor.submit(() -> {
    System.out.println("Task executed by " + Thread.currentThread().getName());
});
```

<br>

## 3. Can you list some _non-object-oriented_ features of _Java_?

While Java is primarily an **object-oriented** language, it also incorporates several non-object-oriented features, allowing for multi-paradigm development:

### Primitive Data Types

Java supports **primitive data types** such as `int`, `boolean`, `char`, etc., which are not objects and provide simple value storage.

```java
int number = 42;
boolean isTrue = true;
char letter = 'A';
```

### Static Methods and Variables

**Static members** belong to the class rather than instances, allowing for utility functions and shared data.

```java
public class MathUtils {
    public static final double PI = 3.14159;
    
    public static int add(int a, int b) {
        return a + b;
    }
}
```

### Package-Level Access

Java's **default (package-private) access modifier** limits visibility to within the same package, providing a non-OO way to control access.

```java
package com.example;

class PackagePrivateClass {
    void packagePrivateMethod() {
        // Accessible only within the same package
    }
}
```

### Utility Classes

Java allows the creation of **utility classes** with only static methods, which don't require instantiation.

```java
public final class StringUtils {
    private StringUtils() {} // Prevent instantiation
    
    public static boolean isEmpty(String str) {
        return str == null || str.trim().isEmpty();
    }
}
```

### Single Inheritance

Java supports **single inheritance** for classes, which can be seen as a limitation compared to full object-oriented languages that allow multiple inheritance.

```java
public class Animal {}
public class Mammal extends Animal {} // Only one superclass allowed
```

### Procedural Programming Style

Java allows for a more **procedural style** of programming within methods, especially in the `main` method.

```java
public class Main {
    public static void main(String[] args) {
        int x = 5;
        int y = 10;
        int sum = x + y;
        System.out.println("Sum: " + sum);
    }
}
```

### Interfaces

While interfaces are object-oriented, Java's **functional interfaces** and **default methods** provide a way to achieve some functional programming paradigms.

```java
@FunctionalInterface
public interface Calculator {
    int calculate(int a, int b);
    
    default void printResult(int result) {
        System.out.println("Result: " + result);
    }
}
```
<br>

## 4. Describe the difference between _JDK_, _JRE_, and _JVM_.

The **JVM** (Java Virtual Machine) is the cornerstone of Java's "write once, run anywhere" philosophy. It's an abstract computing machine that provides a runtime environment in which Java bytecode can be executed.

#### Key Functions

- **Bytecode Interpretation**: Translates Java bytecode into machine-specific instructions.
- **Memory Management**: Handles memory allocation and deallocation, including **garbage collection**.
- **JIT Compilation**: Compiles frequently executed bytecode to native machine code for improved performance.
- **Exception Handling**: Manages the execution of `try-catch` blocks and handles runtime exceptions.
- **Security**: Implements the Java security model to protect against malicious code.

### JRE: Java Runtime Environment

The **JRE** (Java Runtime Environment) is the minimum environment required to execute a Java application. It consists of the JVM, core libraries, and other supporting files.

#### Components

- **JVM**: An implementation of the JVM specification for a particular platform.
- **Core Libraries**: Essential Java API classes (e.g., `java.lang`, `java.util`).
- **Supporting Files**: Configuration files and resources needed for Java applications.

### JDK: Java Development Kit

The **JDK** (Java Development Kit) is a superset of the JRE, providing everything needed for Java application development.

#### Key Components

- **JRE**: Includes a complete Java Runtime Environment.
- **Development Tools**: 
  - `javac`: The Java compiler
  - `java`: The Java application launcher
  - `javadoc`: Documentation generator
  - `jdb`: Java debugger
- **Additional Libraries**: Extra APIs for development (e.g., `javax` packages).

### Relationship and Usage

- **Development**: Use the JDK to write, compile, and debug Java code.
- **Deployment**: Use the JRE to run Java applications on end-user machines.
- **Execution**: The JVM, part of both JRE and JDK, actually runs the Java program.

### Code Example

Here's a simple demonstration of how these components interact:

```java
// This file is named HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

To compile and run this program:

1. Use the JDK's `javac` to compile:
   ```
   javac HelloWorld.java
   ```
   This creates `HelloWorld.class` containing bytecode.

2. Use the JRE's `java` to run:
   ```
   java HelloWorld
   ```
   The JVM within the JRE executes the bytecode.
<br>

## 5. What is the role of the _ClassLoader_?

The **ClassLoader** is a crucial component in Java's runtime environment, responsible for loading class files into memory.

### Key Functions

1. **Loading Classes**: Finds and reads the binary representation of a class or interface.

2. **Linking Classes**:
   - **Verification**: Ensures the loaded class adheres to Java language and JVM specifications.
   - **Preparation**: Allocates memory for class variables and initializes them with default values.
   - **Resolution**: Replaces symbolic references with direct references to other classes.

3. **Initializing Classes**: Executes the static initializers and initializes static fields of the class.

### Types of ClassLoaders

1. **Bootstrap ClassLoader**: 
   - Written in native code (C++)
   - Loads core Java API classes from `rt.jar` or modules in Java 9+

2. **Extension ClassLoader** (Platform ClassLoader in Java 9+):
   - Loads classes from `lib/ext` directory or specified by `java.ext.dirs`

3. **Application ClassLoader**:
   - Loads user-defined classes from the classpath

4. **Custom ClassLoaders**:
   - User-defined loaders for specific loading behaviors

### Delegation Hierarchy

ClassLoaders follow the **delegation principle**:

1. When a class is requested, the loader first delegates to its parent.
2. If the parent can't load the class, the current loader attempts to load it.
3. This continues up to the Bootstrap ClassLoader.

### Dynamic Class Loading

Java provides methods for runtime class loading:

- `Class.forName(String className)`
- `ClassLoader.loadClass(String name)`

These methods enable dynamic behaviors like plugin systems.

### Code Example

```java
public class ClassLoaderDemo {
    public static void main(String[] args) throws Exception {
        // Using Class.forName
        Class<?> stringClass = Class.forName("java.lang.String");
        System.out.println("Loaded: " + stringClass.getName());

        // Using ClassLoader
        ClassLoader classLoader = ClassLoaderDemo.class.getClassLoader();
        Class<?> mathClass = classLoader.loadClass("java.lang.Math");
        System.out.println("Loaded: " + mathClass.getName());

        // Displaying ClassLoader hierarchy
        ClassLoader current = ClassLoaderDemo.class.getClassLoader();
        while (current != null) {
            System.out.println(current.getClass().getName());
            current = current.getParent();
        }
        System.out.println("Bootstrap ClassLoader");
    }
}
```
<br>

## 6. What is the difference between a _path_ and a _classpath_ in _Java_?

In Java, the **classpath** and **path** serve different purposes:

### Classpath

The **classpath** is a parameter that tells the Java Virtual Machine (JVM) where to find compiled Java classes (`.class` files) and packages during runtime. It's crucial for the JVM to locate and load classes when executing a Java program.

#### Key aspects of classpath:

- It's specific to Java runtime environment
- Can include directories, JAR files, and ZIP archives
- Used by the JVM to resolve class dependencies

#### Setting the classpath:

1. **Command-line**: Using `-cp` or `-classpath` option
   ```bash
   java -cp .:/path/to/some.jar MyApp
   ```

2. **Environment variable**: Setting `CLASSPATH`
   ```bash
   export CLASSPATH=.:/path/to/some.jar
   ```

3. **In IDEs**: Most IDEs provide GUI tools to manage classpath

4. **Build tools**: Maven and Gradle manage classpath automatically

### Path

The **path** is a system environment variable that specifies directories where executable programs are located. It's used by the operating system to find executables when you run commands in the terminal or command prompt.

#### Key aspects of path:

- It's a general operating system concept, not specific to Java
- Contains directories, not individual files
- Used by the OS to locate executable files

#### Setting the path:

```bash
export PATH=$PATH:/new/directory
```

### Comparison

| Aspect | Classpath | Path |
|--------|-----------|------|
| Purpose | Locates Java classes | Locates executable programs |
| Scope | Java runtime | Operating system |
| Content | Directories, JAR files, ZIP archives | Directories only |
| Used by | Java Virtual Machine | Operating system |

### Example

Consider a Java application with the following structure:

```
/MyProject
    /src
        /com/example
            Main.java
    /lib
        external.jar
```

After compilation:

```
/MyProject
    /bin
        /com/example
            Main.class
    /lib
        external.jar
```

To run this application:

1. **Path**: Ensure Java executable is in the system path
   ```bash
   export PATH=$PATH:/path/to/java/bin
   ```

2. **Classpath**: Set classpath to include compiled classes and external JAR
   ```bash
   java -cp ./bin:./lib/external.jar com.example.Main
   ```

### Best Practices

1. Use relative paths when possible for portability
2. Leverage build tools like Maven or Gradle for dependency management
3. Keep classpath entries minimal to avoid conflicts and improve performance
4. Use wildcard (*) judiciously to include all JARs in a directory

### Common Issues

- **ClassNotFoundException**: Often due to missing classpath entries
- **NoClassDefFoundError**: Can occur if a required class is not found at runtime
- **Version conflicts**: When multiple versions of a class are in the classpath

<br>

## 7. Can you explain the difference between an _int_ and an _Integer_ in _Java_?

In Java, **int** and **Integer** are two distinct data types with unique properties and use cases.

### Key Distinctions

#### int
- **Primitive data type**
- Represents whole numbers between $-2^{31}$ and $2^{31} - 1$
- Memory allocation: Fixed $32$ bits (or $4$ bytes)
- Instantiation: Direct, no constructor required
- Default value: $0$
- Performance: Generally faster due to direct value storage
- Usage in generics: Not allowed

#### Integer
- **Wrapper class** for the primitive `int`
- Provides additional functionality via class methods
- Memory allocation: Variable, typically more than `int`
- Instantiation: Through constructor, auto-boxing, or `valueOf()`
- Default value: `null` (if not assigned)
- Performance: Slightly slower due to object overhead
- Usage in generics: Allowed

### Code Example: int and Integer

```java
public class IntVsInteger {
    public static void main(String[] args) {
        int primitiveInt = 10;  // Direct assignment
        Integer objInt = Integer.valueOf(20);  // Preferred instantiation method

        // Auto-boxing (conversion from primitive to object)
        Integer autoBoxed = primitiveInt;

        // Unboxing (conversion from object to primitive)
        int unboxed = objInt;

        System.out.println("Primitive int: " + primitiveInt);
        System.out.println("Integer object: " + objInt);
        System.out.println("Auto-boxed Integer: " + autoBoxed);
        System.out.println("Unboxed int: " + unboxed);

        // Demonstrating default values
        int defaultInt;
        Integer defaultInteger;
        System.out.println("Default int: " + (defaultInt = 0));  // Compile-time error without assignment
        System.out.println("Default Integer: " + defaultInteger);  // Prints "null"

        // Using Integer methods
        System.out.println("Max int value: " + Integer.MAX_VALUE);
        System.out.println("Binary representation of 20: " + Integer.toBinaryString(20));
    }
}
```
<br>

## 8. What are _wrapper classes_ in _Java_?

**Wrapper classes** in Java allow you to work with primitive data types as objects. They are particularly useful when working with generic collections or when using features that require objects, such as **Java Bean properties**.

Wrapper classes not only provide a way to convert primitives to and from objects but also offer various utility methods specific to each primitive type.

### Core Wrapper Classes

| Primitive | Wrapper Class | Conversion Methods | Primitive Example | Wrapper Example |
| --- | --- | --- | --- | --- |
| `boolean` | `Boolean` | `.valueOf()` <br> `.parseBoolean()` <br> `.booleanValue()` | `true` | `Boolean.TRUE` |
| `byte` | `Byte` | `.valueOf()` <br> `.parseByte()` <br> `.byteValue()` | `123` | `Byte.valueOf((byte)123)` |
| `char` | `Character` | `.valueOf()` <br> `.charValue()` | `'a'` | `Character.valueOf('a')` |
| `short` | `Short` | `.valueOf()` <br> `.parseShort()` <br> `.shortValue()` | `123` | `Short.valueOf((short)123)` |
| `int` | `Integer` | `.valueOf()` <br> `.parseInt()` <br> `.intValue()` | `123` | `Integer.valueOf(123)` |
| `long` | `Long` | `.valueOf()` <br> `.parseLong()` <br> `.longValue()` | `123L` | `Long.valueOf(123L)` |
| `float` | `Float` | `.valueOf()` <br> `.parseFloat()` <br> `.floatValue()` | `123.45f` | `Float.valueOf(123.45f)` |
| `double` | `Double` | `.valueOf()` <br> `.parseDouble()` <br> `.doubleValue()` | `123.45` | `Double.valueOf(123.45)` |

### Use Cases for Wrapper Classes

#### 1. Collections

Generic collections in Java require objects, not primitives. Wrapper classes allow you to use primitives in these collections.

```java
List<Integer> numbers = new ArrayList<>();
numbers.add(5);  // Autoboxing: int to Integer
int num = numbers.get(0);  // Unboxing: Integer to int
```

#### 2. Nullability

Wrapper classes can represent the absence of a value using `null`, which primitives cannot.

```java
Integer age = null;  // Valid
int primitiveAge = null;  // Compilation error
```

#### 3. Java Beans

In Java Beans, properties are typically represented using wrapper classes to allow for unset values.

```java
public class Customer {
    private Integer age;  // Can be null if age is unknown
    
    public Integer getAge() {
        return age;
    }
    
    public void setAge(Integer age) {
        this.age = age;
    }
}
```

#### 4. Utility Methods

Wrapper classes provide useful utility methods for their respective types.

```java
String binaryString = Integer.toBinaryString(42);
int maxValue = Integer.MAX_VALUE;
boolean isDigit = Character.isDigit('7');
```
<br>

## 9. What does it mean that _Java_ is a _statically typed_ language?

Java being a **statically typed language** means that the type of a variable is known at compile time. This characteristic requires explicit declaration of a variable's type before it can be used.

### Key Characteristics of Static Typing in Java

#### Type Safety
- All data objects have a specific type
- Types cannot change unless explicitly converted
- Helps prevent type-related errors at runtime

#### Performance Efficiency
- Compile-time type determination allows for code optimization
- Reduces runtime overhead associated with type checking

#### Predictability
- Known types improve code reliability and maintainability
- Easier to reason about code behavior

#### Enhanced Development Experience
- IDEs can provide better auto-completion and error detection
- Facilitates early identification of type-related issues

#### Code Clarity
- Explicitly defined types enhance code readability
- Makes the intended use of variables more apparent

### Example: Static Typing in Java

```java
public class StaticTypingDemo {
    public static void main(String[] args) {
        // Explicit type declarations
        int number = 10;
        String text = "Hello, Java!";
        double decimal = 3.14;

        // Type-safe operations
        int sum = number + 5;  // Valid: int + int
        String greeting = text + " Welcome!";  // Valid: String concatenation

        // Compile-time type checking
        // int result = number + text;  // Compilation error: incompatible types

        // Type conversion (casting)
        double convertedNumber = (double) number;  // Explicit casting from int to double

        System.out.println("Sum: " + sum);
        System.out.println("Greeting: " + greeting);
        System.out.println("Converted number: " + convertedNumber);
    }
}
```
<br>

## 10. Is _Java_ a pure _object-oriented language_? Why or why not?

Java is **not** a pure object-oriented language. While it incorporates many object-oriented programming (OOP) principles, it retains some elements from procedural programming.

### Object-Oriented Features in Java

Java supports the four main pillars of OOP:

1. **Encapsulation**: Achieved through access modifiers (`public`, `private`, `protected`).
2. **Abstraction**: Implemented via abstract classes and interfaces.
3. **Inheritance**: Supported using the `extends` keyword for classes and `implements` for interfaces.
4. **Polymorphism**: Realized through method overloading and overriding.

### Non-Pure OOP Elements in Java

1. **Primitive Data Types**: Java includes non-object primitives like `int`, `boolean`, `char`, etc.

2. **Static Members**: The `static` keyword allows for class-level fields and methods, not tied to object instances.

3. **Procedural Constructs**: Java supports procedural programming elements such as control flow statements (`if`, `for`, `while`, etc.).

### Code Example: Mixed OOP and Non-OOP Features

```java
public class Example {
    private int instanceVar;  // Encapsulation: private instance variable
    public static int staticVar = 10;  // Static variable

    public void instanceMethod() {
        // Procedural construct
        if (instanceVar > 5) {
            System.out.println("Greater than 5");
        }
    }

    public static void main(String[] args) {
        int localVar = 20;  // Primitive type
        Example obj = new Example();
        obj.instanceMethod();  // OOP: method invocation on object
        System.out.println(Example.staticVar);  // Accessing static member
    }
}
```
<br>

## 11. What is _bytecode_ in the context of _Java_?

**Bytecode** in Java refers to the compact, platform-independent instructions generated by the Java compiler. It serves as an intermediate representation between Java source code and the Java Virtual Machine (JVM) execution environment.

### Key Characteristics

1. **Platform Independence**: Bytecode is designed to run on any device with a compatible JVM, embodying Java's "Write Once, Run Anywhere" philosophy.

2. **Compact Format**: Bytecode instructions are typically more concise than equivalent machine code, reducing storage and transmission requirements.

3. **Verification**: The JVM performs bytecode verification to ensure code safety and integrity before execution.

### Execution Process

1. **Compilation**: Java source code is compiled into bytecode.
   ```java
   javac MyProgram.java  // Produces MyProgram.class
   ```

2. **JVM Interpretation**: The JVM interprets bytecode instructions at runtime.
   ```java
   java MyProgram  // Executes bytecode in MyProgram.class
   ```

3. **Just-In-Time (JIT) Compilation**: For performance optimization, the JVM may compile frequently executed bytecode sections into native machine code.

### Bytecode Structure

Bytecode consists of one-byte opcodes followed by zero or more operands. For example:

```
iconst_1    // Push integer constant 1 onto the stack
istore_1    // Store top of stack into local variable 1
```

### Advantages

- **Portability**: Enables cross-platform execution without recompilation.
- **Security**: Facilitates bytecode verification, enhancing runtime safety.
- **Optimization**: Allows for runtime optimizations by the JVM.

### Limitations

- **Performance Overhead**: Interpretation can be slower than native code execution, though mitigated by JIT compilation.
- **Limited Low-Level Control**: Restricts direct hardware access, which may be necessary for certain system-level operations.

### Tools for Bytecode Analysis

- **javap**: Java's built-in disassembler for viewing bytecode.
  ```bash
  javap -c MyProgram.class
  ```

- **ASM**: A bytecode manipulation and analysis framework.
<br>

## 12. How does _garbage collection_ work in _Java_?

In **Java**, the **Virtual Machine** (JVM) manages memory through **automatic garbage collection** (GC). This process identifies and reclaims objects that are no longer in use.

### Key Concepts

- **Reachability**: Objects are considered "alive" if they are reachable from the **root object**, which can be a `Thread`, `Stack`, or `Static` reference. Unreachable objects are eligible for garbage collection.

- **Reference Types**: There are different reference types that play a role in determining an object's reachability and GC eligibility.

### Reference Types

- **Strong References**: The most common type, created with `Object obj = new Object()`. Objects with strong references are not eligible for GC.

- **Soft References**: Denoted by `SoftReference<Object> softRef = new SoftReference<>(obj)`. Soft-referenced objects are garbage-collected only if the JVM requires memory.

- **Weak References**: Created with `WeakReference<Object> weakRef = new WeakReference<>(obj)`. These objects are reclaimed during the next GC cycle if they are not reachable.

- **Phantom References**: **Rarely used**, these are created using `PhantomReference`, typically in conjunction with a `ReferenceQueue`. They are enqueued before being collected during the next GC cycle.

- **Finalization**: The GC process can **finalize** an object before it reclaims it. This capability is associated with `finalize()` method, allowing the object to perform any necessary cleanup actions before being garbage-collected.

### Code example: Different types of references

Here is the Java code:

```java
import java.lang.ref.*;

public class ReferenceTypes {
    public static void main(String[] args) {
        Object obj = new Object();  // Strong Reference
        SoftReference<Object> softRef = new SoftReference<>(obj);  // Soft Reference
        WeakReference<Object> weakRef = new WeakReference<>(obj);  // Weak Reference

        PhantomReference<Object> phantomRef = new PhantomReference<>(obj, new ReferenceQueue<>());  // Phantom Reference
        obj = null;  // obj is no longer a strong reference to the object, making it eligible for garbage collection
    }
}
```

### Interview Tips

- Each reference type caters to specific memory management requirements. Understanding their use-cases is crucial for efficient resource utilization.

- The `finalize()` method, while still available, is **considered obsolete**. Its use is generally discouraged due to potential performance and reliability concerns.

- Familiarize yourself with more modern memory management tools, such as `java.lang.ref.Cleaner`, introduced in Java 9, for effective resource management in better ways.
<br>

## 13. What is the purpose of the _'final'_ keyword?

In Java, the `final` keyword offers **restrictions and benefits**. It primarily maintains the immutability of different entities.

### Core Functions

- **Class Immutability**: Makes a class unextendable.
- **Method Immutability**: Disallows method overriding.
- **Variable Immutability**: Commands a constant value for primitives and a constant reference for objects.

### Advantages

- **Enhanced Security**: Avoids data tampering through unintended extensions, method modifications, or reassignments.
- **Code Clarity**: Clarifies the intended use of class members, ensuring a reliable and coherent design.
- **Concurrent Safety**: Guarantees thread-safe data in **situations of code shared across threads**.

### Practical Applications

- **Inheritance Control**: Effortlessly sets up classes that are not designed for extension. This is beneficial when aiming to preserve a rigorous design.
- **Performance Optimization**: For primitive variables and simple data structures like Strings, using `final` eliminates the need for certain checks and operations, potentially speeding up the code execution.

- **Intelligent Compilation**: Can be leveraged by Java's JIT (Just-In-Time) compiler to make certain assumptions that would otherwise necessitate costly runtime checks.

### Example: `final` for Method Immutability & Variable Immutability

Here is the Java code:

```java
class Parent {
    // Prevent method overriding
    public final void doTask() {
        System.out.println("Parent class method");
    }

    // Prevent re-assignment of variables
    public final String name = "John";

    public final void display() {
        System.out.println("Name: " + name);
    }
}

class Child extends Parent {
    // This will cause a compilation error
    // Trying to override a final method
    // @Override
    public void doTask() {
        System.out.println("Child class method");
    }

    // Since 'name' is final, this code will cause a compilation error
    // public void changeName() {
    //     name = "Sara";
    // }
}

public class Main {
    public static void main(String[] args) {
        Child child = new Child();
        child.display();
    }
}
```
<br>

## 14. Can we _overload_ or _override_ _static methods_ in _Java_?

Garbage collection in Java is an **automatic memory management process** that identifies and removes objects that are no longer needed by the program. Here's how it works:

### Garbage Collection Process

1. **Marking**: The garbage collector identifies which objects are in use and which are not.
2. **Deletion**: Unused objects are deleted.
3. **Compaction**: After deleting unused objects, the remaining objects are moved to make the heap more compact.

### Garbage Collection Algorithms

Java uses different garbage collection algorithms:

#### Serial Garbage Collector
- Single-threaded collector
- Suitable for small applications with limited memory

#### Parallel Garbage Collector
- Uses multiple threads for minor garbage collection
- Default for most applications

#### Concurrent Mark Sweep (CMS) Collector
- Minimizes pauses by doing most of its work concurrently with the application threads

#### G1 (Garbage First) Collector
- Designed for applications with large amounts of memory
- Divides the heap into regions for more efficient collection

### Memory Allocation

Java uses a **generational memory model**:

1. **Young Generation**:
   - Where new objects are allocated
   - Further divided into Eden space and two Survivor spaces

2. **Old Generation**:
   - Long-lived objects are moved here from Young Generation

3. **Permanent Generation** (Before Java 8) / **Metaspace** (Java 8+):
   - Stores metadata about classes and methods

### Example of Garbage Collection

```java
public class GCExample {
    public static void main(String[] args) {
        for (int i = 0; i < 1000000; i++) {
            Object obj = new Object();
            // obj becomes eligible for garbage collection after this loop iteration
        }
        System.gc(); // Suggestion to run Garbage Collector
    }
}
```

### Key Points

- Garbage collection is **automatic** in Java
- Objects become eligible for garbage collection when they are no longer reachable
- The `System.gc()` method suggests running the garbage collector but doesn't guarantee immediate execution
- Garbage collection can affect performance, especially during "stop-the-world" events
- Different JVM implementations may use different garbage collection strategies
<br>

## 15. What is the significance of _'this'_ keyword in _Java_?

The `this` keyword in Java is a reference to the current instance of a class. It serves several important purposes in object-oriented programming.

### Key Uses of 'this' Keyword

#### 1. Distinguishing Instance Variables from Local Variables

When a method or constructor parameter has the same name as an instance variable, `this` helps to differentiate between them:

```java
public class Person {
    private String name;

    public Person(String name) {
        this.name = name; // 'this.name' refers to the instance variable
    }
}
```

#### 2. Invoking Current Class Methods

`this` can be used to call other methods within the same class:

```java
public class Calculator {
    public void multiply(int a, int b) {
        int result = a * b;
        this.display(result);
    }

    private void display(int value) {
        System.out.println("Result: " + value);
    }
}
```

#### 3. Passing Current Object as Parameter

`this` can be passed as an argument in method calls when an object needs to pass a reference to itself:

```java
public class Employee {
    public void updateRecord(Database db) {
        db.update(this); // Passing the current Employee object
    }
}
```

#### 4. Constructor Chaining

`this()` can be used to call another constructor in the same class:

```java
public class Rectangle {
    private int width, height;

    public Rectangle() {
        this(1, 1); // Calls the two-parameter constructor
    }

    public Rectangle(int width, int height) {
        this.width = width;
        this.height = height;
    }
}
```

#### 5. Returning Current Class Instance

`this` can be returned to allow method chaining:

```java
public class StringBuilder {
    private String str = "";

    public StringBuilder append(String s) {
        str += s;
        return this; // Allows chaining like: new StringBuilder().append("A").append("B")
    }
}
```
<br>



#### Explore all 100 answers here 👉 [Devinterview.io - Java](https://devinterview.io/questions/web-and-mobile-development/java-interview-questions)

<br>

<a href="https://devinterview.io/questions/web-and-mobile-development/">
<img src="https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/github-blog-img%2Fweb-and-mobile-development-github-img.jpg?alt=media&token=1b5eeecc-c9fb-49f5-9e03-50cf2e309555" alt="web-and-mobile-development" width="100%">
</a>
</p>

