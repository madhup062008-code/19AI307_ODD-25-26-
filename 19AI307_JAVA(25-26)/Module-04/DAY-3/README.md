# Ex.No:4(C) COMPOSITION IN JAVA

## QUESTION:

Implement a Java program in which a `Library` contains multiple `Book` objects. Each `Book` is created inside the `Library`, demonstrating composition. Read the number of books and their title and author, create the books through the `Library`, and display all books.

## AIM:

To implement composition in Java by creating and managing `Book` objects inside a `Library` object.

## ALGORITHM:

1. Start the program.
2. Create a `Book` class with private `title` and `author` fields set through its constructor.
3. Create a `Library` class holding a list of `Book` objects.
4. Add an `addBook()` method in `Library` that creates a `Book` and stores it internally.
5. Read the number of books and each book's title and author.
6. Call `addBook()` through the `Library` object for each entry.
7. Call `showBooks()` to display every stored book.
8. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate composition between Library and Book classes using Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.*;

class Book {
    private String title;
    private String author;

    Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> books = new ArrayList<>();

    void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println("- " + b.getDetails());
        }
    }
}

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
    }
}
```

## OUTPUT:

```text
Books in Library:
- Java Basics by James Gosling
- Clean Code by Robert Martin
```

## RESULT:

Thus, the Java program to demonstrate composition by creating Book objects inside a Library was executed successfully.
