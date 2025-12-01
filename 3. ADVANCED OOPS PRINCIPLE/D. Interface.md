
## **Ex.No: 3(D) : Interface**

**QUESTION:**

You’re developing a multi-console gaming platform that supports different controllers. Each controller has its own way of mapping buttons for actions like Jump, Shoot, and Pause.

To unify this behavior, you're asked to design a system using Java Interfaces. The interface will standardize the controls, and each controller will implement them differently.

Your Task:
Create an interface GameController with methods:

jump()
shoot()
pause()
Implement three controller types:

PlayBoxController
XCubeController
RetroFunController
Based on input from the user, select the controller and action, and call the correct method.

| Controller | Action | Output Printed                  |
| ---------- | ------ | ------------------------------- |
| Playbox    | jump   | PlayBox: Press X to Jump!       |
| Playbox    | shoot  | PlayBox: Press R2 to Shoot!     |
| Playbox    | pause  | PlayBox: Press Start to Pause.  |
| xcube      | jump   | X-Cube: Press A to Jump!        |
| xcube      | shoot  | X-Cube: Press RT to Shoot!      |
| xcube      | pause  | X-Cube: Press Menu to Pause.    |
| retro      | jump   | RetroFun: Use Up Arrow to Jump! |
| retro      | shoot  | RetroFun: Press B to Shoot!     |
| retro      | pause  | RetroFun: Press P to Pause.     |

If invalid controller is entered, print:
Unsupported controller!

If invalid action is entered, print:
Unknown action!

Input Format:
Line 1 → Controller type (playbox, xcube, retro)
Line 2 → Action (jump, shoot, pause)

Output Format:
Print the correct action message as shown in the table above

**AIM:**

To implement polymorphism using interfaces where multiple controllers implement standardized actions in different ways.

**ALGORITHM:**

1. Define `GameController` interface with three methods: jump(), shoot(), pause().
2. Implement the interface in:

   * PlayBoxController
   * XCubeController
   * RetroFunController
3. Read controller type and action from the user.
4. Create appropriate controller object based on input.
5. Call the method corresponding to selected action.
6. If invalid controller or action → print respective error message.

**PROGRAM:**

```
Program to demonstrate Interfaces using Gaming Controllers
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;

interface GameController {
    void jump();
    void shoot();
    void pause();
}

class PlayBoxController implements GameController {
    public void jump() {
        System.out.println("PlayBox: Press X to Jump!");
    }
    public void shoot() {
        System.out.println("PlayBox: Press R2 to Shoot!");
    }
    public void pause() {
        System.out.println("PlayBox: Press Start to Pause.");
    }
}

class XCubeController implements GameController {
    public void jump() {
        System.out.println("X-Cube: Press A to Jump!");
    }
    public void shoot() {
        System.out.println("X-Cube: Press RT to Shoot!");
    }
    public void pause() {
        System.out.println("X-Cube: Press Menu to Pause.");
    }
}

class RetroFunController implements GameController {
    public void jump() {
        System.out.println("RetroFun: Use Up Arrow to Jump!");
    }
    public void shoot() {
        System.out.println("RetroFun: Press B to Shoot!");
    }
    public void pause() {
        System.out.println("RetroFun: Press P to Pause.");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String controllerType = sc.nextLine().trim().toLowerCase();
        String action = sc.nextLine().trim().toLowerCase();

        GameController controller = null;

        switch (controllerType) {
            case "playbox":
                controller = new PlayBoxController();
                break;
            case "xcube":
                controller = new XCubeController();
                break;
            case "retro":
                controller = new RetroFunController();
                break;
            default:
                System.out.println("Unsupported controller!");
                return;
        }

        switch (action) {
            case "jump":
                controller.jump();
                break;
            case "shoot":
                controller.shoot();
                break;
            case "pause":
                controller.pause();
                break;
            default:
                System.out.println("Unknown action!");
        }
    }
}
```

**OUTPUT:**


<img width="1160" height="243" alt="image" src="https://github.com/user-attachments/assets/2be7efda-1d74-4a16-b5bf-b87e95b7ddb7" />


**RESULT:**
The program successfully demonstrates interfaces in Java by providing different controller behaviors for standardized actions.

