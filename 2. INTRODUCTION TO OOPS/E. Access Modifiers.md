## **Ex.No: 2(E) : Access Modifiers**

**QUESTION:**

Create a class `SpeedLimit` with a **final** method `displayLimit()` that prints:

> "Max Speed: 80 km/h"

Try to override it in a subclass and show that overriding a **final method** is **not allowed** in Java.

**AIM:**

To demonstrate the use of the `final` access modifier in Java which prevents method overriding.

**ALGORITHM:**

1. Create a class `SpeedLimit` with a final method `displayLimit()`.
2. Create a subclass `HighwaySpeed` that extends `SpeedLimit`.
3. Try overriding the final method inside the subclass and observe the compilation error.
4. In the main class, create an object of the subclass and call the final method.
5. The program will compile successfully only when overriding is removed.

**PROGRAM:**

```
Program to demonstrate the final access modifier preventing method overriding
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
class SpeedLimit {
  final void displayLimit() {
    System.out.println("Max Speed: 80 km/h");
  }
}

class HighwaySpeed extends SpeedLimit {
  // Overriding is not allowed for a final method
  // If attempted, it will throw a compile-time error
}

public class main {
  public static void main(String[] args) {
    HighwaySpeed s = new HighwaySpeed();
    s.displayLimit();
  }
}
```

**OUTPUT:**

<img width="637" height="203" alt="image" src="https://github.com/user-attachments/assets/2bf353e1-c7d4-42ac-a1a7-d56eebb5f926" />


**RESULT:**

The program successfully demonstrated that a **final method cannot be overridden** in a subclass. Any attempt to override results in a compile-time error.

