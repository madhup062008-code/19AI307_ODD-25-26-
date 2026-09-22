# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:

You are creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create `Button` and `Checkbox` objects for `dark` and `light` themes. Let the user choose the theme, generate the corresponding UI components, and display their types.

## AIM:

To implement the Abstract Factory design pattern in Java by creating related Button and Checkbox objects for different themes.

## ALGORITHM:

1. Start the program.
2. Define `Button` and `Checkbox` interfaces.
3. Create light and dark implementations of both interfaces.
4. Define a `UIFactory` interface with methods to create a button and a checkbox.
5. Create `LightUIFactory` and `DarkUIFactory` implementing `UIFactory`.
6. Read the selected theme and create the matching factory.
7. Use the factory to create and render a button and a checkbox.
8. Stop the program.

## PROGRAM:

```java
/*
Program to implement the Abstract Factory design pattern for light and dark UI themes using Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

interface Button { void render(); }
interface Checkbox { void render(); }

class LightButton implements Button {
    public void render() { System.out.println("Light Button created"); }
}
class DarkButton implements Button {
    public void render() { System.out.println("Dark Button created"); }
}
class LightCheckbox implements Checkbox {
    public void render() { System.out.println("Light Checkbox created"); }
}
class DarkCheckbox implements Checkbox {
    public void render() { System.out.println("Dark Checkbox created"); }
}

interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

class LightUIFactory implements UIFactory {
    public Button createButton() { return new LightButton(); }
    public Checkbox createCheckbox() { return new LightCheckbox(); }
}

class DarkUIFactory implements UIFactory {
    public Button createButton() { return new DarkButton(); }
    public Checkbox createCheckbox() { return new DarkCheckbox(); }
}

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String theme = sc.next();

        UIFactory factory;
        if (theme.equalsIgnoreCase("light")) factory = new LightUIFactory();
        else if (theme.equalsIgnoreCase("dark")) factory = new DarkUIFactory();
        else {
            System.out.println("Invalid theme");
            return;
        }

        Button b = factory.createButton();
        Checkbox c = factory.createCheckbox();
        b.render();
        c.render();
    }
}
```

## OUTPUT:

```text
Dark Button created
Dark Checkbox created
```

## RESULT:

Thus, the Java program to implement the Abstract Factory design pattern for light and dark UI components was executed successfully.
