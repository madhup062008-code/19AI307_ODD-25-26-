# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java program to find the average of `n` numbers stored in an array.

### Sample Input
```text
5
10
20
30
40
50
```

### Sample Output
```text
The average of elements is 30.00
```

## AIM:

To write a Java program to read elements into an array and compute the average of those elements.

## ALGORITHM:

1. Start the program and import `java.util.Scanner`.
2. Read the number of elements, `n`.
3. Create an integer array of size `n`.
4. Initialize a variable `total` to 0.
5. Using a `for` loop, read each element into the array and add it to `total`.
6. Compute the average as `total / n`, converting to a decimal result.
7. Display the average formatted to two decimal places.
8. Stop the program.

## PROGRAM:

```java
/*
Program to implement the Array concept using Java
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
        int[] arr = new int[n];
        int total = 0;

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
            total = total + arr[i];
        }

        double avg = (double) total / n;
        System.out.printf("The average of elements is %.2f", avg);
    }
}
```

## OUTPUT:

```text
The average of elements is 30.00
```

## RESULT:

Thus, the Java program was successfully implemented using an array and a `for` loop to calculate the average of the array elements.
