## CSCI3155 Lab 3: Solutions
#### Lincoln Samelson & Brent Hebert

**1)**

*(a)*
```
const x = 5;
const f = function (y) { return x };
const g = function (x) { return f(1) };
g(3)
```
Under dynamic scoping, g(3) returns 3 because the input scope for x is used as opposed to 'const x = 5'

**2)**

*(c)*
e1 MUST be evaluated before evaluating e2; thus, the rules enforce an evaluation order of left to right.  This makes it deterministic.

**3)**
To switch the evaluation order to right to left:
```
      e2 -> e2'
---------------------
e1 bop e2 -> e1 bop e2'


e1 -> e1' bop in{+, -, &, *}
----------------------------
  e1 bop e2 -> e1' bop e2
  
  
n' = n1 + n2
------------
n1 + n2 = n'
```

**4)**

*(a)*
False; '&& e2' is a good example because we don't have to evaluate e2, no matter how complex it may be.  We can simply ignore it due to short-circuiting. 

*(b)*
'e1 && e2' does short circuit because it includes the case:
```
--------------------
false && e2 -> false
```

