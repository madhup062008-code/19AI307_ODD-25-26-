# Ex.No:5(E) MULTITHREADING - SYNCHRONIZATION

## QUESTION:

Write a Java program to read N integers from the user and use a fixed thread pool of size 3 to process each number. Each task must multiply its input by 2 and return the result. Display the results in the same order as the input.

## AIM:

To demonstrate multithreading in Java using a fixed thread pool and process multiple tasks while preserving the order of their results.

## ALGORITHM:

1. Start the program.
2. Read the number of tasks, T.
3. Create a fixed thread pool of size 3 using `Executors.newFixedThreadPool(3)`.
4. For each input number, submit a task that multiplies it by 2, storing the returned `Future` in a list.
5. Iterate over the list of `Future` objects in input order.
6. Call `get()` on each to retrieve and display its result.
7. Shut down the thread pool.
8. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate a fixed thread pool for processing multiple tasks concurrently in Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.*;
import java.util.concurrent.*;

public class Prog {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        int t = sc.nextInt();

        ExecutorService pool = Executors.newFixedThreadPool(3);
        List<Future<Integer>> futures = new ArrayList<>();

        for (int i = 0; i < t; i++) {
            int num = sc.nextInt();
            futures.add(pool.submit(() -> num * 2));
        }

        for (Future<Integer> f : futures) {
            System.out.println("Result: " + f.get());
        }

        pool.shutdown();
    }
}
```

## OUTPUT:

```text
Result: 10
Result: 20
Result: 30
```

## RESULT:

Thus, the Java program to process multiple tasks using a fixed thread pool of size 3 and display the results in input order was executed successfully.
