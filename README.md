# 💳 Credit Card Checker (Java)

A simple Java program that validates **8-digit credit card numbers** using a simplified version of the **Luhn Algorithm**.  
This project demonstrates basic arithmetic logic, modular division, and condition handling for number verification.

---

## 📂 Project Structure
```
Credit-Card-Checker-main/
└── CreditCardChecker.java
```

---

## 🧩 Overview
The `CreditCardChecker` class determines whether a given **8-digit integer** is a valid credit card number based on the following logic:

- Doubles every second digit from the right.  
- If doubling results in a number greater than 9, 9 is subtracted from it (mimicking digit summation).  
- Adds all adjusted digits together.  
- The number is **valid** if the total sum is divisible by 10.

This process is adapted from the **Luhn Algorithm**, used in real-world credit card validation (simplified here for 8-digit inputs).

---

## 🧠 Core Class: `CreditCardChecker`

### Method
```java
public static boolean check(int creditNum)
```
Validates the given number and returns `true` if it passes the check, `false` otherwise.

**Algorithm Steps:**
1. Extract digits from right to left.
2. Double every second digit.
3. If doubling > 9, subtract 9.
4. Sum all digits.
5. Return `true` if the sum is divisible by 10.

---

## 🧪 Example Usage
```java
public class Main {
    public static void main(String[] args) {
        int validNum = 12345670; // Example of a valid 8-digit number
        int invalidNum = 87654321;

        System.out.println(validNum + " is valid? " + CreditCardChecker.check(validNum));
        System.out.println(invalidNum + " is valid? " + CreditCardChecker.check(invalidNum));
    }
}
```

### Sample Output
```
12345670 is valid? true
87654321 is valid? false
```

---

## ⚙️ How to Run

1. Ensure **Java (JDK 8+)** is installed.  
2. Save both `CreditCardChecker.java` and `Main.java` in the same folder.  
3. Compile and execute:
   ```bash
   javac CreditCardChecker.java Main.java
   java Main
   ```

---
