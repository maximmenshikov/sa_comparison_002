# PVS-Studio warning informativeness according to 5W+1H system.

## Methodology.

We are checking which questions does PVS-Studio answer for different warnings. We have checked lighttpd-1.43. Our goal is to find question rate.

## Intermediate results.

Below are warnings we got (minus some obviously bogus) and their analysis.

### V701 / realloc() possible leak: when realloc() fails in allocating memory, original pointer 'a' is lost. Consider assigning realloc() to a temporary pointer.

* What: original pointer is lost.

* When: When realloc fails in allocating memory.

* Where: File, line.

* How to fix: Consider assigning realloc() to a temporary pointer.

### V707 / Giving short names to global variables is considered to be bad practice. It is suggested to rename 'x' variable.

* What: bad practice.

* When: short name for global variable.

* Where: File, line.

* How to fix: rename 'x' variable.

### V595 / The 'x' pointer was utilized before it was verified against nullptr. Check lines y, z.

* What: The 'x' pointer was utilized before it was verified against nullptr.

* Where: File, lines y, z.

### V580 / An odd explicit type casting: (a * *) & b. Consider verifying it.

* What: An odd explicit type casting.

* Where: File, line.

### V610 / Unspecified behavior. Check the shift operator '>>'. The left operand is negative ('n' = [-1..10]).

* What: Unexpected behaviour due to the use of shift operator '>>'.

* When: The left operand is negative ('n' = [-1..10]).

* Where: File, line.

### V547 / Expression 'a' is always true/false.

* What: Expression is always true/false.

* Where: File, line.

### V560 / A part of conditional expression is always true/false: a.

* What: A part of conditional expression is always true/false: a.

* Where: File, line.

### V519 / The '* c' variable is assigned values twice successively. Perhaps this is a mistake. Check lines: y, z.

* What: The '* c' variable is assigned values twice successively.

* Where: File, lines y, z.

### V512 / A call of the 'memcpy' function will lead to the 'a' buffer becoming out of range.

* What: A call of the 'memcpy' function will lead to the 'a' buffer becoming out of range.

* Where: File, line.

### V734 / An excessive check. Examine the conditions containing search for the substrings "test" and "x-test".

* What: Excessive check.

* When: conditions containing search for the substrings "test" and "x-test".

* Where: File, line.

### V512 / A call of the 'memset' function will lead to underflow of the buffer '& a'.

* What: A call of the 'memset' function will lead to underflow of the buffer '& a'.

* Where: File, line.

### V575 / The 'a' function processes '0' elements. Inspect the first argument.

* What: function processes 0 elements.

* Where: File, line.

### V575 / The null pointer is passed into 'a' function. Inspect the second argument.

* What: The null pointer is passed into 'a' function.

* Where: File, line.

## Final results.

* What? 100%

* When? 30.8%

* Where? 100%

* Who? 0%

* Why? 0%

* How to fix? 15.4%

