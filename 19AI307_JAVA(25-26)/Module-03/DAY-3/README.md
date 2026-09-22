# Ex.No:3(C) ABSTRACTION

## QUESTION:

In a secret intelligence facility, encrypted messages are stored as arrays of characters. Each type of agent has a different way to decode these messages. Define an abstract class `Decoder` with a method `decodeMessage(String[] fragments)`.

**AlphaAgent:** Extracts a meaningful string by rearranging the fragments based on even indices first, then odd indices, and then reversing the final result.

**BetaAgent:** Picks all fragments that start and end with the same letter, joins them with `-`, and removes all vowels from the resulting string.

**Input Format:**

- First line: Integer N (number of fragments)
- Next N lines: the string fragments
- Next line: 1 for AlphaAgent, 2 for BetaAgent

## AIM:

To implement abstraction using an abstract `Decoder` class and different decoding behaviours in `AlphaAgent` and `BetaAgent` subclasses.

## ALGORITHM:

1. Start the program.
2. Create an abstract class `Decoder` with an abstract `decodeMessage()` method.
3. In `AlphaAgent`, collect fragments at even indices, then at odd indices, into one merged array.
4. Build the final string by appending the merged array's elements in reverse order.
5. In `BetaAgent`, select fragments whose first and last characters match, joining them with `-`.
6. Remove all vowels from the joined result in `BetaAgent`.
7. Read the fragments and the agent type, then call the matching decoder.
8. Display the decoded message.
9. Stop the program.

## PROGRAM:

```java
/*
Program to implement abstraction using different message decoding agents in Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.Scanner;

abstract class Decoder {
    abstract String decodeMessage(String[] fragments);
}

class AlphaAgent extends Decoder {
    String decodeMessage(String[] fragments) {
        int n = fragments.length;
        String[] merged = new String[n];
        int idx = 0;

        for (int i = 0; i < n; i += 2) merged[idx++] = fragments[i];
        for (int i = 1; i < n; i += 2) merged[idx++] = fragments[i];

        StringBuilder result = new StringBuilder();
        for (int i = n - 1; i >= 0; i--) result.append(merged[i]);

        return result.toString();
    }
}

class BetaAgent extends Decoder {
    String decodeMessage(String[] fragments) {
        StringBuilder joined = new StringBuilder();

        for (String frag : fragments) {
            if (frag.charAt(0) == frag.charAt(frag.length() - 1)) {
                if (joined.length() > 0) joined.append("-");
                joined.append(frag);
            }
        }

        return joined.toString().replaceAll("[aeiouAEIOU]", "");
    }
}

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        String[] fragments = new String[n];

        for (int i = 0; i < n; i++) {
            fragments[i] = sc.next();
        }

        int type = sc.nextInt();
        Decoder agent = (type == 1) ? new AlphaAgent() : new BetaAgent();

        System.out.println(agent.decodeMessage(fragments));
    }
}
```

## OUTPUT:

```text
osloechoomegabravoalpha
```

## RESULT:

Thus, the Java program to implement abstraction using AlphaAgent and BetaAgent decoders was executed successfully.
