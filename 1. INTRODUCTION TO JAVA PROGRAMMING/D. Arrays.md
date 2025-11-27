## **Ex.No: 1(D) : Arrays**

**QUESTION:**

Write a Java program to count the number of positive, negative, and zero elements in an array.

For example:
<img width="553" height="207" alt="image" src="https://github.com/user-attachments/assets/849a3a01-fbb1-4a29-b8e3-1748e78ba053" />


**AIM:**

To write a Java program that uses arrays to count the number of positive, negative, and zero elements.

**ALGORITHM:**

1. Read the number of elements in the array.
2. Declare an integer array of that size.
3. Initialize three counters: positive, negative, and zero.
4. Read the elements into the array.
5. Traverse the array using a loop:

   * If the element is greater than 0 → increment positive count
   * If the element is less than 0 → increment negative count
   * Otherwise → increment zero count
6. Display the count of positive, negative, and zero elements.

**PROGRAM:**

```
Program to count positive, negative, and zero elements in an array
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.* ;
public class main {
    public static void main (String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt() ;
        int[] arr = new int[n] ;
        int pve=0, nve=0, zero=0 ; 
        for (int i=0;i<n;i++) {
            arr[i] = sc.nextInt() ;
            if (arr[i] > 0) pve+=1 ;
            else if (arr[i] < 0) nve+=1 ;
            else zero+=1 ;
        }
        System.out.println ("Positive count: "+pve+"\nNegative count: "+nve+"\nZero count: "+zero);
         
    }
}
```

**OUTPUT:**

<img width="957" height="537" alt="image" src="https://github.com/user-attachments/assets/93c549b7-9e4e-4af0-a3f9-97c45ac440ec" />

**RESULT:**

The Java program using arrays successfully counts the number of positive, negative, and zero elements.

