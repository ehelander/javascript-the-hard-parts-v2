# Notes

## [Thread of Execution](https://frontendmasters.com/courses/javascript-hard-parts-v2/thread-of-execution/)

- JavaScript does 2 things:
  1. Executes code line-by-line (the thread of execution)
  2. Saves data in memory
- Variable and function names: *identifiers*.
- When a `const` doesn't yet have a value (as when being assigned the output of a function), it is *unitialized* (vs. as is used to be: `undefined`).

## [Functions](https://frontendmasters.com/courses/javascript-hard-parts-v2/functions/)

- Execution context:
  - Created to run the code of a function
  - Comprised of:
    - Thread of execution
      - How many threads of execution are there in JavaScript? One. So we can only do one thing at a time.
        - This comes into play more with asynchronous JavaScript.
    - Memory
      - 'Local' when not in the global execution context.
  - The overall 'program': Global execution context.
  - In the execution context we:
    - Store the input: parameter (label) and argument (value)
  - The function call *evaluates to* the result.

## [Call Stack](https://frontendmasters.com/courses/javascript-hard-parts-v2/call-stack/)

- JavaScript keeps track of which function is currently running via the *call stack*.
  - We only interact with the top thing in the call stack.
    - The `return` keyword indicates we should pop the current function off the call stack.
    - As soon as you start running JavaScript, we add `global()` on the bottom of the stack.