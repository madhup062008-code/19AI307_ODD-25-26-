# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

Create a Super class `Person` with fields `name` and `age`. Create a subclass `Student` that inherits from `Person` and adds a field `marks` (integer). Implement a method in `Student` called `calculateGrade()` which returns the grade based on the marks:

- Marks >= 90: Grade A
- Marks >= 75 and < 90: Grade B
- Marks >= 50 and < 75: Grade C
- Marks < 50: Grade F

## AIM:

To implement inheritance by creating a superclass `Person` and a subclass `Student`, and to calculate a grade based on marks.

## ALGORITHM:

1. Start the program.
2. Create a superclass `Person` with `name` and `age` fields.
3. Create a subclass `Student` that extends `Person` and adds a `marks` field.
4. Define `calculateGrade()` in `Student` using the given mark ranges.
5. Read the student's name, age, and marks.
6. Call `calculateGrade()` and store the result.
7. Display the student's details and grade.
8. Stop the program.

## PROGRAM:

```java
/*
Program to implement inheritance and aggregation concepts using Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

class Person {
    String name;
    int age;
}

class Student extends Person {
    int marks;

    char calculateGrade() {
        if (marks >= 90) return 'A';
        else if (marks >= 75) return 'B';
        else if (marks >= 50) return 'C';
        else return 'F';
    }
}

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Student st = new Student();

        st.name = sc.next();
        st.age = sc.nextInt();
        st.marks = sc.nextInt();

        char grade = st.calculateGrade();

        System.out.printf("Name: %s\nAge: %d\nMarks: %d\nGrade: %c", st.name, st.age, st.marks, grade);
    }
}
```

## OUTPUT:

```text
Name: Jeeva
Age: 18
Marks: 95
Grade: A
```

## RESULT:

Thus, the Java program to implement inheritance and calculate the student grade based on marks was executed successfully.
