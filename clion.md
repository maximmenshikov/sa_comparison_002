# CLion warning informativeness according to 5W+1H system.

## Methodology.

We are checking which questions does CLion answer for different warnings. We have checked lighttpd-1.43, and definitely got a lot of false positives. However, our goal is to find question rate.

## Intermediate results.

### Data flow analysis / Context-sensitive analysis / Unreachable code.
* What: Unreachable code.

* Where: file, line.

### Data flow analysis / Context-sensitive analysis / Casting to probably incompatible type.
* What: castng to probably incompatible type

* Where: file, line.

### Data flow analysis / Context-sensitive analysis / Condition is always true (+* When reached).
* What: Condition is always true (+* When reached)

* Where: file, line.

How to fix: buttons to remove condition or to turn it to 1.

### Data flow analysis / Not initialized variable / Local variable 'x' might not have been initialized.
* What: Not initialized variable.

* Where: file, line.

* Why: Local variable 'x' might not have been initialized.

* How to fix: Initialize local variable 'x'

### General / Local value escapes scope / Value escapes the local scope.
* What: value escapes the local scope

* Where: file, line.

### General / Loop condition isn't updated inside the loop / Local variables used in loop condition are not updated in the loop.
* What: This may cause an infinite loop if executed and is probably not * What was intended.

* Where: file, line.

* Why: Local variables used in loop condition are not updated in the loop.

### General / Missing switch case / Default case is not handled.
* What: Default case is not handled.

* Where: file, line.

### General / Simplifiable statement / Expression can be simplified to 'x'.
* What: Expression can be simplified to 'x'.

* How to fix: 'Simplify expression'.

### General / Condition is always false.
* What: Condition is always false.

* How to fix: Button to remove block under condition.

### General / 'If' statement has identical branches.
* What: 'If' statement has identical branches.

* Where: file, line.

* How to fix: remove branch.

## Type checks / Const expression required / Initializer of the static global variable must be const.
* What: Initializer of the static global variable must be const.

* Where: File, line.

* How to fix: Make parameter 'x' const.

## Type checks / Implicit integer and enum conversion / Taking enum type 'x' from integer.
* What: Implicit integer and enum conversion.

* Where: File, line.

* Why: Taking enum type 'x' from integer.

* How to fix: Cast expression.

## Type checks / Implicit integer and enum conversion / Enum 'x' has no constant to represent the integer value 'y'.
* What: Implicit integer and enum conversion.

* Where: File, line.

* Why: Enum 'x' has no constant to represent the integer value 'y'.

* How to fix: Cast expression to 'x'.

## Type checks / Implicit pointer and integer conversion / Taking integer from pointer 'x*' without a cast.
* What: Implicit pointer and integer conversion.

* Where: File, line.

* Why: Taking integer from pointer 'x*' without a cast.

* How to fix: Cast expression to 'int', change type of parameter 'a' to 'int'.

## Type checks / Incompatible pointers / Parameter type mismatch: Incompatible pointer types 'a*' and 'b*'.
* What: Parameter type mismatch: Incompatible pointer types 'a*' and 'b*'.

* Where: File, line.

* How to fix: Cast expression, change type.

## Type checks / Incompatible pointers / Incompatible pointer types 'const a* const' and 'a*'.
* What: Incompatible pointer types 'const a* const' and 'a*'.

* Where: File, line.

* How to fix: Cast expression, change type.

## Type checks / Redundant cast / Casting expression to 'a*' is redundant.
* What: Casting expression to 'a*' is redundant.

* Where: File, line.

* How to fix: Remove redundant cast.

## Type checks / Signedness mismatch / Using 'unsigned a' for signed values of type 'const a'.
* What: Using 'unsigned a' for signed values of type 'const a'. Signedness mismatch.

* Where: File, line.

* How to fix: Cast expression to 'unsigned a', change type of parameter 'b' to 'unsigned a *'.


## Type checks / Value may not fit into receiver / Values of type 'a' may not fit into the receiver type 'b'.
* What: Values of type 'a' may not fit into the receiver type 'b'.

* Where: File, line.

* Why: The range of values of type b is not large enough to store all possible values of type a.

* How to fix: Cast expression to 'x', change type of field 'y' to 'x'.

## Unused code / Unused x.
* What: x is never used.

* Where: File, line.

* How to fix: Remove x.
