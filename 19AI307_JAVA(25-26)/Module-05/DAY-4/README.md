# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

Write a Java program to determine the priority and name of the current thread. Read the thread name from the user, set its priority to 5, and display the priority, thread name, and thread information.

## AIM:

To demonstrate how to set and retrieve the name and priority of the current thread in Java.

## ALGORITHM:

1. Start the program.
2. Read the desired thread name using `Scanner`.
3. Get a reference to the currently executing thread using `Thread.currentThread()`.
4. Set the thread's name to the entered value.
5. Set the thread's priority to 5.
6. Display the thread's priority, name, and full thread information.
7. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate thread name and priority using Java.
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
        String threadName = sc.nextLine();

        Thread current = Thread.currentThread();
        current.setName(threadName);
        current.setPriority(5);

        System.out.print("Priority of Thread: " + current.getPriority()
            + "\nName of Thread: " + current.getName()
            + "\n" + current);
    }
}
```

## OUTPUT:

```text
Priority of Thread: 5
Name of Thread: NewThread
Thread[NewThread,5,main]
```

## RESULT:

Thus, the Java program to determine and display the name and priority of the current thread was executed successfully.

> **Note:** The last line's exact format (`Thread[...]`) can vary slightly between Java versions — newer JDKs may print `Thread[#1,NewThread,5,main]` instead of `Thread[NewThread,5,main]`. This is a JDK version difference, not a logic error; check what your college's compiler prints.
