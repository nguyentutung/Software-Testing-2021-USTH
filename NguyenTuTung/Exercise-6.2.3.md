# Exercise 6.2.3

## Write down all 16 tests to satisfy Multiple Base Choice coverage (MBCC) for the second categorization of triang()’s inputs inTable 6.2. Use the values in Table 6.3.
### Code
```java
public enum Triangle {
   SCALENE, ISOSCELES, EQUILATERAL, INVALID
}
public class TriangleType
{
   /**
     * @param s1, s2, s3:  sides of the putative triangle
     * @return enum describing type of triangle
     */
   public static Triangle triangle (int s1, int s2, int s3)
   {
      // Reject non-positive sides
      if (s1 <= 0 || s2 <= 0 || s3 <= 0)
         return (Triangle.INVALID);

      // Check triangle inequality
      if (s1+s2 <= s3 || s2+s3 <= s1 || s1+s3 <= s2)
         return (Triangle.INVALID);

      // Identify equilateral triangles
      if ((s1 == s2) && (s2 == s3))
         return Triangle.EQUILATERAL;

      // Identify isosceles triangles
      if ((s1 == s2) || (s2 == s3) || (s1 == s3))
         return Triangle.ISOSCELES;

      return (Triangle.SCALENE);
   }
}
```
### Tables
#### Table 6.2
|Partition|b1|b2|b3|b4|
|---|---|---|---|---|
|side1|>1|=1|=0|<0|
|side2|>1|=1|=0|<0|
|side3|>1|=1|=0|<0|

#### Table 6.3

|Partition|b1|b2|b3|b4|
|---|---|---|---|---|
|side1|2|1|0|-1|
|side2|2|1|0|-1|
|side3|2|1|0|-1|

### Test case

#### Multiple Base Choice Coverage (MBCC) :  At least one, and possibly more, base choice blocks are chosen for each characteristic, and base tests are formed by using each base choice for each characteristic at least once. Subsequent tests are chosen by holding all but one base choice constant for each base test and using each non-base choice in each other characteristic.

```
{(2, 2, 2), //F irst base test
(0, 2, 2),(−1, 2, 2), 
(2, 1, 2),(2, 0, 2),(2, −1, 2), 
(2, 2, 1),(2, 2, 0),(2, 2, −1), 
{(1, 2, 2), //Second base test
(0, 2, 2),(−1, 2, 2), 
(1, 1, 2),(1, 0, 2),(1, −1, 2),
(1, 2, 1),(1, 2, 0),(1, 2, −1), 



}
```
