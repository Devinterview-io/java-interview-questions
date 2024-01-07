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

**Java** introduced the groundbreaking concept of **Write Once, Run Anywhere** (WORA) that revolutionized how developers create software. This approach is particularly useful in **cross-platform** use-cases.

### Main Components of Java that Enable WORA

1. **JVM**: The Java Virtual Machine serves as an **abstraction layer** between the Java code and the underlying hardware or operating system. When a Java program is executed, JVM interprets and runs the bytecode.
   
2. Compiler: Java code is compiled into platform-independent bytecode. This bytecode is then executed by a compatible JVM running on any system, making it **universal**.

3. Standard Library: Java comes with a comprehensive **standard library** that provides cross-platform capabilities, such as file handling and networking.

### How Java Achieves WORA

- **Platform-Independence through Bytecode**: Java source code is compiled into a format called bytecode, not into machine code for a specific CPU. Interpreting bytecode makes Java applications accessible across different architectures and operating systems. Java bytecode also works efficiently on various devices, scaling from ordinary cellphones to complex supercomputers.

- **JVM**: JVM is like a **virtual computer** that forms an interface between your program and the underlying device. For each operating system, there's a specific JVM version tailored to transcend the uniqueness of that environment, ensuring that WORA is attainable even within the context of machines with diverse specifications and distinct OS characteristics.

- **Garbage Collection**: Java’s automatic memory management releases from memory the data which is no longer used or referenced, reducing the risk of memory leaks. This design aspect makes the development more manageable, especially when targeting different platforms.

- **No Pointers, Secure Execution**: By not exposing low-level memory details with pointers, Java offers a more **secure execution**, which is crucial when considering systems with different security paradigms. This level of safety with operation across numerous environments aligns with the principles of WORA.

### The "Hello World" Example in Action

1. **Java on Windows**: Compile Code: `javac HelloWorld.java`. Run: `java HelloWorld`. Output: `Hello, World!`.

2. **Java on Linux**: Same commands as Windows.

3. **Java on Mac**: Same as Windows and Linux.

4. **Java on Different Architectures**: Given the same Java bytecode, all systems executing compatible JVM versions would produce the same "Hello, World!" result.

Thus, **Write Once, Run Anywhere** with Java is not just a conceptual idea; it's a practical reality.

### Code Example: "Hello, World!" in Java

Here is the Java code:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
<br>

## 2. What are the _main features_ of _Java_?

**Java**'s robustness makes it stand out with its powerful features.

### Core Features of Java

1. **Platform Independence**: Write once, run anywhere (WORA) through Java Virtual Machine (JVM).
  
2. **Object-Oriented Design**: Emphasizes on objects and classes, promoting encapsulation, inheritance, and polymorphism.
  
3. **Strong Typing**: Variables are strongly typed, reducing ambiguity and potential for errors.

4. **Security**: Offers a secure platform with features such as a bytecode verifier and a security manager.
  
5. **Memory Management**: Centralized memory allocation and automatic garbage collection, reducing the risk of memory leaks.

6. **Concurrency**: Multi-threading, enabling concurrent execution and efficient multitasking.

7. **Architecture-Neutrality**: Promotes scalability in terms of hardware and software configurations.

8. **Dynamic Linking**: Modules can be loaded on-the-fly if needed, enhancing flexibility.

9. **Simplicity**: Easy-to-learn syntax and standard libraries simplify software development.

10. **Portability**: Java's "compile once, run anywhere" philosophy enables it to function across diverse platforms.

11. **JIT Compilation**: Combines the flexibility of bytecode with the performance of machine code.
  

### Additional Java Features

- **Multi-threading and Synchronization**: Allows multiple tasks to run concurrently within a program. Special care is needed to ensure thread safety.
  
- **Portable Object-Oriented Language**: Well-suited for web-based systems, IoT platforms, and cloud services.
  
- **Exception Handling**: Provides a robust system to capture and handle runtime errors.

- **Role in the Big Data Ecosystem**: With tools like Hadoop and Apache Spark, Java has an influential presence in big data processing.

