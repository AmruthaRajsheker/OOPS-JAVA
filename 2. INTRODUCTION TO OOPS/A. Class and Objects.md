## **Ex.No: 2(A) : Class and Objects**

**QUESTION:**

Create a class `Car` with attributes **brand**, **model**, and **year**. Create 2 objects and print their details.

**Example Output:**
Car 1: Toyota Innova 2022
Car 2: Hyundai i20 2021

**AIM:**

To implement a Java program that demonstrates the concept of classes and objects by creating a Car class and displaying details of two car objects.

**ALGORITHM:**

1. Create a class named `Car` with three data members: brand, model, and year.
2. Create two objects of the class inside the `main` method.
3. Assign values to each object’s data members.
4. Print the values stored in the objects.

**PROGRAM:**

```
Program to demonstrate Class and Objects in Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
class Car {
  String brand;
  String model;
  int year;
}

public class prog {
  public static void main(String[] args) {
    Car car1 = new Car();
    car1.brand = "Toyota";
    car1.model = "Innova";
    car1.year = 2022;

    Car car2 = new Car();
    car2.brand = "Hyundai";
    car2.model = "i20";
    car2.year = 2021;

    System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
    System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
  }
}
```

**OUTPUT:**

<img width="671" height="225" alt="image" src="https://github.com/user-attachments/assets/10c7d803-c41c-4312-84eb-3f244d3d6063" />


**RESULT:**

The concept of classes and objects in Java was successfully demonstrated by creating two Car objects and printing their details.

