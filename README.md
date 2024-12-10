# Julia Integer Overflow Bug

This repository demonstrates a subtle integer overflow bug in a simple Julia function.  The function `myfunction` squares its input if the input is greater than 10, otherwise it increments the input by 1.  The problem arises when the square of the input exceeds the maximum representable integer value. 

The `bug.jl` file contains the buggy code.  The `bugSolution.jl` file provides a corrected version that mitigates the overflow issue.

## How to Reproduce

1. Clone this repository.
2. Run `bug.jl` using a Julia interpreter.  Observe the output for both small and very large inputs. You might need to test with unusually large inputs to reveal the issue.
3. Run `bugSolution.jl`. Note the improved behavior.

## Solution

The solution involves using appropriate data types (like BigInt) to handle potentially large integer calculations, preventing overflow.