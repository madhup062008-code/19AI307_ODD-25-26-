# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Write a program to access a static variable using both class name and object.

**For example:**

```text
48
```

Expected output:

```text
Accessing using class name: 48
Accessing using object: 48
```

## AIM:

To access a static variable using both the class name and an object in Java.

## ALGORITHM:

1. Start the program.
2. Declare a static integer variable `number` in the class.
3. Read a value into it using `Scanner`.
4. Access and print the variable using the class name.
5. Create an object of the class.
6. Access and print the same variable using the object reference.
7. Stop the program.

## PROGRAM:

```java
/*
Program to access a static variable using class name and object.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

public class Prog {
    static int number;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        number = sc.nextInt();

        System.out.println("Accessing using class name: " + Prog.number);

        Prog p = new Prog();
        System.out.println("Accessing using object: " + p.number);
    }
}
```

## OUTPUT:

```text
Accessing using class name: 48
Accessing using object: 48
```

## RESULT:

Thus, the Java program to access a static variable using both class name and object was executed successfully.