- **Libraries and Tools**: Rich suite of libraries and a comprehensive development kit (JDK).

- **APIs for common tasks**: Provides classes and methods to perform standard and advanced functions, like string operations and database connectivity.

- **Diverse Data Structures**: Offers collections, arrays, list interfaces, and more for efficient data management.

- **Random Access Files and I/O Streams**: Streamlines handling of data from various sources like keyboards, files, and network connections.

- **Networking Capabilities**: Simplifies tasks such as socket programming, URL handling, and more.

- **Integration with Other Languages**: Leverages the Java Native Interface (JNI) and Java Virtual Machine (JVM) to support native and non-Java code.

- **JVM Optimizations**: The JVM continuously evolves, fine-tuning its operations for efficiency and performance.
<br>

## 3. Can you list some _non-object-oriented_ features of _Java_?

Although Java is primarily an **object-oriented** language, it incorporates several **procedural programming** features, allowing multi-paradigm development:

- **Primitive Data Types**: These non-OO data types describe simple values (integers, Booleans, etc.)
- **Non-Static Methods**: Objects operate on instance data via methods.
- **Package-Level Scopes**: 'package-private' (default) visibility limits accessibility to the package, such as a directory in the file system.
- **Utility Classes**: As an example, `java.util.Arrays` includes static methods to manipulate arrays without requiring an object instance.
- **Lack of Multiple Inheritance**: Java employs a single-inheritance model to prevent complexities linked with inheriting from multiple parents.

### Code Example: Utility Class

Here is the Java code:

```java
// Greeter.java
package com.example;

public class Greeter {
    private String message;

    public Greeter(String message) {
        this.message = message;
    }

    public String getMessage() {
        return message;
    }
}

// GreeterUtility.java
package com.example;

public class GreeterUtility {
    private GreeterUtility() {
        // Private constructor to prevent instantiation
    }

    public static void printMessage(Greeter greeter) {
        System.out.println(greeter.getMessage());
    }
}

// Main.java
package com.example;

public class Main {
    public static void main(String[] args) {
        Greeter greeter = new Greeter("Hello, World!");
        GreeterUtility.printMessage(greeter);
    }
}
```

In this example, `GreeterUtility` is a utility class without any non-static methods, demonstrating a **basic implementation of a non-OO feature**.
<br>

## 4. Describe the difference between _JDK_, _JRE_, and _JVM_.

Unraveling **JVM**, **JRE**, and **JDK** is essential for understanding Java's inner workings.

### JVM: The Java Virtual Machine

The **JVM** is the key execution environment for Java applications and is responsible for many crucial tasks, including memory management, garbage collection, and platform independence.

#### Core Functions

- **Bytecode Interpreter**: Translates Java bytecode into native machine instructions.
- **Memory Management**: Allocates and manages memory for Java objects. This includes garbage collection.
- **JIT Compiler**: Compiles frequently-used code from bytecode to native machine instructions for better performance.
- **Exception Handling**: Implements the try-catch blocks and handles exceptions.
- **Security and Accessibility**: Regulates application accessibility and security features.

### JRE: Java Runtime Environment

The **JRE** serves as the runtime environment for Java applications and contains everything necessary for their execution, excluding development tools.

#### Key Elements

- **JVM**: This is an instance of JVM tailored to run Java applications.
- **Libraries and Components**: Comprehensive suite offering classes, methods, and utilities from Java's extensive library.
- **Configuration and Resources**: Necessities like properties and settings vital for Java's execution.
- **Runtime Tools**: Utilities that support performance monitoring, diagnostics, and remote debugging.

### JDK: Java Development Kit

Compared to the JRE, the **JDK** is a comprehensive kit encompassing both the runtime environment and development tools, like **compilers** and debuggers. While JRE is designed purely for running Java applications, JDK is meant for developing and debugging applications, in addition to running them.

#### Major Components

