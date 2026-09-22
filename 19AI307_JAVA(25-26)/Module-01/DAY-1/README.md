# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:

Write a Java program that reads a person's name, age, and a favorite decimal number from the user, and prints them back using three different output methods:

- `System.out.print()` to print a greeting using the name.
- `System.out.println()` to print a line stating the age.
- `System.out.printf()` to print the favorite number rounded to exactly 2 decimal places.

### Input Format
- First line: String — the person's name (no spaces)
- Second line: Integer — the person's age
- Third line: Decimal — the person's favorite number

### Sample Input
```text
Lovely
20
3.14
```

### Sample Output
```text
Hello, Lovely
You are 20 years old
Your favorite number is 3.14
```

## AIM:

To write a Java program that demonstrates the difference between `print()`, `println()`, and `printf()` using values entered by the user.

## ALGORITHM:

1. Start the program and import `java.util.Scanner`.
2. Create a `Scanner` object to read console input.
3. Read the name as a string, the age as an integer, and the favorite number as a double.
4. Print a greeting message using `System.out.print()`, ending it with a manual newline.
5. Print the age message using `System.out.println()`.
6. Print the favorite number formatted to two decimal places using `System.out.printf()` with the `%.2f` specifier.
7. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate print(), println() and printf() in Java
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

        String name = sc.next();
        int age = sc.nextInt();
        double favNum = sc.nextDouble();

        System.out.print("Hello, " + name + "\n");
        System.out.println("You are " + age + " years old");
        System.out.printf("Your favorite number is %.2f", favNum);
    }
}
```

## OUTPUT:

```text
Hello, Lovely
You are 20 years old
Your favorite number is 3.14
```

## RESULT:

Thus, the Java program was successfully executed to demonstrate the use of `print()`, `println()`, and `printf()` for displaying output in different formats.
