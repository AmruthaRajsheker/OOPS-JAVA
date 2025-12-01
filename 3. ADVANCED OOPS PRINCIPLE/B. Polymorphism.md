

## **Ex.No: 3(B) : Polymorphism**

**QUESTION:**

Create a base class `BankAccount` with methods `deposit()` and `withdraw()`.

Create two subclasses:

* **SavingsAccount**: allows withdrawal but limits it to ₹10,000 per transaction
* **CheckingAccount**: allows withdrawal with a ₹10 fee per transaction

Input account type, deposit amount, and withdrawal amount from the user.

If checking account has insufficient balance print:
**"Insufficient balance in CheckingAccount (including ₹10 fee)."**

**AIM:**

To demonstrate runtime polymorphism in Java using method overriding in different account types.

**ALGORITHM:**

1. Create a base class `BankAccount` with:

   * variable `balance`
   * methods `deposit()` and `withdraw()`
2. Create a subclass `SavingsAccount` and override `withdraw()` to limit withdrawal to ₹10,000.
3. Create a subclass `CheckingAccount` and override `withdraw()` to deduct ₹10 as transaction fee.
4. Take user input for:

   * account type
   * deposit amount
   * withdrawal amount
5. Based on the type, create the correct account object using polymorphism.
6. Perform deposit and withdrawal operations.
7. Print final balance.

**PROGRAM:**

```
Program to demonstrate Polymorphism using Bank Accounts in Java
Developed by: AMRUTHA RAJSHEKER
Register Number: 212222110003
```

**Sourcecode.java:**

```java
import java.util.Scanner;

class BankAccount {
  double balance;
  void deposit(double amount) {
    balance += amount;
    System.out.println("Deposited: ₹" + amount);
  }
  void withdraw(double amount) {}
}

class SavingsAccount extends BankAccount {
  void withdraw(double amount) {
    if (amount <= 10000) {
      balance -= amount;
      System.out.println("Withdrawn from SavingsAccount: ₹" + amount);
    } else {
      System.out.println("Withdrawal limit for SavingsAccount is ₹10,000 per transaction.");
    }
  }
}

class CheckingAccount extends BankAccount {
  void withdraw(double amount) {
    double total = amount + 10;
    if (balance >= total) {
      balance -= total;
      System.out.println("Withdrawn from CheckingAccount: ₹" + amount + " (₹10 fee applied)");
    } else {
      System.out.println("Insufficient balance in CheckingAccount (including ₹10 fee).");
    }
  }
}

public class Main {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String type = sc.nextLine().trim().toLowerCase();
    double depositAmt = sc.nextDouble();
    double withdrawAmt = sc.nextDouble();
    
    BankAccount account;
    if (type.equals("savings"))
      account = new SavingsAccount();
    else
      account = new CheckingAccount();

    account.deposit(depositAmt);
    account.withdraw(withdrawAmt);
    System.out.printf("Final Balance: ₹%.2f", account.balance);
  }
}
```

**OUTPUT:**

<img width="1329" height="403" alt="image" src="https://github.com/user-attachments/assets/b242536d-b3ed-488a-89ec-3277ca0746ea" />



**RESULT:**

The program successfully demonstrates runtime polymorphism by invoking overridden withdraw methods based on the account type.