- **JRE**: JDK incorporates a full JRE, thus it includes all of its elements.
- **Development Tools**: Such as Java Compiler (javac), Java Debugger, and other utilities indispensable for compiling, debugging, and monitoring Java programs.
- **Libraries**: Extensive sets of libraries similar to those contained in the JRE.

### Code Example: JDK, JRE, and JVM in Action

Here is the Java code:

```java
 public class JDKExample{
   public static void main(String[] args){
     System.out.println("Hello, Java World!");
   }
 }
```
<br>

## 5. What is the role of the _ClassLoader_?

**Class Loaders** play a pivotal role in the runtime environment of Java, managing the process of loading classes into memory.

### Key Functions

- **Loading Classes**: This involves finding and defining the binary representation of a class or interface.

- **Linking Classes**:
  - Verification: Ensures classes adhere to Java language and platform restrictions.
  - Preparation: Allocates memory for class variables and initial default values.
  - Resolution: Interclass references are replaced with direct references.

- **Initializing Classes**: This step involves executing the Java code that initializes the class.


### Types of Class Loaders

1. **Bootstrap Class Loader**: It's built into the JVM and loads core Java API classes from the `rt.jar` file or equivalent.

2. **Extension Class Loader**: Also a part of the JRE. It loads classes from the `lib/ext` directory or any directories specified by the `java.ext.dirs` system property.

3. **System (Application) Class Loader**: Primarily responsible for loading user-defined classes. It's a child of the Extension Class Loader and loads from the classpath.

4. **Custom (User-Defined) Class Loaders**: Java allows for custom class loaders to support dynamic loading and control over class-loading behavior.


**Delegation Hierarchy**: Each subsequent loader falls back to its parent loader, ensuring that classes are loaded only once, it's also known as the "Principle of Delegation".

### Dynamic Class Loading

Java provides methods for dynamic loading of classes, such as:

- `Class.forName(String className)`: Loads and returns a reference to the class specified by the input string.
- `ClassLoader.loadClass(String name)`: A higher-level method, invoking the loadClass method of the appropriate ClassLoader.

These methods are key to enabling dynamic software behavior, like plug-in systems and service registries.

### Code Example: Class Loading

Here is the Java code:

```java
public class CustomClassLoaderExample {

    public static void main(String[] args) throws ClassNotFoundException, IllegalAccessException, InstantiationException {

        // Using Class.forName for dynamic loading
        Class<?> dynamicClass = Class.forName("com.example.DynamicClass");
        DynamicClass dynamicInstance = (DynamicClass) dynamicClass.newInstance();
        dynamicInstance.sayHello();

        // Using custom class loader for loading a class from file system
        File file = new File("/path/to/CustomClass.class");
        byte[] classData = Files.readAllBytes(file.toPath());
        CustomClassLoader customClassLoader = new CustomClassLoader();
        Class<?> customClass = customClassLoader.defineClass("com.example.CustomClass", classData);
        CustomClass customInstance = (CustomClass) customClass.newInstance();
        customInstance.someMethod();
    }
}
```
<br>

## 6. What is the difference between a _path_ and a _classpath_ in _Java_?

In Java, **the classpath** tells the JVM where to locate compiled Java classes during runtime. These could be your own classes or third-party library classes.

On the other hand, a **file path** is the location of a file or directory within the file system, which may or may not pertain to Java classes.

For example, let's say you have a Java file named `HelloWorld.java` and the corresponding compiled `.class` file. If the file path to `HelloWorld.class` is "C:/classes" and the package is `com.example`, the corresponding entry on the classpath would be "C:/classes/com/example".

### Importance of Classpath

The classpath is crucial for the Java Virtual Machine (JVM) to locate classes during runtime. When you run a Java program, the JVM uses the classpath to resolve and load **dependent classes**.

#### Default Classpath Entries

- Current Directory (.)
- JAR Files (.jar)
- Directories with .class Files

### Ways to Set the Classpath

1. **Command-Line**: Use `java -cp` or `java -classpath`.

2. **Environment Variable**: The `CLASSPATH` environment variable can define a global classpath for the system.

