# Ex.No:5(A) INPUTSTREAMREADER

## QUESTION:

Write a Java program to demonstrate chaining of streams using `BufferedReader` on top of `InputStreamReader` on top of `System.in`. Read the user's name and age and display the details.

## AIM:

To demonstrate stream chaining in Java using `System.in`, `InputStreamReader`, and `BufferedReader` for reading input.

## ALGORITHM:

1. Start the program.
2. Wrap `System.in` inside an `InputStreamReader`.
3. Wrap the `InputStreamReader` inside a `BufferedReader`.
4. Read the name using `readLine()`.
5. Read the age line and parse it into an integer.
6. Display the user's details.
7. Close the `BufferedReader`.
8. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate chaining of input streams using Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Prog {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        String name = reader.readLine();
        int age = Integer.parseInt(reader.readLine());

        System.out.println("--- User Details ---");
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);

        reader.close();
    }
}
```

## OUTPUT:

```text
--- User Details ---
Name: Ram
Age: 25
```

## RESULT:

Thus, the Java program to demonstrate chaining of BufferedReader, InputStreamReader, and System.in was executed successfully.
