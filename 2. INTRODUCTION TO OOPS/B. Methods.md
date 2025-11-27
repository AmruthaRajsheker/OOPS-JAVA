## **Ex.No: 2(B) : Methods**

**QUESTION:**

Write a method `int cube(int x)` that calls another method `int square(int x)` internally to calculate the cube as:

cube(x) = x * square(x)

**AIM:**

To write a Java program using methods where one method calls another to compute the cube of a number.

**ALGORITHM:**

1. Define a method `square(int x)` that returns x multiplied by itself.
2. Define a method `cube(int x)` that returns x multiplied by the result of `square(x)`.
3. Read an integer from the user.
4. Call the `cube()` method and print the result.

**PROGRAM:**

```
Program to demonstrate methods in Java by calculating cube using square()
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;
class prog {
  static int square(int x) {
    return x * x;
  }
  static int cube(int x) {
    return x * square(x);
  }

  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    System.out.println(cube(n));
  }
}
```

**OUTPUT:**

<img width="703" height="205" alt="image" src="https://github.com/user-attachments/assets/7f4f70f3-48b0-4a53-9e90-701ec66a3d5d" />


**RESULT:**

The program successfully demonstrates method calling by using one method (`square`) inside another (`cube`) to calculate the cube of a number.

