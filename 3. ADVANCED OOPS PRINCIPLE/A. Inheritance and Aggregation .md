## **Ex.No: 3(A) : Inheritance and Aggregation**

**QUESTION:**

Design a system to manage student assignments.

**Super Class — Student**

* studentId
* studentName

**Subclass — Assignment**

* assignmentId
* title
* submissionDate
* grade (int, if grade = -1 → print “Not graded”)

The program should accept inputs for a student and their assignment details, and then display them.


**AIM:**

To implement inheritance by creating a subclass `Assignment` that extends `Student` and displaying student assignment details.

**ALGORITHM:**

1. Create a superclass `Student` with studentId and studentName.
2. Create a subclass `Assignment` with extra attributes: assignmentId, title, submissionDate, and grade.
3. Use a constructor or setters to assign input values to the object.
4. If grade is `-1`, print `"Not graded"` else print the grade.
5. Display all details of the student and assignment.

**PROGRAM:**

```
Program to demonstrate Inheritance in Student Assignment Management System
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.*;

class Student {
    String studentId, studentName;
    Student(String studentId, String studentName) {
        this.studentId = studentId;
        this.studentName = studentName;
    }
}

class Assignment extends Student {
    String assignmentId, title, submissionDate;
    int grade;
    Assignment(String studentId, String studentName, String assignmentId, String title, String submissionDate, int grade) {
        super(studentId, studentName);
        this.assignmentId = assignmentId;
        this.title = title;
        this.submissionDate = submissionDate;
        this.grade = grade;
    }
    void display() {
        System.out.println("Student ID: " + studentId);
        System.out.println("Student Name: " + studentName);
        System.out.println("Assignment ID: " + assignmentId);
        System.out.println("Title: " + title);
        System.out.println("Submission Date: " + submissionDate);
        if (grade == -1) System.out.println("Grade: Not graded");
        else System.out.println("Grade: " + grade);
        System.out.println();
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
            String sid = sc.next();
            String sname = sc.next();
            String aid = sc.next();
            String title = sc.next();
            String date = sc.next();
            int grade = sc.nextInt();
            Assignment a = new Assignment(sid, sname, aid, title, date, grade);
            a.display();
        
        sc.close();
    }
}
```

**OUTPUT:**

<img width="1110" height="563" alt="image" src="https://github.com/user-attachments/assets/5ef73fdf-57c8-4819-b651-3a300759dc1b" />


**RESULT:**

The program successfully demonstrates inheritance by extending student details into assignment details and printing the grade status accordingly.


