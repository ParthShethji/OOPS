# Object-Oriented Programming (OOP) - Basics to Advanced

## 1️⃣ Introduction to OOP
### What is Object-Oriented Programming (OOP)?
OOP is a programming paradigm based on objects that contain **data (attributes)** and **behavior (methods)**.

### Key Concepts of OOP:
- **Encapsulation** → Hiding data and controlling access.
- **Abstraction** → Hiding implementation details and showing only necessary features.
- **Inheritance** → Reusing properties and behaviors from a parent class.
- **Polymorphism** → One method behaving differently based on context.

---

## 2️⃣ Class and Object
### **Class**
A blueprint for creating objects. It defines attributes (variables) and behaviors (methods).

### **Object**
An instance of a class.

---

## 3️⃣ Inheritance
### What is Inheritance?
Inheritance allows a **child class** to acquire properties and methods from a **parent class**.

### **Types of Inheritance**
1. **Single Inheritance** → One class inherits from another.
2. **Multilevel Inheritance** → A class inherits from another class, which in turn inherits from another.
3. **Hierarchical Inheritance** → Multiple classes inherit from the same parent.
4. **Multiple Inheritance (via Interfaces in Java)** → A class can implement multiple interfaces.

---

## 4️⃣ Polymorphism
### What is Polymorphism?
Polymorphism means **one method behaving in multiple ways**.

### **Types of Polymorphism**
1. **Method Overloading (Compile-time Polymorphism)** → Multiple methods with the **same name but different parameters**.
2. **Method Overriding (Runtime Polymorphism)** → A child class redefines a method from the parent class.

---

## 5️⃣ Abstraction
### What is Abstraction?
Abstraction means **hiding the implementation details** and **showing only the necessary features**.

### **How to Achieve Abstraction?**
- **Abstract Class** → Can have both **abstract methods (without body)** and **concrete methods (with body).**
- **Interface** → A blueprint containing only method declarations (before Java 8).

### **Abstract Class vs Interface**
| Feature           | Abstract Class  | Interface |
|------------------|----------------|-----------|
| **Methods** | Can have **both abstract & concrete methods** | Can have **only abstract methods** (before Java 8) |
| **Variables** | Can have instance variables | Only **public static final** variables (constants) |
| **Multiple Inheritance** | **Not supported** | **Supported** (can implement multiple interfaces) |
| **Access Modifiers** | Can have any modifier (private, protected, etc.) | Methods are **public by default** |

---

## 6️⃣ Encapsulation
### What is Encapsulation?
Encapsulation is **hiding data inside a class** and **allowing controlled access** using methods.

### **How to Achieve Encapsulation?**
✔ **Declare variables as `private`** (cannot be accessed directly).
✔ **Use `getter` and `setter` methods** to access and modify data.

### **Why is Encapsulation Important?**
✔ **Data security** → Prevents direct modification of data.
✔ **Better code control** → Only specific methods can change the values.
✔ **Improves maintainability** → Changes in data handling do not affect other parts of the program.

---

## 7️⃣ Abstraction vs Encapsulation
| Feature           | Abstraction  | Encapsulation |
|------------------|----------------|----------------|
| **Definition** | Hides the **implementation details** and shows only relevant information | Hides **data** by restricting direct access and using methods |
| **Focus** | **Hiding the working of a system** | **Hiding the data itself** |
| **How it's Achieved?** | Using **abstract classes** and **interfaces** | Using **private variables** and **getter/setter methods** |
| **Example** | ATM machine (we see only options, not internal code) | Capsule (medicine inside is hidden) |

---

## 8️⃣ Code Example Covering All OOP Concepts
```java
// Encapsulation: Using private variables and getter/setter methods
class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() { return name; }
    public void setName(String name) { this.name = name; }

    public int getAge() { return age; }
    public void setAge(int age) { this.age = age; }
}

// Abstraction: Hiding implementation details using an abstract class
abstract class Animal {
    abstract void makeSound();
    void sleep() {
        System.out.println("Sleeping...");
    }
}

// Inheritance: Dog inherits from Animal
class Dog extends Animal {
    void makeSound() {
        System.out.println("Woof Woof!");
    }
}

// Polymorphism: Method Overloading (Compile-time Polymorphism)
class MathUtils {
    int add(int a, int b) { return a + b; }
    int add(int a, int b, int c) { return a + b + c; }
}

// Interface: Achieving multiple inheritance
interface Flyable {
    void fly();
}

class Bird extends Animal implements Flyable {
    void makeSound() {
        System.out.println("Chirp Chirp!");
    }
    public void fly() {
        System.out.println("Flying high!");
    }
}

// Main class to test all OOP concepts
public class OOPExample {
    public static void main(String[] args) {
        // Encapsulation example
        Person p = new Person("Alice", 25);
        System.out.println("Person: " + p.getName() + ", Age: " + p.getAge());
        
        // Abstraction & Inheritance example
        Dog d = new Dog();
        d.makeSound();
        d.sleep();
        
        // Polymorphism example
        MathUtils math = new MathUtils();
        System.out.println("Sum: " + math.add(2, 3));
        System.out.println("Sum: " + math.add(2, 3, 4));
        
        // Interface example
        Bird b = new Bird();
        b.makeSound();
        b.fly();
    }
}
```

### **Output:**
```
Person: Alice, Age: 25
Woof Woof!
Sleeping...
Sum: 5
Sum: 9
Chirp Chirp!
Flying high!
```

---

## Summary
| OOP Concept | Description |
|------------|------------|
| **Encapsulation** | Hides data using private variables and provides controlled access via methods. |
| **Abstraction** | Hides implementation details and only exposes relevant features. |
| **Inheritance** | Allows a child class to acquire properties and behaviors from a parent class. |
| **Polymorphism** | Enables one method to behave differently based on context. |

---


