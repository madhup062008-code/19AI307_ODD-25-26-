# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION

## QUESTION:

Write a Java program to serialize a collection of `Student` objects stored in an `ArrayList` into a file named `students.dat`. Then deserialize the collection from the file and display the student details.

## AIM:

To demonstrate serialization and deserialization of a collection of Java objects using `ObjectOutputStream` and `ObjectInputStream`.

## ALGORITHM:

1. Start the program.
2. Create a `Student` class implementing `Serializable`.
3. Read the number of students and each student's id, name, and marks into an `ArrayList`.
4. Serialize the list into `students.dat` using `ObjectOutputStream`.
5. Deserialize the list back using `ObjectInputStream`.
6. Display each deserialized student's details.
7. Stop the program.

## PROGRAM:

```java
/*
Program to demonstrate serialization and deserialization of an ArrayList<Student> using Java.
Developed by: ALLEN PRAKASH J
RegisterNumber: 212225040017
*/
```

## Sourcecode.java:

```java
import java.io.*;
import java.util.*;

class Student implements Serializable {
    private static final long serialVersionUID = 1L;
    private int id;
    private String name;
    private double marks;

    Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class Prog {
    static void saveStudents(List<Student> list, String file) throws IOException {
        ObjectOutputStream out = new ObjectOutputStream(new FileOutputStream(file));
        out.writeObject(list);
        out.close();
        System.out.println("Students serialized successfully into: " + file);
    }

    @SuppressWarnings("unchecked")
    static List<Student> loadStudents(String file) throws IOException, ClassNotFoundException {
        ObjectInputStream in = new ObjectInputStream(new FileInputStream(file));
        List<Student> list = (List<Student>) in.readObject();
        in.close();
        System.out.println("Students deserialized successfully from: " + file);
        return list;
    }

    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = sc.nextInt();
        for (int i = 0; i < n; i++) {
            int id = sc.nextInt();
            String name = sc.next();
            double marks = sc.nextDouble();
            students.add(new Student(id, name, marks));
        }

        saveStudents(students, "students.dat");
        List<Student> loaded = loadStudents("students.dat");

        System.out.println();
        System.out.println("Deserialized Students:");
        for (Student s : loaded) {
            System.out.println(s);
        }
    }
}
```

## OUTPUT:

```text
Students serialized successfully into: students.dat
Students deserialized successfully from: students.dat

Deserialized Students:
Student{id=101, name='Alice', marks=89.5}
Student{id=102, name='Bob', marks=92.0}
```

## RESULT:

Thus, the Java program to serialize and deserialize a collection of Student objects was executed successfully.
