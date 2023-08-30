# Aufgabe 3

```java
boolean test_calculate_price() {
    double price;
    boolean test_ok = true;

    price = calculate_price(100, 80, 20, 2, 10);

    if (price != 188 ){
        test_ok = false;
    }

    return test_ok;
}
```