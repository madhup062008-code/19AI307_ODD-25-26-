# Ex.No:3(E) INNER CLASS/ ENUM

## QUESTION:

Write a Java program to create an enum `Season` with values `WINTER`, `SPRING`, `SUMMER`, and `FALL`. Use a switch statement to display a custom message based on the current season.

**For example:**

Input:

```text
winter
```

Output:

```text
It's cold outside. Stay warm!
```

## AIM:

To create an enum in Java and use a switch statement to display a message based on the selected season.

## ALGORITHM:

1. Start the program.
2. Create the `Season` enum with `WINTER`, `SPRING`, `SUMMER`, and `FALL`.
3. Read the season name as a string and convert it to uppercase.
4. Convert the string into the matching enum constant using `valueOf()`.
5. Use a `switch` statement on the enum to select the correct message.
6. Display the message for the matched season.
7. Catch `IllegalArgumentException` for any invalid season name.
8. Stop the program.

## PROGRAM:

```java
/*
Program to implement an enum and switch statement using Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

enum Season {
    WINTER, SPRING, SUMMER, FALL
}

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.next().toUpperCase();

        try {
            Season season = Season.valueOf(input);
            switch (season) {
                case WINTER:
                    System.out.println("It's cold outside. Stay warm!");
                    break;
                case SPRING:
                    System.out.println("Flowers are blooming. Enjoy the fresh air!");
                    break;
                case SUMMER:
                    System.out.println("It's sunny and hot. Time for the beach!");
                    break;
                case FALL:
                    System.out.println("Leaves are falling. Autumn is beautiful!");
                    break;
            }
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid season entered.");
        }
    }
}
```

## OUTPUT:

```text
It's cold outside. Stay warm!
```

## RESULT:

Thus, the Java program to create an enum and display season-specific messages using a switch statement was executed successfully.
