# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

Write a Java program that reads two integers and divides the first integer by the second integer. Handle the case when division by zero occurs using exception handling and display an appropriate error message.

## AIM:

To implement exception handling in Java by handling an `ArithmeticException` caused by division by zero.

## ALGORITHM:

1. Start the program.
2. Read two integers, `a` and `b`, using `Scanner`.
3. Inside a `try` block, divide `a` by `b` and print the result.
4. Catch `ArithmeticException` when `b` is zero.
5. Print an error message for the division-by-zero case.
6. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate exception handling using try and catch in Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();

        try {
            int result = a / b;
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) {
            System.out.println("Error: Division by zero");
        }
    }
}
```

## OUTPUT:

```text
Error: Division by zero
```

## RESULT:

Thus, the Java program to perform safe division and handle division by zero using exception handling was executed successfully.
