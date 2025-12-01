## **Ex.No: 5(C) : File Handling**

**QUESTION:**

Read a file and reverse the order of words in each line.

For example:

| Input                                          | Result                                                    |
| ---------------------------------------------- | --------------------------------------------------------- |
| Java is fun <br> exit                          | Reversed lines: <br> fun is Java                          |
| Learning Java is powerful <br> exit            | Reversed lines: <br> powerful is Java Learning            |
| I love programming <br> Java is best <br> exit | Reversed lines: <br> programming love I <br> best is Java |

**AIM:**

To read lines of text, reverse the order of words in each line, and print the reversed output until "exit" is encountered.

**ALGORITHM:**

1. Create a Scanner to read input line by line.
2. Print "Reversed lines:" before output begins.
3. Loop until no more input is available:

   * Read a line
   * If the line is "exit", break the loop
   * Split the line into an array of words
   * Print words in reverse order
4. Continue reading and reversing lines until "exit".

**PROGRAM:**

```
Program to reverse the order of words from file input line by line
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;
class prog {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Reversed lines:");
        while(sc.hasNextLine()) {
            String line = sc.nextLine();
            if(line.equals("exit"))
                break;
            String[] words = line.trim().split("\\s+");
            for(int i = words.length - 1; i >= 0; i--) {
                System.out.print(words[i]);
                if(i > 0)
                    System.out.print(" ");
            }
            System.out.println();
        }
    }
}
```

**OUTPUT (Example):**

<img width="949" height="341" alt="image" src="https://github.com/user-attachments/assets/ac980fe2-556f-4fcd-9b79-045874e3ec36" />


**RESULT:**
Hence, the program successfully reads text input line by line and prints the words in reverse order, demonstrating file/stream handling in Java.


