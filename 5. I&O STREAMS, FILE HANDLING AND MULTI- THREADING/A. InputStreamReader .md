

## **Ex.No: 5(A) : InputStreamReader**

**QUESTION:**

Write a program to read user input from the keyboard using InputStreamReader

**AIM:**

To read input from the keyboard using `InputStreamReader` and `BufferedReader` classes in Java.

**ALGORITHM:**

1. Create an `InputStreamReader` object to read input from `System.in`.
2. Wrap it inside a `BufferedReader` to read data efficiently.
3. Read a line of text entered by the user.
4. Concatenate the input with a greeting message.
5. Print the output.
6. Use try-catch to handle input exceptions.

**PROGRAM:**

```
Program to read user input using InputStreamReader in Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.io.*;
class prog {
    public static void main(String[] args) {
        try {
            InputStreamReader isr = new InputStreamReader(System.in);
            BufferedReader br = new BufferedReader(isr);
            String name = br.readLine();
            System.out.println("Hello, " + name + "!");
        } catch(Exception e) {
            System.out.println("error");
        }
    }
}
```

**OUTPUT (Example):**

<img width="562" height="266" alt="image" src="https://github.com/user-attachments/assets/59a16abb-5895-402a-a474-5fcee30137f7" />


**RESULT:**
Hence, the program successfully reads input from the keyboard through InputStreamReader and displays the expected output.

