## **Ex.No: 4(A) : Exception Handling**

**QUESTION:**

You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

**AIM:**

To handle a `NullPointerException` by ensuring that the array element is not null before calling string methods.

**ALGORITHM:**

1. Create a String array to store input.
2. Read inputs until an empty line is encountered.
3. Store each input in the array, allowing `"null"` input to convert to actual null.
4. While printing:

   * Check if the array element is not null
   * If not null → call `.toUpperCase()`
   * Else → print a message `"Null element"`
5. Close the Scanner object.

**PROGRAM:**

```
Program to handle NullPointerException while converting to uppercase
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.Scanner;
public class UppercaseArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String[] arr = new String[100];
        int i = 0;
        while (sc.hasNextLine()) {
            String input = sc.nextLine();
            if (input.equals("")) break;
            arr[i++] = input.equals("null") ? null : input;
        }
        for (int j = 0; j < i; j++) {
            if (arr[j] != null)
                System.out.println(arr[j].toUpperCase());
            else
                System.out.println("Null element");
        }
        sc.close();
    }
}
```

**OUTPUT (Example):**

<img width="961" height="312" alt="image" src="https://github.com/user-attachments/assets/ebb48eb6-5de6-4d9e-8979-34151f1e10d2" />


**RESULT:**

Hence, the program successfully avoids NullPointerException by validating that each string element is not null prior to calling .toUpperCase().
