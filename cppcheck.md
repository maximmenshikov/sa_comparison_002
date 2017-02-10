# cppcheck 1.76 warning informativeness according to 5W+1H system.

## Environment

* Ubuntu 16.10


## Methodology.

We are checking which questions does Clang answer for different warnings. We have checked lighttpd-1.4.43.

## Intermediate results.

Below are warnings we got (minus some obviously bogus) and their analysis.

### [path:line]: (style) The scope of the variable 'x' can be reduced.

* What: The scope of the variable can be reduced.

* Where: File, line.

### [path1] -> [path2]: (warning) Either the condition '0!=x' is redundant or there is possible null pointer dereference: x.

* What: Either the condition is redundant or there is possible null pointer dereference.

* When: When condition is not met.

* Where: File, line.

### [path:line]: (error) Return value of allocation function 'x' is not stored.

* What: Return value of allocation function is not stored.

* Where: File, line.

### [path:line]: (error) Memory leak: x

* What: Memory leak.

* Where: File, line, resource.

### [path:line]: (style) Variable 'x' is assigned a value that is never used.

* What: Variable value is unused.

* Where: File, line.

### [path:line]: (style) Unused variable: x

* What: Unused variable.

* Where: File, line.

### [path:line]: (style) Condition 'x==0' is always true

* What: Condition is always true

* Where: File, line.

### [path:line]: (error) #error neither X nor Y nor Z are defined

* What: Undefined macros.

* Where: File, line.
