# Ex.No:2(B) METHOD AND PASSING VALUE

## QUESTION:

Write a method that tries to modify the passed value and print `"Inside method: "+num`.

Show in `main()` that the original value does not change.

After calling the method in `main`, print `"Outside method: "+num`.

**For example:**

```text
10
```

Expected output:

```text
Inside method: 20
Outside method: 10
```

## AIM:

To demonstrate that modifying a primitive `int` parameter inside a method does not change the original variable in `main()`.

## ALGORITHM:

1. Start the program.
2. Create a static method `modifyValue(int num)`.
3. Inside the method, add 10 to the local copy of `num` and print it.
4. In `main()`, read the original value using `Scanner`.
5. Call `modifyValue(num)`.
6. Print the original value again after the call to show it is unchanged.
7. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate parameter passing using an integer value.
Developed by: ALLEN PRAKASH J
RegisterNumber: 212225040017
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

public class Prog {
    static void modifyValue(int num) {
        num = num + 10;
        System.out.println("Inside method: " + num);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        modifyValue(num);
        System.out.println("Outside method: " + num);
    }
}
```

## OUTPUT:

```text
Inside method: 20
Outside method: 10
```

## RESULT:

Thus, the Java program demonstrating modification of a primitive value inside a method was executed successfully, and the original value remained unchanged.
