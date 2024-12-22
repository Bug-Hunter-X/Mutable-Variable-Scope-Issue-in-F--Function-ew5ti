# F# Mutable Variable Scope Bug

This repository demonstrates a common, yet subtle, bug in F# related to the use of mutable variables within functions. The code in `bug.fs` shows how modifying mutable variables within a function unexpectedly changes global variable values. The solution is provided in `bugSolution.fs`.

## Problem Description

The issue arises from unexpected side effects when using mutable variables within a function.  The function alters global variables used before the function is called, resulting in different output than what might be initially expected.

## Solution

The solution illustrates how to avoid unexpected mutable variable side effects by creating local copies of variables and working with them, leaving the original variables unchanged, or by avoiding mutable variables altogether when possible. 

## How to reproduce

1. Clone this repository.
2. Open `bug.fs` and compile using an F# compiler (e.g., `fsharpc bug.fs`).
3. Execute the compiled code. Note the incorrect output.
4. Open `bugSolution.fs`, compile it, and run the code.  Observe the correct output demonstrating how to avoid side effects.