# Ex.No:3(D) INTERFACE

## QUESTION:

You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.

**Bot Types:**

- `SunBot`: Predicts `"HOT"` if temperature > 30, else `"MODERATE"`.
- `RainBot`: Predicts `"COLD"` if temperature < 20, else `"WARM"`.

**Input:**

- temperature
- botType (1 for SunBot, 2 for RainBot)

**For example:**

```text
35 1
```

```text
HOT
```

## AIM:

To implement an interface in Java and provide different weather predictions through classes implementing the common interface.

## ALGORITHM:

1. Start the program.
2. Define a `Bot` interface with the method `predict(int temp)`.
3. Implement `SunBot`, returning `HOT` above 30 degrees and `MODERATE` otherwise.
4. Implement `RainBot`, returning `COLD` below 20 degrees and `WARM` otherwise.
5. Read the temperature and the bot type.
6. Create the corresponding bot object based on the type.
7. Call `predict()` and display the result.
8. Stop the program.

## PROGRAM:

```java
/*
Program to implement an interface using Java weather prediction bots.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

interface Bot {
    String predict(int temp);
}

class SunBot implements Bot {
    public String predict(int temp) {
        return (temp > 30) ? "HOT" : "MODERATE";
    }
}

class RainBot implements Bot {
    public String predict(int temp) {
        return (temp < 20) ? "COLD" : "WARM";
    }
}

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temp = sc.nextInt();
        int botType = sc.nextInt();

        Bot bot = (botType == 1) ? new SunBot() : new RainBot();

        System.out.println(bot.predict(temp));
    }
}
```

## OUTPUT:

```text
HOT
```

## RESULT:

Thus, the Java program to implement a common interface for weather prediction bots was executed successfully.
