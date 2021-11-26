# Java Object-Oriented Programming

## Class blueprint

```java
// Class blueprint
public class MyClass {
  // Can have attributes...
  private String attribute1;  // private attribute member, getter/setter are needed
  MyEnum myEnum;
  static string staticAttribute1 = "Static Attribute"; // belongs to the class

  // Constructor
  MyClass() {
    // Initiate the instance of MyClass class.
    this("'this' is used to call alternate constructors from within a constructor");
    // optional code lines...
  }

  // Constructor
  MyClass(String message) {
    // Initiate the instance of MyClass class.
  }

  // Setter for private attribute
  public void setAttribute1(attribute1) {
    this.attribute1 = attribute1;  // note: "this" keyword is needed to disambuguate the variable reference.
  }

  // Getter for private attribute
  public String getAttribute1() {
    return attribute1;
  }

  // Methods or behaviours:
  void myMethod() {
    // no modifier so the method is accessible from its package only.
    this.attribute1 = 'xyz';
  }

  private void myPrivateMethod() {
    // private so only accessible from this classs
  }

  protected void myProtectedMethod() {
    // protected method so accessible from this class and sub-classes
  }

  public void myPublicMethod() {
    // public method so accessible from anywhere;
  }

  // Static method
  static void myStaticMethod() {
    // A static method does not rely on any non-static attribute or member.
  }
}
```

### Static vs Non-Static members

- Non-Static Member: is accessible from an instance and belongs to that instance
- Static Member: is accessible through the class and belongs to that class
  - Static members can be accessed using the class name, example:

## Enum blueprint

```java
// Enum blueprint
public enum MyEnum {
  CONSTANT1,
  CONSTANT2,
  ...,
  CONSTANTN
}
```

## Main class blueprint

```java
// Main class
public class Main {
  public static void main(String[] arg) {
    MyClass myClass = new MyClass('abc'); // Create an object of type MyClass

    myClass.myMethod('xyz');  // Call a method from my object
  }

}
```

## Princibles

### Encapsulation

- allow us to bind together data and related functionality
- prevent classes from becoming tightly coupled
- easily modify the inner workings of one class without affecting the rest of the program
- restrictions
  - we need a clear interface between a given class and the rest of the program
  - everything can't have direct access
- make the class attributes hideen from other classes using encapsulation
- provide a clear interface through public methods
- benefits
  - clear pathways for classes to communicate
  - less code changes required for a refactoring change
  - less likely for an attribute to be overwritten with an invalid or null value unexpectedly
- Access Modifiers in Java:
  - private: only visible in class that the member lives in
  - no modifier: only visible in package the member lives in
  - protected: visible to the package and all subclasses
  - public: accessible everywhere within the program

### Inheritance

- allow us to create class hierarchies
- Subclass (child class)
  - inherits properties
  - referred to as the child class
- Superclass (parent class)
  - is inherited from
  - referred to as the parent class
- promotes code reusability and scalability
- leveraging inheritance:
  - a class can only have one superclass but multiple subclasses
  - if multiple super classes is needed then multilevel inheritance is required

```java
public class MySuperClass {
  protected String a1;
  private String a2;

  MySuperClass(String a1, String a2) {
    // Super Class constructor
    this.a1 = a1;
    this.a2 = a2;
  }

  public void myMethod() {
    // Method of the Super Class
  }
}

public class MySubClass extends MySuperClass {
  MySubClass(String arg1, String arg2) {
    super(arg1, arg2);  // call superclass with arguments
    // Sub Class constructor
  }

  public String getA1() {
    return super.a1;  // this.a1 would also work for this Superclass protected variable;
  }

  @Override
  public void myMethod() {
    // Override the Super Class Method within the Sub Class
  }
}

```

### Polymorphism

- the ability for an object or function to take amny different forms
- Java supports two types of polymorphism: run time and compile-time polymorphism
- it helps to reduce complexity and write reusable code

```java


```

## Usefull build-in JAVA commands
- System.out.println("string...");

