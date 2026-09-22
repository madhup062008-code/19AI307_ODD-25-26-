# Ex.No:4(E) DESIGN PATTERN -- BEHAVIOUR PATTERN

## QUESTION:

Design a Java product management system using the Model-View-Controller (MVC) approach. Create a `Product` model to store the product name, price, and code. Create a view to display the product details and a controller to update the product price and refresh the view automatically.

## AIM:

To implement separation of model, view, and controller responsibilities in a Java product management system and demonstrate automatic view refresh after updating the model.

## ALGORITHM:

1. Start the program.
2. Create the `Product` model with `name`, `price`, and `code` fields, with getters and a price setter.
3. Create a `ProductView` class with a `displayProduct()` method.
4. Create a `ProductController` class that holds a `Product` and a `ProductView`.
5. Read the product's name, price, code, and the new price.
6. Create the controller with the initial details and call `updateView()`.
7. Call `updatePrice()` with the new price to update the model and refresh the view.
8. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate model, view, and controller separation in a Java product management system.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

class Product {
    private String name;
    private double price;
    private String code;

    Product(String name, double price, String code) {
        this.name = name;
        this.price = price;
        this.code = code;
    }

    String getName() { return name; }
    double getPrice() { return price; }
    String getCode() { return code; }
    void setPrice(double price) { this.price = price; }
}

class ProductView {
    void displayProduct(String name, double price, String code) {
        System.out.println("--- Product Details ---");
        System.out.println("Name : " + name);
        System.out.println("Price: " + price);
        System.out.println("Code : " + code);
    }
}

class ProductController {
    private Product product;
    private ProductView view;

    ProductController(String name, double price, String code) {
        product = new Product(name, price, code);
        view = new ProductView();
    }

    void updateView() {
        view.displayProduct(product.getName(), product.getPrice(), product.getCode());
    }

    void updatePrice(double newPrice) {
        product.setPrice(newPrice);
        view.displayProduct(product.getName(), product.getPrice(), product.getCode());
    }
}

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        ProductController controller = new ProductController(sc.next(), sc.nextDouble(), sc.next());
        controller.updateView();
        controller.updatePrice(sc.nextDouble());
    }
}
```

## OUTPUT:

```text
--- Product Details ---
Name : Laptop
Price: 55000.0
Code : P101
--- Product Details ---
Name : Laptop
Price: 52000.0
Code : P101
```

## RESULT:

Thus, the Java program to implement model, view, and controller separation and update the product price with automatic view refresh was executed successfully.
