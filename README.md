# Unexpected Behavior of Logical Indexing on Empty Arrays within a Function in MATLAB

This repository demonstrates an uncommon bug in MATLAB related to logical indexing on empty arrays within a function's scope.  The behavior differs from when the same operation is performed outside the function.

## Problem Description
When performing logical indexing on an empty array within a MATLAB function, the results may be unexpected and inconsistent with the behavior when performing the same operation in the base workspace. This is likely due to how MATLAB handles variable scoping and the implicit creation of empty arrays within the function's context.

## Steps to Reproduce
1. Run the `bug.m` script. 
2. Observe that the variable 'result' unexpectedly contains the value 'anotherValue', even though the expected behavior based on the condition should have set it to someValue.

## Solution
The `bugSolution.m` file demonstrates a solution to address this inconsistency. By explicitly handling the case of empty arrays before performing logical indexing, we avoid the unexpected behavior and guarantee consistent results.

## Additional Notes
This bug might be subtle and challenging to detect, especially in large, complex MATLAB projects. Understanding how MATLAB handles scope and empty arrays is crucial for writing robust and predictable code.