
## **Ex.No: 3(C) : Abstraction**

**QUESTION:**

In a secret facility, you are designing intelligent agents that can explore grid-based mazes. Each agent sees the maze differently and interprets it using their unique instinct.

You are to build a system using abstraction where a base class MazeAgent declares an abstract method:

abstract String generateNavigationCode(String[] maze);
Two agents – ScoutAgent and HunterAgent – extend this class, but behave very differently.

Agent Behaviors
ScoutAgent
This agent is highly sensitive to special signals placed in the maze. Every time it senses the signal (@), it records where (which corridor row) the signal was found.
The final navigation code is the sequence of all those rows where it felt the signal — encoded as numbers.

HunterAgent
This agent is on the lookout for how trapped it might be. It keeps a strict count of all obstructions it sees in the maze walls.
If the number of such obstructions is equal or more than 10, it believes it's been trapped. Otherwise, it considers itself safe to escape.

🛠️ Your Task:
Implement the abstract class and its derived classes.

Accept maze rows as input.

Create the agent based on input.

Print the navigation code they generate.

Input Format:
n
maze_row_1
maze_row_2
...
maze_row_n
type
n = number of rows in the maze

Each maze_row_i = a string containing symbols (like #, ., @)

type = 1 for ScoutAgent, 2 for HunterAgent

Output Format:
A string representing the navigation code as computed by the selected agent. -

For HunterAgent - "TRAPPED"/ "ESCAPE"

**AIM:**

To implement abstraction in Java using different agents interpreting a maze based on overridden abstract methods.

**ALGORITHM:**

1. Create an abstract class containing an abstract method to generate a navigation code.
2. Implement ScoutAgent detecting '@' and capturing row positions.
3. Implement HunterAgent counting '#' obstructions and returning TRAPPED/ESCAPE.
4. Take maze input.
5. Create agent based on input type.
6. Display navigation result.

**PROGRAM:**

```
Program to demonstrate abstraction using maze exploration agents
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;
abstract class maze {
  abstract String nav(String[] m);
}

class scout extends maze {
  String nav(String[] m) {
    String res = "";
    for (int i = 0; i < m.length; i++) {
      for (char c : m[i].toCharArray()) {
        if (c == '@')
          res += (i + 1);
      }
    }
    return res;
  }
}

class hunt extends maze {
  String nav(String[] m) {
    int count = 0;
    for (String r : m) {
      for (char c : r.toCharArray()) {
        if (c == '#')
          count++;
      }
    }
    return (count >= 10) ? "TRAPPED" : "ESCAPE";
  }
}

class prog {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    String[] m = new String[n];
    for (int i = 0; i < n; i++)
      m[i] = sc.next();
    int t = sc.nextInt();
    maze a;
    if (t == 1)
      a = new scout();
    else
      a = new hunt();
    System.out.println(a.nav(m));
  }
}
```

**OUTPUT (Example):**

<img width="565" height="536" alt="image" src="https://github.com/user-attachments/assets/c5a5d6df-7473-40ec-a609-4d19eea9eadb" />


**RESULT:**

The program successfully demonstrates abstraction by creating different intelligent agents that interpret the maze using overridden abstract methods.


