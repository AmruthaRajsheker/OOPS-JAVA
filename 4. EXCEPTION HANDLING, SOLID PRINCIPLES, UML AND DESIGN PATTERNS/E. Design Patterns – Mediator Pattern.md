

## **Ex.No: 4(E) : Design Patterns – Mediator Pattern**

**QUESTION:**

Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.

For example:

| Input                                                         | Result                                                                                                                                                                                                         |
| ------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 3 <br> true <br> AirIndia101 <br> SpiceJet505 <br> Indigo303  | AirIndia101 granted landing. <br> AirIndia101 landed successfully. <br> SpiceJet505 granted landing. <br> SpiceJet505 landed successfully. <br> Indigo303 granted landing. <br> Indigo303 landed successfully. |
| 3 <br> false <br> AirIndia101 <br> SpiceJet505 <br> Indigo303 | AirIndia101 granted landing. <br> AirIndia101 landed successfully. <br> SpiceJet505 denied landing. Runway busy. <br> Indigo303 denied landing. Runway busy.                                                   |

**AIM:**

To implement the Mediator Design Pattern using a centralized Air Traffic Control (ATC) system to manage landing requests from multiple airplanes.

**ALGORITHM:**

1. Create `AirTrafficControl` mediator class to control access to the runway.
2. Create `Airplane` class to request landing via mediator.
3. Accept:

   * number of airplanes `n`
   * boolean indicating whether a landed plane releases runway
4. For each airplane:

   * Try to land using mediator
   * If runway free → grant landing and optionally release runway
5. Display results after each landing request.

**PROGRAM:**

```
Program to demonstrate Mediator Pattern using Air Traffic Control System
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;

class AirTrafficControl {
    private boolean runwayFree = true;
    public AirTrafficControl() {
        this.runwayFree = true;
    }
    public synchronized boolean requestLanding(Airplane plane) {
        if (runwayFree) {
            System.out.println(plane.getName() + " granted landing.");
            System.out.println(plane.getName() + " landed successfully.");
            runwayFree = false;
            return true;
        } else {
            System.out.println(plane.getName() + " denied landing. Runway busy.");
            return false;
        }
    }
    public synchronized void releaseRunway() {
        runwayFree = true;
    }
}

class Airplane {
    private String name;
    private AirTrafficControl atc;
    private boolean canReleaseRunway;
    public Airplane(String name, AirTrafficControl atc, boolean canReleaseRunway) {
        this.name = name;
        this.atc = atc;
        this.canReleaseRunway = canReleaseRunway;
    }
    public String getName() {
        return name;
    }
    public void requestLanding() {
        boolean landedSuccessfully = atc.requestLanding(this);
        if (landedSuccessfully && canReleaseRunway) {
            atc.releaseRunway();
        }
    }
}

public class AirTrafficSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        while (sc.hasNextInt()) {
            int n = sc.nextInt();
            if (!sc.hasNextBoolean()) break;
            boolean planesCanReleaseRunway = sc.nextBoolean();
            sc.nextLine();
            AirTrafficControl atc = new AirTrafficControl();
            List<Airplane> planes = new ArrayList<>();
            for (int i = 0; i < n; i++) {
                String planeName = sc.nextLine();
                planes.add(new Airplane(planeName, atc, planesCanReleaseRunway));
            }
            for (Airplane plane : planes) {
                plane.requestLanding();
            }
        }
        sc.close();
    }
}
```

**OUTPUT (Sample):**


<img width="978" height="519" alt="image" src="https://github.com/user-attachments/assets/517f3999-5074-4b24-b645-c5341ea6ddfe" />


**RESULT:**
Hence, the program successfully demonstrates the Mediator Pattern by enabling a centralized Air Traffic Control to coordinate landing requests among multiple airplane objects.


