# F# Mutable Variable Swapping Issue

This example demonstrates a common misunderstanding in F# involving mutable variables and pass by value.  The `swap` function attempts to swap the values of `x` and `y`, but due to pass by value, it only modifies local copies within the function.

## Bug
The code in `bug.fs` attempts to swap two mutable variables. However, because F# uses pass by value for mutable variables, the swap operation within the function doesn't affect the original variables.

## Solution
The solution in `bugSolution.fs` shows how to correctly swap mutable variables using a tuple or by returning new values.