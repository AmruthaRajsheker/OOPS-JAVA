## **Ex.No: 5(E) : Multithreading – Synchronization**

**QUESTION:**

Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

**Input:**

* Two lines: a and b values

**Output:**

```
a = <swapped_a>
b = <swapped_b>
```

For example:

| Input     | Result            |
| --------- | ----------------- |
| 5 <br> 10 | a = 10 <br> b = 5 |

**AIM:**

To demonstrate synchronization in Java by swapping two integer variables using a synchronized block.

**ALGORITHM:**

1. Read values of a and b.
2. Create a lock object for synchronization.
3. Use a synchronized block on the lock to:

   * store a temporarily
   * assign b to a
   * assign stored value to b
4. Print the swapped values.

**PROGRAM:**

```
Program to implement synchronized block for safe variable swapping
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        Object lock = new Object();

        synchronized(lock) {
            int t = a;
            a = b;
            b = t;
        }

        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}
```

**OUTPUT (Example):**

<img width="608" height="318" alt="image" src="https://github.com/user-attachments/assets/94cc0e5e-5b86-4d38-b585-5c475f242f8d" />


**RESULT:**
Hence, the program successfully swaps two integer variables using a synchronized block, ensuring thread-safe access to shared data.

