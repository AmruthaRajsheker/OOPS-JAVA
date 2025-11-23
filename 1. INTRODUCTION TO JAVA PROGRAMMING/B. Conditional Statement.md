
## **Ex.No: 1(B) : Conditional Statement**

**QUESTION:**

You're entering a magical maze with a 3-digit access code. Based on its digits, the maze behaves differently:

• If the middle digit is 0 → Maze freezes. </br>
• If the sum of digits is exactly 15 → Maze reflects you back. </br>
• If the first digit is odd and the last digit is even → Maze opens. </br>
• Otherwise → Maze collapses. </br>

Print one of the following based on input: 

• Freezes </br>
• Reflects </br>
• Opens </br>
• Collapses </br>



**AIM:**

To write a Java program using conditional statements to determine the maze's behavior based on a 3-digit input code.

**ALGORITHM:**

1. Read the 3-digit number as input.
2. Extract:

   * First digit → divide by 100
   * Middle digit → remove last digit then fetch remainder when divided by 10
   * Last digit → remainder when divided by 10
3. Check the conditions in order:

   * If the middle digit equals 0 → output **Freezes**
   * Else if the sum of digits equals 15 → output **Reflects**
   * Else if first digit is odd and last digit is even → output **Opens**
   * Else → output **Collapses**
4. Display the result.

**PROGRAM:**

```
Program to implement conditional statements using Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;
public class main {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    int first = n / 100;
    int mid = (n / 10) % 10;
    int last = n % 10;

    if (mid == 0)
      System.out.println("Freezes");
    else if (first + mid + last == 15)
      System.out.println("Reflects");
    else if (first % 2 == 1 && last % 2 == 0)
      System.out.println("Opens");
    else
      System.out.println("Collapses");
  }
}
```

**OUTPUT:**

<img width="1157" height="326" alt="image" src="https://github.com/user-attachments/assets/df1ce1d8-239e-4135-9c2d-70bcad645f6c" />


**RESULT:**

The program for implementing conditional statements was executed successfully and the correct maze response was produced based on the input.