3. **IDEs**: They often have built-in tools for managing the classpath. Select this option to manage the classpath yourself.

4. **Manifest File**: If a JAR file contains a manifest file (META-INF/MANIFEST.MF), it can include a `Class-Path` attribute that lists other JAR files to be included in the classpath.

5. **Java Virtual Machine**: When it's run, you can use the `-cp` command-line argument to set the classpath.

6. **Web Applications**: For web applications, the classpath is usually configured in the web.xml file.

### Code Example: Setting the Classpath

```java
// Using the -cp flag when running the javac or java command
// java -cp .:/path/to/some.jar MyApp
// javac -cp .:/path/to/some.jar Main.java
```

### Handling dependencies with Maven and Gradle

**Maven** and **Gradle** are popular build tools for Java that automate dependency management and help in setting up the classpath.

#### Maven

In Maven, dependencies are declared in a project `pom.xml` file. Maven then resolves and downloads these dependencies from a central repository. Each project's dependencies are managed by the corresponding `pom.xml` file.

#### Gradle

Gradle, on the other hand, uses a `build.gradle` file that's typically more concise and flexible than Maven's `pom.xml`. Libraries and their versions are specified in a similar way to Maven, but with a slightly different syntax.

### Key Steps in Classpath Management

- **Understand Project Structure**: Know where your compiled classes (`.class` files) and external libraries are located.
- **Be Consistent**: Ensure everyone working on the project follows the same classpath settings.
- **Automation is Key**: Leverage build tools like Maven or Gradle to streamline the process.

### Best Practices

When managing the classpath,

- **Avoid Absolute Paths**: They can cause portability issues.
- **Use Build Tools**: They simplify dependency management and classpath configurations.
- **Limit Classpath Entries**: A long classpath can degrade performance.

### Common Pitfalls

- **Missing Dependencies**: Neglecting to include all necessary dependencies in the classpath can lead to runtime errors.
- **Order Matters**: If the same class is present in multiple locations on the classpath, the order determines which one is used.
<br>

## 7. Can you explain the difference between an _int_ and an _Integer_ in _Java_?

In Java, **int** and **Integer** may seem similar, but they are distinct data types with unique properties and characteristics.

### Key Distinctions

#### int
 - It's a **primitive data type**.
 - Represents whole numbers between $-2^{31}$ and $2^{31} - 1$.
 - Memory allocation: Fixed $32$ bits (or $4$ bytes).
 - Instantiation: Direct, no constructor required.
 - Default value: $0$.
 - Performance: Usually faster since it's not an object.
 - Usage in generics: Not allowed.

#### Integer
 - It's a **wrapper class** for the primitive `int`.
 - Provides additional functionality via class methods.
 - Memory allocation: Variable. Typically requires more memory than the primitive `int`.
 - Instantiation: Through constructor or auto-boxing.
 - Default value: `null` (if not assigned a value).
 - Performance: May be slightly slower due to object handling overhead.
 - Usage in generics: Allowed.

### Code Example: int and Integer

Here is the Java code:

```java
public class IntVsInteger {
    public static void main(String[] args) {
        int primitiveInt = 10;  // Direct assignment
        Integer objInt = new Integer(20);  // Instantiation through constructor

        // Auto-boxing (conversion from primitive to object)
        Integer autoBoxed = primitiveInt;

        // Unboxing (conversion from object to primitive)
        int unboxed = objInt;

        System.out.println("Primitive int: " + primitiveInt);
        System.out.println("Integer object: " + objInt);
        System.out.println("Auto-boxed Integer: " + autoBoxed);
        System.out.println("Unboxed int: " + unboxed);

        // Uncomment the following line to witness default values
        // System.out.println("Unassigned Integer: " + unassigned);
    }
}
```
<br>

## 8. What are _wrapper classes_ in _Java_?

**Wrapper classes** in Java let you work with primitives as reference types. This is particularly useful in generic collections or when using features that require objects, like **Java Bean properties**.

