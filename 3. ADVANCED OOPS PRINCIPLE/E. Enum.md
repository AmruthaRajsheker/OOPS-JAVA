## **Ex.No: 3(E) : Enum**

**QUESTION:**

Write a Java program to create an enum Season with values WINTER, SPRING, SUMMER, and FALL. Use a switch statement to display a custom message based on the current season.

| Input  | Result                        |
| ------ | ----------------------------- |
| winter | It's cold outside. Stay warm! |

For example:

| Input  | Result                                     |
| ------ | ------------------------------------------ |
| fall   | Leaves are falling. Autumn is beautiful!   |
| spring | Flowers are blooming. Enjoy the fresh air! |
| summer | It's sunny and hot. Time for the beach!    |
| winter | It's cold outside. Stay warm!              |

**AIM:**

To implement an enum in Java and use a switch statement to display a message based on the input season.

**ALGORITHM:**

1. Define enum `Season` with four constants: WINTER, SPRING, SUMMER, FALL.
2. Read user input and convert to uppercase.
3. Convert input into an enum value using `valueOf()`.
4. Use switch case:

   * WINTER → Cold weather message
   * SPRING → Flower blooming message
   * SUMMER → Sunny beach message
   * FALL → Autumn message
5. Display the correct message.

**PROGRAM:**

```
Program to demonstrate Enum and Switch Case in Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.Scanner;

enum Season {
    WINTER, SPRING, SUMMER, FALL
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine().toUpperCase();
        scanner.close();
        
        Season season = Season.valueOf(input);
        
        switch (season) {
            case WINTER:
                System.out.println("It's cold outside. Stay warm!");
                break;
            case SPRING:
                System.out.println("Flowers are blooming. Enjoy the fresh air!");
                break;
            case SUMMER:
                System.out.println("It's sunny and hot. Time for the beach!");
                break;
            case FALL:
                System.out.println("Leaves are falling. Autumn is beautiful!");
                break;
        }
    }
}
```

**OUTPUT:**

<img width="1032" height="278" alt="image" src="https://github.com/user-attachments/assets/8f513bcb-fa42-4a4a-ab7e-78abdb2261df" />

**RESULT:**

The program successfully utilizes Enum and Switch statements to print season-specific messages based on user input.

