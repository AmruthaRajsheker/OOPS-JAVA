## **Ex.No: 1(E) : Strings and Math Functions**

**QUESTION:**

Write a Java program to check whether a given string is a palindrome.

A palindrome is a word or phrase that reads the same forwards and backwards.
Example: *level*, *madam*, *racecar*.

**AIM:**

To write a Java program using string operations to check whether the given string is a palindrome.

**ALGORITHM:**

1. Read a string as input from the user.
2. Reverse the string using `StringBuilder`.
3. Compare the original string with the reversed string using `.equals()`.
4. If both are equal, display that the string is a palindrome.
5. Otherwise, display that the string is not a palindrome.

**PROGRAM:**

```
Program to check whether a string is a palindrome using Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;
public class prog {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String str = sc.nextLine();

    if (str.equals(new StringBuilder(str).reverse().toString()))
      System.out.println(str + " is a palindrome.");
    else
      System.out.println(str + " is not a palindrome.");
  }
}
```

**OUTPUT:**

<img width="825" height="273" alt="image" src="https://github.com/user-attachments/assets/d16069de-871d-418a-a1e8-c8fcafa3380b" />


**RESULT:**

The program successfully checks and displays whether the given string is a palindrome using string operations and built-in methods.


