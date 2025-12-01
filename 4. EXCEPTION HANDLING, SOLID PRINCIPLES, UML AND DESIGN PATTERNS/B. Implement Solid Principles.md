

## **Ex.No: 4(B) : Implement SOLID Principles – Singleton Design Pattern**

**QUESTION:**

You are designing a microservices-based system where multiple services like AuthService, UserService, OrderService, etc., need to log important system events.

To maintain centralized logging (and not have separate loggers for each service), the system uses a Singleton Logger.

Each service logs messages with its name and log level.

Log levels can be: INFO, WARNING, or ERROR.

Every log message is stored in order of occurrence and the logger prints the entire log history each time a new message is added.

🧩 Concepts Student Must Apply:
Implement a Singleton class (Logger) that holds logs.

Maintain logs as a list of strings.

Each log message must be formatted as:
"[Service] [LEVEL]: message"

Print full log history after each new log.

Input Format:
First line: Integer n – number of logs
Next n lines: Each contains:
[ServiceName] [Level] [Message]
(The message has no spaces.)

Output Format:
After each log, print:

[Service] [LEVEL]: message
Current Logs:

1. log1
2. log2
   ...

**AIM:**

To design a centralized logging system using the Singleton pattern to ensure a single shared logger instance across services.

**ALGORITHM:**

1. Create a Singleton class `Logger` with:

   * A static reference to itself
   * A list to maintain log history
   * A method to log messages and display complete history
2. Read the number of logs `n` from user input.
3. For each input:

   * Extract service name, log level, and message
   * Format message and call logger to store log
   * Display updated log history
4. Ensure only one logger instance exists.

**PROGRAM:**

```
Program to implement Singleton Logger for centralized logging in microservices
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;
class Logger {
    private static Logger instance;
    private List<String> logs;

    private Logger() {
        logs = new ArrayList<>();
    }

    public static Logger getInstance() {
        if (instance == null) instance = new Logger();
        return instance;
    }

    public void addLog(String service, String level, String message) {
        String log = service + " " + level + ": " + message;
        System.out.println(log);
        logs.add(log);
        System.out.println("Current Logs:");
        for (int i = 0; i < logs.size(); i++) {
            System.out.println((i + 1) + ". " + logs.get(i));
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] input = sc.nextLine().split(" ");
            String service = input[0];
            String level = input[1];
            String message = input[2];

            Logger logger = Logger.getInstance();
            logger.addLog(service, level, message);
            System.out.println();
        }
    }
}

```

**OUTPUT (Example):**

<img width="1176" height="659" alt="image" src="https://github.com/user-attachments/assets/65b69c46-b81f-41e8-ace9-1c18216a5dff" />


**RESULT:**

Hence, the program successfully maintains a centralized logging mechanism using the Singleton pattern, ensuring only one logger is shared across services and all logs are printed in sequence.

