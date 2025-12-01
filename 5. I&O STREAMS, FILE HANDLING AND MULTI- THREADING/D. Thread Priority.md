## **Ex.No: 5(D) : Thread Priority**

**QUESTION:**

Write a java program for set the priority and name of the current thread. Consider two threads t1 and t2

Note : Read the threadname from the User

set the priority as 4 for t1 and set the priority as 2 for t2

For example:

| Input                           | Result                                                        |
| ------------------------------- | ------------------------------------------------------------- |
| First Thread <br> Second Thread | Thread[First Thread,4,main] <br> Thread[Second Thread,2,main] |

**AIM:**

To demonstrate setting thread name and priority for the current thread and an additional thread in Java.

**ALGORITHM:**

1. Read two thread names from user input.
2. Get the current thread and set:

   * name from input
   * priority as 4
3. Create new thread t2 and set:

   * name from input
   * priority as 2
4. Print both thread details.

**PROGRAM:**

```
Program to set thread name and priority in Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.Scanner;
public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        Thread t1 = Thread.currentThread();
        t1.setName(name1);
        t1.setPriority(4);
        System.out.println(t1);

        Thread t2 = new Thread();
        t2.setName(name2);
        t2.setPriority(2);
        System.out.println(t2);
    }
}
```

**OUTPUT (Example):**

<img width="970" height="274" alt="image" src="https://github.com/user-attachments/assets/704979e8-43d3-4eec-a333-fe91bcfb78d9" />


**RESULT:**
Hence, the program successfully updates and displays thread name and priority for both the main thread and an additional thread.


