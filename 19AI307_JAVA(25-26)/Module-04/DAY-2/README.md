# Ex.No:4(B) IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM

## QUESTION:

Implement the Observer pattern for a smart-city Air Quality Index (AQI) sensor network. Create a `SensorNetwork` as the subject and controller classes as observers: `GreenZoneController` (AQI < 100), `AlertZoneController` (AQI between 100 and 200), and `DangerZoneController` (AQI > 200), each reacting only to its corresponding range.

## AIM:

To implement the Observer design pattern in Java by allowing AQI controllers to receive and process sensor notifications according to their assigned ranges.

## ALGORITHM:

1. Start the program.
2. Define a `ZoneObserver` interface with a `check(sensorId, aqi)` method.
3. Implement `GreenZoneController`, `AlertZoneController`, and `DangerZoneController`, each acting only within its own AQI range.
4. Create a `SensorNetwork` class holding a list of registered observers.
5. Register all three controllers with the sensor network.
6. Read the number of readings, then each sensor ID and AQI value.
7. For each reading, notify all registered observers through the sensor network.
8. Stop the program.

## PROGRAM:

```java
/*
Program to implement the Observer pattern for an AQI monitoring system using Java.
Developed by: MADHU .P
RegisterNumber: 212225040215
*/
```

## Sourcecode.java:

```java
import java.util.*;

interface ZoneObserver {
    void check(String sensorId, int aqi);
}

class GreenZoneController implements ZoneObserver {
    public void check(String sensorId, int aqi) {
        if (aqi < 100)
            System.out.println("[GreenZoneController]: AQI is good at Sensor " + sensorId + ". No action needed.");
    }
}

class AlertZoneController implements ZoneObserver {
    public void check(String sensorId, int aqi) {
        if (aqi >= 100 && aqi <= 200)
            System.out.println("[AlertZoneController]: Moderate AQI at Sensor " + sensorId + ". Send public health alert.");
    }
}

class DangerZoneController implements ZoneObserver {
    public void check(String sensorId, int aqi) {
        if (aqi > 200)
            System.out.println("[DangerZoneController]: Critical AQI at Sensor " + sensorId + "! Trigger lockdown protocol.");
    }
}

class SensorNetwork {
    private List<ZoneObserver> observers = new ArrayList<>();

    void register(ZoneObserver obs) {
        observers.add(obs);
    }

    void receiveData(String id, int aqi) {
        System.out.println("Sensor " + id + " reports AQI: " + aqi);
        for (ZoneObserver obs : observers) {
            obs.check(id, aqi);
        }
    }
}

public class Prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        SensorNetwork network = new SensorNetwork();

        network.register(new GreenZoneController());
        network.register(new AlertZoneController());
        network.register(new DangerZoneController());

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] parts = sc.nextLine().trim().split("\\s+");
            network.receiveData(parts[0], Integer.parseInt(parts[1]));
        }
    }
}
```

## OUTPUT:

```text
Sensor S1 reports AQI: 50
[GreenZoneController]: AQI is good at Sensor S1. No action needed.
Sensor S2 reports AQI: 150
[AlertZoneController]: Moderate AQI at Sensor S2. Send public health alert.
Sensor S3 reports AQI: 250
[DangerZoneController]: Critical AQI at Sensor S3! Trigger lockdown protocol.
```

## RESULT:

Thus, the Java program to implement the Observer pattern for an AQI sensor network was executed successfully.
