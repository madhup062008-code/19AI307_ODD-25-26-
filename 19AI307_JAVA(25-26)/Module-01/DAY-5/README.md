# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to calculate the power of a given number using a built-in math function.

### Sample Input
```text
3
2
```

### Sample Output
```text
3.0 raised to the power of 2.0 is: 9.0
```

## AIM:

To write a Java program to compute the power of a number using the `Math.pow()` function.

## ALGORITHM:

1. Start the program and import `java.util.Scanner`.
2. Read the base number as a `double`.
3. Read the exponent as a `double`.
4. Compute the result using `Math.pow(base, exponent)`.
5. Display the base, exponent, and computed result.
6. Stop the program.

## PROGRAM:

```java
/*
Program to implement Strings and Math Function using Java
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
        double base = sc.nextDouble();
        double exp = sc.nextDouble();

        double result = Math.pow(base, exp);

        System.out.println(base + " raised to the power of " + exp + " is: " + result);
    }
}
```

## OUTPUT:

```text
3.0 raised to the power of 2.0 is: 9.0
```

## RESULT:

Thus, the Java program was successfully implemented using the `Math.pow()` function to calculate the power of a given number.
