
## **Ex.No: 4(D) : Design Patterns – Abstract Factory**

**QUESTION:**

Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.

**AIM:**

To implement the Factory Design Pattern in Java to create different notification objects dynamically based on user input.

**ALGORITHM:**

1. Create `Notification` interface with method `notifyUser()`.
2. Implement the interface in:

   * `EmailNotification`
   * `SMSNotification`
   * `PushNotification`
3. Create `NotificationFactory` to return an object based on user input.
4. In main:

   * Continuously read input notification type
   * Break on `"exit"`
   * For valid type → call notifyUser()
   * For invalid type → show an error message

**PROGRAM:**

```
Program to demonstrate Factory Pattern using Notification senders
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.Scanner;

interface Notification {
    void notifyUser();
}

class EmailNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Email Notification");
    }
}

class SMSNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending SMS Notification");
    }
}

class PushNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Push Notification");
    }
}

class NotificationFactory {
    public Notification createNotification(String type) {
        if (type == null) return null;
        switch (type.toLowerCase()) {
            case "email":
                return new EmailNotification();
            case "sms":
                return new SMSNotification();
            case "push":
                return new PushNotification();
            default:
                return null;
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        NotificationFactory factory = new NotificationFactory();
        while (true) {
            String input = sc.nextLine();
            if (input.equalsIgnoreCase("exit")) break;
            Notification n = factory.createNotification(input);
            if (n != null) n.notifyUser();
            else System.out.println("Invalid notification type: " + input);
        }
        sc.close();
    }
}
```

**OUTPUT (Example):**

<img width="590" height="348" alt="image" src="https://github.com/user-attachments/assets/0024a471-e422-451d-958d-7078063ee00b" />

**RESULT:**
Hence, the program successfully applies the Factory Design Pattern to dynamically generate various notification sender objects and invoke their respective behaviors.

