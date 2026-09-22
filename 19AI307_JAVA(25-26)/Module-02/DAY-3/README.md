# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

Write a Java program to create a class called `Smartphone` with private instance variables `brand`, `model`, and `storageCapacity`. Provide public getter and setter methods to access and modify these variables. Add a method called `increaseStorage()` that takes an integer value and increases the `storageCapacity` by that value.

## AIM:

To implement encapsulation using private instance variables, public getter and setter methods, and a method to increase storage capacity.

## ALGORITHM:

1. Start the program.
2. Create the `Smartphone` class with private fields `brand`, `model`, and `storageCapacity`.
3. Add public getter and setter methods for each field.
4. Add an `increaseStorage(int value)` method that adds the given value to `storageCapacity` when it is positive.
5. Read the brand, model, initial storage, and the amount to increase.
6. Call the setters to store the initial values, then call `increaseStorage()`.
7. Display the updated smartphone details.
8. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate encapsulation using getter, setter, and update methods.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    public String getBrand() { return brand; }
    public String getModel() { return model; }
    public int getStorageCapacity() { return storageCapacity; }

    public void setBrand(String brand) { this.brand = brand; }
    public void setModel(String model) { this.model = model; }
    public void setStorageCapacity(int storageCapacity) { this.storageCapacity = storageCapacity; }

    public void increaseStorage(int value) {
        if (value > 0) {
            storageCapacity += value;
        }
    }

    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
    }
}

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Smartphone phone = new Smartphone();

        phone.setBrand(sc.nextLine());
        phone.setModel(sc.nextLine());
        phone.setStorageCapacity(sc.nextInt());
        phone.increaseStorage(sc.nextInt());

        phone.display();
    }
}
```

## OUTPUT:

```text
Brand: Samsung
Model: GalaxyS21
Updated Storage Capacity: 192 GB
```

## RESULT:

Thus, the Java program to implement encapsulation using private variables and public methods was executed successfully.
