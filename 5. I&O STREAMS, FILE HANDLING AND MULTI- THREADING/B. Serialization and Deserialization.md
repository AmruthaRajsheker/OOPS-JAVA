## **Ex.No: 5(B) : Serialization and Deserialization**

**QUESTION:**

Write a Java program to read multiple UTF strings from the user, write them to a ByteArrayOutputStream using DataOutputStream, and display the byte array contents.

| Input                   | Result                                                                                                                                                  |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2 <br> hello <br> world | Byte array contents: <br> 0 5 104 101 108 108 111 0 5 119 111 114 108 100 <br> Total bytes: 14 <br><br> Strings read from memory: <br> hello <br> world |

**AIM:**

To serialize multiple UTF strings into a byte array using `ByteArrayOutputStream` and `DataOutputStream`, and then read them back using `ByteArrayInputStream` and `DataInputStream`.

**ALGORITHM:**

1. Read the number of strings from the user.
2. Store each string into memory by writing UTF data using `DataOutputStream`.
3. Convert the output stream to a byte array.
4. Display byte array contents and number of bytes stored.
5. Read back the strings using `DataInputStream`.
6. Display retrieved strings from memory.

**PROGRAM:**

```
Program to demonstrate serialization and deserialization of UTF Strings in memory
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.io.*;
import java.util.Scanner;

public class UTFStringsInMemoryUserInput {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            ByteArrayOutputStream baos = new ByteArrayOutputStream();
            DataOutputStream dos = new DataOutputStream(baos);

            int n = scanner.nextInt();
            scanner.nextLine();

            for (int i = 0; i < n; i++) {
                String str = scanner.nextLine();
                dos.writeUTF(str);
            }

            byte[] byteData = baos.toByteArray();

            System.out.println("Byte array contents:");
            for (byte b : byteData) {
                System.out.print(b + " ");
            }
            System.out.println("\nTotal bytes: " + byteData.length);

            ByteArrayInputStream bais = new ByteArrayInputStream(byteData);
            DataInputStream dis = new DataInputStream(bais);

            System.out.println("\nStrings read from memory:");
            for (int i = 0; i < n; i++) {
                String s = dis.readUTF();
                System.out.println(s);
            }
        } catch(Exception e) {} 
    }
}
```

**OUTPUT (Example):**

<img width="1284" height="666" alt="image" src="https://github.com/user-attachments/assets/2e454f3d-029f-4a61-8ce0-7a1c449014ce" />


**RESULT:**
Hence, the program successfully demonstrates serialization and deserialization of UTF strings using byte stream classes in Java and retrieves them accurately from memory.

