# Exercise 9.1.2.4

## Consider the following BNF:

```
A ::= 0 B | 0 M | 0 B M
0 ::= "w" | "x" | "s" | "m"
B ::= "i" | "f" | "c" | "r"
M ::= "o" | "t" | "p" | "a" | "h"
```
###(a) How many nonterminal symbols are in the grammar?
There are 4 nonterminal symbols: A, 0, B, M

###(b) How many terminal symbols are in the grammar?
All letters in quotes are terminal symbols

###(c) Write two strings that are valid according to the BNF.
 "sip", "mro"
###(d) For each of your two strings, give two valid mutants of the string.
 "sia"
 "mrt"
###(e) For each of your two strings, give two invalid mutants of the string.
 "sim" "mic"