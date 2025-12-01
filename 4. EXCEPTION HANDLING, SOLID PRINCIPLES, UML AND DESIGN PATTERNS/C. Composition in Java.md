## **Ex.No: 4(C) : Composition in Java**

**QUESTION:**

A Department contains Professor objects, but professors can exist independently.
If no inputs gets passed, print “No professors assigned.”

For example:

| Input                                  | Result                                                                |
| -------------------------------------- | --------------------------------------------------------------------- |
| 2 <br> Dr. Hariharan <br> Dr. Saveetha | Department: Computer Science <br> - Dr. Hariharan <br> - Dr. Saveetha |

**AIM:**

To implement a composition relationship in Java where a Department contains Professor objects, while professors exist independently.

**ALGORITHM:**

1. Create a `Professor` class with attribute **name**.
2. Create a `Department` class that contains a list of Professors.
3. Read number of professors from the user.
4. For each input, create a Professor object and add it to the Department.
5. If the department has no professors, print:

   * “No professors assigned.”
6. Otherwise print professor names under the department.

**PROGRAM:**

```
Program to demonstrate Composition in Java using Department and Professor classes
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;

public class DepartmentAssociation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();  
        sc.nextLine();

        Department dept = new Department("Computer Science");

        for (int i = 0; i < n; i++) {
            String profName = sc.nextLine();
            Professor prof = new Professor(profName);
            dept.addProfessor(prof);
        }

        dept.showProfessors();
        sc.close();
    }
}

class Professor {
    private String name;

    public Professor(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}

class Department {
    private String name;
    private List<Professor> professors;

    public Department(String name) {
        this.name = name;
        this.professors = new ArrayList<>();
    }

    public void addProfessor(Professor prof) {
        professors.add(prof);
    }

    public void showProfessors() {
        System.out.println("Department: " + name);
        if (professors.isEmpty()) {
            System.out.println("No professors assigned.");
        } else {
            for (Professor p : professors) {
                System.out.println("- " + p.getName());
            }
        }
    }
}
```

**OUTPUT:**

<img width="1059" height="243" alt="image" src="https://github.com/user-attachments/assets/8a3bbe82-9fa3-498f-b708-9aab59f44342" />


**RESULT:**
Hence, the program successfully demonstrates composition in Java by associating multiple independent Professor objects with a Department and displaying them effectively.

