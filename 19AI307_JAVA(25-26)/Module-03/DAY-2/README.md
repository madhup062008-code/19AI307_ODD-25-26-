# Ex.No:3(B) POLYMORPHISM

## QUESTION:

Write a Java program that calculates the area of different shapes using method overloading. Create a class `AreaCalculator` with:

- `area(int side)` for square
- `area(int length, int breadth)` for rectangle
- `area(double radius)` for circle

**For example:**

```text
4
5 6
3.0
```

```text
Area of square: 16
Area of rectangle: 30
Area of circle: 28.274333882308138
```

## AIM:

To implement compile-time polymorphism using method overloading for calculating the areas of different shapes.

## ALGORITHM:

1. Start the program.
2. Create a class `AreaCalculator`.
3. Define three overloaded `area()` methods for square, rectangle, and circle.
4. Read the side of the square and call the matching overload.
5. Read the length and breadth of the rectangle and call the matching overload.
6. Read the radius of the circle and call the matching overload.
7. Display all three calculated areas.
8. Stop the program.

## PROGRAM:

```java
/*
Program to implement polymorphism using method overloading in Java.
Developed by: ALLEN PRAKASH J
RegisterNumber: 212225040017
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

class AreaCalculator {
    int area(int side) {
        return side * side;
    }
    int area(int length, int breadth) {
        return length * breadth;
    }
    double area(double radius) {
        return Math.PI * radius * radius;
    }
}

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        AreaCalculator calc = new AreaCalculator();

        int side = sc.nextInt();
        System.out.println("Area of square: " + calc.area(side));

        int length = sc.nextInt();
        int breadth = sc.nextInt();
        System.out.println("Area of rectangle: " + calc.area(length, breadth));

        double radius = sc.nextDouble();
        System.out.println("Area of circle: " + calc.area(radius));
    }
}
```

## OUTPUT:

```text
Area of square: 16
Area of rectangle: 30
Area of circle: 28.274333882308138
```

## RESULT:

Thus, the Java program to calculate the area of different shapes using method overloading was executed successfully.