Wrapper classes not only provide a way to convert primitives to and from objects, but they also offer a variety of useful methods and utilities specific to each type of primitive.

### Core Wrapper Classes

| Primitive | Wrapper Class | Conversion Method | ValueType Example | Wrapper Example |
| --- | --- | --- | --- | --- |
| boolean | Boolean | `.valueOf()` <br> `.parseBoolean()` <br> `.booleanValue()` | `true` | `Boolean.TRUE` |
| byte | Byte | `.valueOf()` <br> `.parseByte()` <br> `.byteValue()` | `123` | `Byte.valueOf(123)` |
| char | Character | `.valueOf()` <br> `.charValue()` | `'a'` | `Character.valueOf('a')` |
| short | Short | `.valueOf()` <br> `.parseShort()` <br> `.shortValue()` | `123` | `Short.valueOf(123)` |
| int | Integer | `.valueOf()` <br> `.parseInt()` <br> `.intValue()` | `123` | `Integer.valueOf(123)` |
| long | Long | `.valueOf()` <br> `.parseLong()` <br> `.longValue()` | `123L` | `Long.valueOf(123L)` |
| float | Float | `.valueOf()` <br> `.parseFloat()` <br> `.floatValue()` | `123.45f` | `Float.valueOf(123.45f)` |
| double | Double | `.valueOf()` <br> `.parseDouble()` <br> `.doubleValue()` | `123.45` | `Double.valueOf(123.45)` |

### When to Use Wrappers

1. **Collections**: Specialized collections like `ArrayList<int>` are not possible because generics need classes.

   For instance:

   ```java
   List<Integer> intList = new ArrayList<>();
   intList.add(5); // autoboxing: converts int to Integer
   int num = intList.get(0);  // unboxing: converts Integer to int
   ```

2. **Nullability**: If you need to represent that a number might not have a value, such as when getting input from a text field, using the wrapper `Integer` allows for `null`. The primitive `int` cannot be `null`.

3. **Java Beans**: In scenarios like `getCustomerAge()` of a `Customer` class, the returned age should be the reference type `Integer`, which conveniently accepts `null` for unspecified ages.
<br>

## 9. What does it mean that _Java_ is a _statically typed_ language?

**Static typing** requires the explicit declaration of a variable's type before it is used. This enables early identification of certain types of errors, such as type mismatches or unsupported operations on a specific type.

### Key Characteristics

- **Type Safety**: All data objects are of a specific type, and their types do not change unless explicitly converted.
  
- **Performance Efficiency**: Compile-time type determination helps optimize code and reduce overhead.

- **Predictability**: Predictable types improve the integrity and reliability of the code.

- **Tool Support**: IDEs can leverage static typing for better auto-completion and error checking.

- **Code Clarity**: Explicitly defined types make code easier to comprehend.

### Sample Java Code: Static Typing in Action

Here is the Java code:

```java
// Explicitly declare types
int num1 = 5;
double num2 = 3.5;
String text = "Hello, Java!";

// Type-safe arithmetic
double sum = num1 + num2;  // Results in a double

// Incompatible types are caught at compile-time
//int result = num1 + text;  // Compilation error: incompatible types
```
<br>

## 10. Is _Java_ a pure _object-oriented language_? Why or why not?

**Java** isn't a pure **object-oriented language**. While most of its features align with OOP principles, some non-object-specific elements that originate from **procedural programming** still persist.

### OOP in Java

- **Encapsulation**: Achieved through access specifiers (`public`, `private`, `protected`) that protect classes, fields, and methods. 
- **Abstraction**: Implemented via abstract classes and interfaces. 
- **Inheritance**: Supported for classes using the `extends` keyword and for interfaces using `extends` or `implements`. Java doesn't support multiple inheritance for classes, but it allows multiple inheritance through interfaces.
- **Polymorphism**: Realized through method overloading and method overriding. 

### Lack of Full OOP Purity

