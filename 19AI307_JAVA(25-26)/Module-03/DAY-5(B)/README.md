# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to demonstrate the use of a Wrapper Class by converting a primitive integer value into an `Integer` object using autoboxing and converting the `Integer` object back into a primitive integer using unboxing. Display both values.

## AIM:

To demonstrate the use of the `Integer` wrapper class and the concepts of autoboxing and unboxing in Java.

## ALGORITHM:

1. Start the program.
2. Read an integer value using `Scanner`.
3. Assign the primitive value to an `Integer` object, letting Java autobox it.
4. Assign the `Integer` object back to a primitive `int`, letting Java unbox it.
5. Display the original primitive value, the wrapper object, and the unboxed value.
6. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate Wrapper Class using autoboxing and unboxing in Java.
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
        int primitiveValue = sc.nextInt();

        Integer wrapperObj = primitiveValue;
        int unboxedValue = wrapperObj;

        System.out.println("Primitive value: " + primitiveValue);
        System.out.println("Wrapper object: " + wrapperObj);
        System.out.println("Unboxed value: " + unboxedValue);
    }
}
```

## OUTPUT:

```text
Primitive value: 25
Wrapper object: 25
Unboxed value: 25
```

## RESULT:

Thus, the Java program to demonstrate the Integer Wrapper Class using autoboxing and unboxing was executed successfully.
