# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:

A locker system accepts a numeric code and decides access based on these rules:

- If the code is **odd**, or lies outside the range 0–999, access is **denied**.
- If the code is **even** and less than 100, it is classified as a **Weak Code**.
- If the code is **even** and lies between 100 and 999 (inclusive), it is classified as a **Strong Code**.

Write a Java program that reads a code and prints the correct classification.

### Sample Input
```text
42
```

### Sample Output
```text
Weak Code
```

## AIM:

To write a Java program using conditional (`if-else`) statements to classify a numeric code as "Weak Code", "Strong Code", or "Access Denied".

## ALGORITHM:

1. Start the program and import `java.util.Scanner`.
2. Create a `Scanner` object and read the integer code.
3. Check first whether the code is outside the valid range (less than 0 or greater than 999); if so, deny access.
4. Otherwise, check whether the code is odd; if so, deny access.
5. Otherwise (code is even and in range), check whether it is less than 100; if so, print "Weak Code".
6. Otherwise, print "Strong Code".
7. Close the Scanner and stop the program.

## PROGRAM:

```java
/*
Program to implement a conditional statement using Java
Developed by: ALLEN PRAKASH J
RegisterNumber: 212225040017
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int code = sc.nextInt();

        if (code < 0 || code > 999) {
            System.out.println("Access Denied");
        } else if (code % 2 != 0) {
            System.out.println("Access Denied");
        } else if (code < 100) {
            System.out.println("Weak Code");
        } else {
            System.out.println("Strong Code");
        }

        sc.close();
    }
}
```

## OUTPUT:

```text
Weak Code
```

## RESULT:

Thus, the Java program was successfully implemented using conditional statements to classify a given code as "Weak Code", "Strong Code", or "Access Denied".
