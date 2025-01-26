# TypeScript Type Error Not Thrown
This example demonstrates a surprising behavior in TypeScript where a type error is not thrown when adding a number and a string.  TypeScript's type system is generally quite strict, but in this specific case, it does not throw the expected type error.

## Problem
The `add` function is defined to accept two numbers and return a number. However, when a string ('10') is passed as the second argument, TypeScript should ideally throw a type error. Instead, the code compiles without errors, and the result is the string concatenation of 5 and '10'.

## Solution
The solution involves using a stricter type checking mechanism, possibly by enabling the `strictNullChecks` compiler option or by performing explicit type guards within the function to ensure that both inputs are indeed numbers before performing the addition operation.