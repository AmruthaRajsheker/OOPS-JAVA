## **Ex.No: 2(D) : Variable Scope and Constructor**

**QUESTION:**

Write a Java program to access a static variable using both the class name and an object reference.

**AIM:**

To demonstrate access of a static variable using class name and object instance, showcasing static scope behavior in Java.

**ALGORITHM:**

1. Create a class `StaticDemo` with a static variable `value`.
2. In the main method:

   * Read an integer from the user.
   * Assign the value to the static variable using the class name.
   * Create an object of `StaticDemo`.
   * Access and print the static variable using class name and object reference.
3. Observe that static variables belong to the class, not individual objects.

**PROGRAM:**

```
Program to demonstrate static variable access in Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.Scanner;

class StaticDemo {
  static int value;
}

class prog {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int input = sc.nextInt();

    StaticDemo.value = input;

    System.out.println("Accessing using class name: " + StaticDemo.value);

    StaticDemo obj = new StaticDemo();
    System.out.println("Accessing using object: " + obj.value);
  }
}
```

**OUTPUT:**

<img width="894" height="327" alt="image" src="https://github.com/user-attachments/assets/89fb1c60-d804-4a87-90c1-1fdd10aee9ae" />


**RESULT:**

The static variable was successfully accessed using both class name and object, proving that static members are shared among all objects of a class.

