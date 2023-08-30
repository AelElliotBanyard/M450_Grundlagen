# Aufgabe 2
## Software-Fehler
### Ein Beispiel für einen Softwarefehler könnte eine Division duch Null sein
```java
public class DivisionExample {
    public static void main(String[] args) {
        int numerator = 10;
        int denominator = 0;
        
        int result = numerator / denominator;
        System.out.println("Ergebnis: " + result);
    }
}
```
### Ein Beispiel für einen hohen Schaden bei dem obigen Software-Fehler könnte zum Beispiel eine fehlerhafte Zinsberechnungs sein

## Software-Mangel
### Ein Beispiel für einen Softwaremangel könnte eine fehlende Eingabeüberprüfung sein
Code ohne Überprüfung:
```java
import java.util.Scanner;

public class InputValidationExample {
    public static void main(String[] args) {
        String name = getUserInput("Geben Sie Ihren Namen ein: ");
        int age = getValidAge("Geben Sie Ihr Alter ein: ");
        String email = getValidEmail("Geben Sie Ihre E-Mail-Adresse ein: ");
        
        System.out.println("Name: " + name);
        System.out.println("Alter: " + age);
        System.out.println("E-Mail: " + email);
    }
    
    public static String getUserInput(String prompt) {
        System.out.print(prompt);
        Scanner scanner = new Scanner(System.in);
        return scanner.nextLine();
    }
}
```

Zusätzlicher Code zur Überprüfung des Users und der Email:
```java
public static int getValidAge(String prompt) {
        while (true) {
            String ageStr = getUserInput(prompt);
            try {
                int age = Integer.parseInt(ageStr);
                if (age >= 0) {
                    return age;
                } else {
                    System.out.println("Bitte geben Sie ein positives Alter ein.");
                }
            } catch (NumberFormatException e) {
                System.out.println("Ungültige Eingabe. Bitte geben Sie eine Zahl ein.");
            }
        }
    }

    public static String getValidEmail(String prompt) {
        while (true) {
            String email = getUserInput(prompt);
            if (email.contains("@")) {
                return email;
            } else {
                System.out.println("Bitte geben Sie eine gültige E-Mail-Adresse ein.");
            }
        }
    }
```

