# Ex.No:2(A) CLASSES AND OBJECTS

## QUESTION:

Create a class `Car` with attributes `brand`, `model`, `year`. Create 2 objects and print their details.

**For example:**

```text
Car 1: Toyota Innova 2022
Car 2: Hyundai i20 2021
```

## AIM:

To create a Java class with attributes, create two objects, assign values through a constructor, and display their details.

## ALGORITHM:

1. Start the program.
2. Create a class `Car` with fields `brand`, `model`, and `year`, and a constructor to initialize them.
3. Create two `Car` objects by passing values through the constructor.
4. Define a `display()` method that prints a car's details.
5. Call `display()` for both objects.
6. Stop the program.

## PROGRAM:

```java
/*
Program to create a class and objects in Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
public class Prog {
    public static void main(String[] args) {
        Car car1 = new Car("Toyota", "Innova", 2022);
        Car car2 = new Car("Hyundai", "i20", 2021);

        car1.display(1);
        car2.display(2);
    }
}

class Car {
    String brand;
    String model;
    int year;

    Car(String brand, String model, int year) {
        this.brand = brand;
        this.model = model;
        this.year = year;
    }

    void display(int index) {
        System.out.println("Car " + index + ": " + brand + " " + model + " " + year);
    }
}
```

## OUTPUT:

```text
Car 1: Toyota Innova 2022
Car 2: Hyundai i20 2021
```

## RESULT:

Thus, the Java program to create a class, create two objects, and display their details was executed successfully.
