# Ex.No:5(C) FILE HANDLING USING JAVA

## QUESTION:

Write a Java program to write a string to a text file named `output.txt` using `FileWriter`. Display a confirmation message after successfully writing the data.

## AIM:

To demonstrate file handling in Java by writing text into a file using `FileWriter`.

## ALGORITHM:

1. Start the program.
2. Import the required I/O classes.
3. Store the text to be written in a string.
4. Create a `FileWriter` for `output.txt`.
5. Write the string into the file using `write()`.
6. Close the `FileWriter`.
7. Display a success message.
8. Stop the program.

## PROGRAM:

```java
/*
Program to write a string into a text file using Java file handling.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.io.FileWriter;
import java.io.IOException;

public class Prog {
    public static void main(String[] args) throws IOException {
        String content = "Hello, this is a sample file written by ALLEN PRAKASH J.";

        FileWriter writer = new FileWriter("output.txt");
        writer.write(content);
        writer.close();

        System.out.println("Successfully wrote to the file.");
    }
}
```

## OUTPUT:

```text
Successfully wrote to the file.
```

## RESULT:

Thus, the Java program to write a string into output.txt using FileWriter was executed successfully.
