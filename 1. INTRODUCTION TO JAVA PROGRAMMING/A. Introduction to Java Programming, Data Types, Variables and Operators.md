
## **Ex.No: 1(A) : Introduction to Java Programming, Data Types, Variables and Operators**


**QUESTION:**

Lovely is learning java basics, can you teach her the different types of datatypes in java? Write a program that uses all datatypes and print them all.

  Input Format: </br>
  byte - 24 </br>
  short - 11000 </br>
  int - 1,34,500 </br>
  long - 24,23,10,34 </br>
  float - 24.20 </br>
  double - 1,30,000.80 </br>
  boolean - true/false </br>
  char - 'u' </br>
  String -"Heyyy, Lovely, Let's learn java!"

**AIM:**

To write a Java program that demonstrates the use of different datatypes and prints their values.

**ALGORITHM:**

1. Import the Scanner class.
2. Create a Scanner object to receive input from the user.
3. Read values for byte, short, int, long, float, double, boolean, char, and String datatypes.
4. Store each input in its corresponding datatype variable.
5. Display all the stored values using print statements.
6. Close the Scanner object.

**PROGRAM:**

```
Program to implement variables and Operators using Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;
public class DataTypesDemo {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    byte b = sc.nextByte();
    short s = sc.nextShort();
    int i = sc.nextInt();
    long l = sc.nextLong();
    float f = sc.nextFloat();
    double d = sc.nextDouble();
    boolean bool = sc.nextBoolean();
    char c = sc.next().charAt(0);
    sc.nextLine();
    String str = sc.nextLine();
    System.out.println("Hey Lovely, let's print all types of data received from user using different data types");
    System.out.println("This is byte datatype " + b);
    System.out.println("This is short datatype " + s);
    System.out.println("This is int datatype " + i);
    System.out.println("This is long datatype " + l);
    System.out.println("This is float datatype " + f);
    System.out.println("This is double datatype " + d);
    System.out.println("This is boolean datatype " + bool);
    System.out.println("This is char datatype " + c);
    System.out.println("This is string datatype " + str);
    sc.close();
  }
}
```

**OUTPUT:**

<img width="1222" height="476" alt="image" src="https://github.com/user-attachments/assets/25192174-39c8-4ae4-bd39-b0a332baa3c7" />


**RESULT:**

The program for demonstrating different datatypes in Java executed successfully.

