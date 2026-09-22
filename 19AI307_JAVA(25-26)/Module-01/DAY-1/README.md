# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
```Lovely is learning java basics, can you teach her the different types of datatypes in java? Write a program that uses all datatypes and print them all.

Input Format:

byte - 24

short - 11000

int - 1,34,500

long - 24,23,10,34

float - 24.20

double - 1,30,000.80

boolean - true/false

char - 'u'

String -"Heyyy, Lovely, Let's learn java!"
```
## AIM:
To write a Java program that demonstrates all basic datatypes and prints their values.

## ALGORITHM :
1.	Start the program and declare variables of all datatypes (byte, short, int, long, float, double, boolean, char, String).
2. Assign the given input values to each variable.
3. Print each variable with a proper label.
4. Ensure numeric values with commas (like 1,34,500) are written without commas in Java.
5. End the program after all values are displayed.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: MADHU .P
RegisterNumber: 212225040215
*/

```

## Sourcecode.java:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        byte inp1=sc.nextByte();
        short inp2=sc.nextShort();
        int inp3=sc.nextInt();
        long inp4=sc.nextLong();
        float inp5=sc.nextFloat();
        double inp6=sc.nextDouble();
        boolean inp7=sc.nextBoolean();
        char inp8=sc.next().charAt(0);
        sc.nextLine();
        String inp9=sc.nextLine();
        System.out.println("Hey Lovely, let's print all types of data received from user using different data types");
        System.out.println("This is byte datatype "+inp1);
        System.out.println("This is short datatype "+inp2);
        System.out.println("This is int datatype "+inp3);
        System.out.println("This is long datatype "+inp4);
        System.out.println("This is float datatype "+inp5);
        System.out.println("This is double datatype "+inp6);
        System.out.println("This is boolean datatype "+inp7);
        System.out.println("This is char datatype "+inp8);
        System.out.println("This is string datatype "+inp9);
    }
}
```
## OUTPUT:
<img width="1377" height="799" alt="image" src="https://github.com/user-attachments/assets/1f9fae82-e549-4efe-b0a3-f39f6dcadd22" />



## RESULT:
Thus,the program executed successfully and printed all the datatypes with their values.