1. **Primitive Data Types**: Java has primitive types (`int`, `short`, `float`, etc.) that aren't objects.
2. **Static Members**: The `static` keyword allows for fields and methods that belong to the class rather than an object.
3. **Procedural Constructs**: Java supports procedural programming constructs like control statements (`if`, `else`, `switch`, `while`, etc.).

### Code Example: Unwrapped `int` and `static` Method

Here is the Java code:

```java
public class Main {
    private int number; // Encapsulated using an instance variable
    
    public static void main(String[] args) {
        int count = 5;  // Primitive type outside the realm of OOP
        Main obj = new Main();
        obj.number = 10; 
        Main.doStatic();  // Invoking a static method directly on the class.
    }
    
    public static void doStatic() {
        System.out.println("Hello from static method!");
    }
}
```
<br>

## 11. What is _bytecode_ in the context of _Java_?

**Java bytecode** refers to the compact, machine-independent instructions generated by the Java compiler. It forms a vital link between Java source code and the runtime execution provided by the Java Virtual Machine (JVM).

### Role in Cross-Platform Execution

- The JVM acts as an interpreter to execute bytecode, ensuring consistent behavior across different platforms.
- **Just-In-Time Compilation** (JIT) further optimizes performance by translating bytecode into native machine code during runtime.

### Advantages

- **Cohesion**: Bytecode encapsulates both object-oriented program logic and related metadata.
- **Efficiency**: Computing compact bytecode reduces network overhead and disk I/O.
- **Protection**: Serving as an intermediate step, bytecode helps obfuscate source code, enhancing security and intellectual property protection.

**Disadvantages**:

- **Performance Overhead**: Interpreting bytecode introduces a performance lag, particularly for compute-intensive tasks. However, JIT compilation helps offset this drawback.
- **Limited Access to System Resources**: Bytecode execution within the JVM is restricted, forfeiting direct hardware access. This ensures security but might pose limitations in specific use cases.
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

**Java** doesn't support **method overloading** with the same method signature but different **static** status. Overriding also doesn't apply to static methods. When both a **subclass** and a **superclass** contain methods with the **same name** and **matching parameter types**, it's called **method hiding**. The method that gets invoked is determined by its **reference type** rather than its **object type**.

### Code Example: Method Hiding

Here is the Java code:

```java
public class Parent {
    static void myMethod() {
        System.out.println("Parent's static method.");
    }

    void anotherMethod() {
        System.out.println("Parent's non-static method.");
    }
}

public class Child extends Parent {
    static void myMethod() {
        System.out.println("Child's static method.");
    }

    public static void main(String[] args) {
        Parent p = new Child();
        p.myMethod(); 
        // Output: "Parent's static method." (method hiding)
    }
}
```
<br>

## 15. What is the significance of _'this'_ keyword in _Java_?

In **Java**, the **'this'** keyword primarily serves to distinguish between class instance and local variables, facilitating clear and unambiguous code.

### Key Functions of 'this' Keyword

- **Accessing Current Object**: Most notably, 'this' provides a reference to the current object, enabling access to its members or invoking its methods.

- **Overloading Method Resolution**: It allows for unambiguous identification of methods in an overloaded class, ensuring the correct one is invoked.

- **Variable Scope Discrimination**: This keyword is essential for disambiguating between class-level and local variables that share the same name.

### Sample 'this' Use-Cases

#### 1. Accessing Class Members

In the following example, 'this' is employed to access the ‘name’ and 'age' members of the class.

```java
public class Person {
    private String name;
    private int age;

    public void setNameAndAge(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```

#### 2. Method Invocation

The 'this' reference can be used to call methods in the same class. This is especially useful for code readability and consistency.

```java
public class Calculator {
    private int accumulator;

    public void add(int num) {
        this.accumulator += num;
    }

    public void subtract(int num) {
        this.add(-num);
    }
}
```

#### 3. Constructor Chaining

When multiple constructors exist, 'this' can be employed to invoke another constructor within the same class.

```java
public class Circle {
    private double radius;

    public Circle() {
        this(1.0);
    }

    public Circle(double radius) {
        this.radius = radius;
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

