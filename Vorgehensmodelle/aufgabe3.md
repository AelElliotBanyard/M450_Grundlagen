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
# Aufgabe 3 - Bonus

```java
double calculatePrice(double baseprice, double specialprice, double extraprice, int extras, double discount) {
    double addon_discount;
    double result;

    if (extras >= 3) 
        addon_discount = 10;
    else if (extras >= 5)
        addon_discount = 15;
    else 
        addon_discount = 0;

    if (discount > addon_discount)
        addon_discount = discount;

    result = baseprice/100.0 * (100-addon_discount) + specialprice
            + extraprice/100.0 * 100;  // Apply addon_discount to extraprice

    return result;
}
```