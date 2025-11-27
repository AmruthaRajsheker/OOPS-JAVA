## **Ex.No: 1(C) : Looping Statement**

**QUESTION:**

Reversing a number means rearranging its digits in the opposite order. For example:

* The reverse of 1234 is 4321
* The reverse of 9870 is 789 (since leading zeros in the reversed number are not shown)

Write a Java program that takes an integer input from the user and reverses its digits using a **while loop**.

The program should repeatedly extract the last digit using the modulus operator (%) and build the reversed number.
The loop continues until the number becomes **0**.
Finally, the reversed number must be displayed as output.

**Example:**

Input: 5600 </br>
Output: Reversed number: 65

**AIM:**

To write a Java program using a while loop to reverse the digits of a given number.

**ALGORITHM:**

1. Read an integer input from the user.
2. Initialize `rev = 0` to store the reversed number.
3. Extract the last digit: `digit = num % 10`.
4. Build the reversed value: `rev = rev * 10 + digit`.
5. Reduce the number: `num = num / 10`.
6. Repeat until the input number becomes 0.
7. Display the reversed number.

**PROGRAM:**

```
Program to reverse a number using a looping statement in Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;
public class ReverseNumber {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int num = sc.nextInt();
    int rev = 0;

    while (num != 0) {
      int digit = num % 10;
      rev = rev * 10 + digit;
      num = num / 10;
    }

    System.out.println("Reversed number: " + rev);
  }
}
```

**OUTPUT:**

<img width="869" height="279" alt="image" src="https://github.com/user-attachments/assets/f66e113f-a365-4292-ba2f-b206b0664c76" />


**RESULT:**

The program using a while loop successfully reversed the given number and displayed the correct output.

