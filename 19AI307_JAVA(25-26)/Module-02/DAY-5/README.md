# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:

Create a class `SpeedLimit` with a final method `displayLimit()` that prints `"Max Speed: 80 km/h"`. Try to override it in a subclass. Show that overriding a final method is not allowed.

## AIM:

To demonstrate that a `final` method cannot be overridden in a subclass.

## ALGORITHM:

1. Start the program.
2. Create the `SpeedLimit` class with `displayLimit()` declared as `final`.
3. Print the speed limit message inside `displayLimit()`.
4. Create a `HighwaySpeed` subclass that extends `SpeedLimit` without overriding the final method (Java would not compile it otherwise).
5. Create a `HighwaySpeed` object referenced by a `SpeedLimit` variable.
6. Call `displayLimit()` on it.
7. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate the use of a final method in Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
class SpeedLimit {
    final void displayLimit() {
        System.out.println("Max Speed: 80 km/h");
    }
}

class HighwaySpeed extends SpeedLimit {
}

public class Prog {
    public static void main(String[] args) {
        SpeedLimit s = new HighwaySpeed();
        s.displayLimit();
    }
}
```

## OUTPUT:

```text
Max Speed: 80 km/h
```

## RESULT:

Thus, the Java program demonstrating that a final method cannot be overridden was executed successfully.
