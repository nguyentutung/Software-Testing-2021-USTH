# Exercise 4.1
## Calc.java

```java
package com.company;

public class Calc {
    static public int add(int a, int b) {
        return a + b;
    }

    static public int subtract(int a, int b) {
        return a - b;
    }

    static public int multiply(int a, int b) {
        return a * b;
    }

    static public double divide (int a, int b)
    {
        return (float) a/b;
    }
}
```

## TestCalc.java

```java
package com.company;

import org.junit.Test;
import static org.junit.Assert.*;

public class TestCalc {
    Calc calc = new Calc();
    private int a = 6;
    private int b = 3;

    @Test
    public void testAdd() {
        assertEquals(calc.add(a, b), 9);
    }

    @Test
    public void testsubtract() {
        assertEquals(calc.subtract(a, b), 3);
    }

    @Test
    public void testMultiply() {
        assertEquals(calc.multiply(a, b), 18);
    }

    @Test
    public void testDivide() {
        assertEquals(calc.divide(a, b), 2, 0);
    }
}
```
