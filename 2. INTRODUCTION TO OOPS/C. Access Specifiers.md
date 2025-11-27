## **Ex.No: 2(C) : Access Specifiers**

**QUESTION:**

Write a Java program to create a class called `Smartphone` with **private** instance variables `brand`, `model`, and `storageCapacity`.
Provide **public** getter and setter methods to access and modify these variables.
Add a method `increaseStorage()` that takes an integer value and increases the storage capacity by that value.

**AIM:**

To implement a Java class using private access specifiers and provide public getter, setter, and operational methods to manage object data securely.

**ALGORITHM:**

1. Create a class `Smartphone` with private variables: brand, model, and storageCapacity.
2. Create public getter and setter methods to access and update each variable.
3. Define a method `increaseStorage(int value)` to increase storage capacity.
4. In the main method:

   * Create an object of the Smartphone class.
   * Read brand, model, storage capacity, and extra storage from user input.
   * Update the storage using setter and increaseStorage() methods.
   * Display the updated details.

**PROGRAM:**

```
Program to demonstrate Access Specifiers in Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.Scanner;

class Smartphone {
  private String brand;
  private String model;
  private int storageCapacity;

  public String getBrand() {
    return brand;
  }

  public String getModel() {
    return model;
  }

  public int getStorageCapacity() {
    return storageCapacity;
  }

  public void setBrand(String brand) {
    this.brand = brand;
  }

  public void setModel(String model) {
    this.model = model;
  }

  public void setStorageCapacity(int storageCapacity) {
    this.storageCapacity = storageCapacity;
  }

  public void increaseStorage(int value) {
    if (value > 0) {
      this.storageCapacity += value;
    }
  }

  public void display() {
    System.out.println("Brand: " + brand);
    System.out.println("Model: " + model);
    System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
    System.out.println("------------------------------");
  }
}

public class Main {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);

    Smartphone phone = new Smartphone();

    phone.setBrand(sc.nextLine());
    phone.setModel(sc.nextLine());
    phone.setStorageCapacity(sc.nextInt());
    int extra = sc.nextInt();

    phone.increaseStorage(extra);
    phone.display();

    sc.close();
  }
}
```

**OUTPUT:**

<img width="1077" height="443" alt="image" src="https://github.com/user-attachments/assets/64418f09-3e4f-4b69-a4ea-d415b691ec5b" />


**RESULT:**

The program successfully demonstrates encapsulation using private access specifiers and public getter, setter, and class methods.

