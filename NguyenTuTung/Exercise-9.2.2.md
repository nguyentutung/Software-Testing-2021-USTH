# Exercise 9.2.2

## Answer questions (a) through (d) for the mutant on line 5 in the method <span style="font-family:Courier">findVal()</span>.

```java
public static int findVal(int numbers[], int val)       
   {                                                       
      int findVal = -1;                                    
                                                        
      for (int i=0; i<numbers.length; i++)         // mutant        
      // for (int i=(0+1); i<numbers.length; i++)  
         if (numbers [i] == val)                         
            findVal = i;                                  
         return (findVal);                                    
   }
```

### (a) If possible, find test inputs that do not reach the mutant.
Can't find. 

### (b) If possible, find test inputs that satisfy reachability but not infection for the mutant
Can't find.

### (c) If possible, find test inputs that satisfy infection, but not propagation for the mutant.
([3, 0] ,1)

### (d) If possible, find test inputs that strongly kill the mutants.
([1, 2] ,1) 