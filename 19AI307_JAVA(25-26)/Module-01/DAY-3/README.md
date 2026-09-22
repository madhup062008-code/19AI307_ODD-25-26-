# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Write a Java program that reads an integer and reverses its digits using a **while loop**, then displays the reversed number. (Any leading zeros produced by the reversal will naturally not be displayed, since they disappear in integer form.)

### Sample Input
```text
5600
```

### Sample Output
```text
Reversed number: 65
```

## AIM:

To write a Java program to reverse the digits of an integer using a `while` loop and the modulus operator.

## ALGORITHM:

1. Start the program and import `java.util.Scanner`.
2. Read the integer to be reversed.
3. Initialize a variable `rev` to 0.
4. While the number is greater than 0:
   - Extract its last digit using the modulus operator (`% 10`).
   - Append the digit to `rev` by computing `rev = rev * 10 + digit`.
   - Remove the last digit from the number using integer division (`/ 10`).
5. Once the loop ends, display `rev` as the reversed number.
6. Stop the program.

## PROGRAM:

```java
/*
Program to implement a Looping Statement using Java
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
        int n = sc.nextInt();
        int rev = 0;

        while (n > 0) {
            int digit = n % 10;
            rev = rev * 10 + digit;
            n = n / 10;
        }

        System.out.printf("Reversed number: %d", rev);
    }
}
```

## OUTPUT:

```text
Reversed number: 65
```

## RESULT:

Thus, the Java program was successfully implemented using a `while` loop to reverse the digits of a given integer.
