# Functions & Callbacks

## [Generalized Functions](https://frontendmasters.com/courses/javascript-hard-parts-v2/generalized-functions/)

- DRY: Don't Repeat Yourself
- Parameters (placeholders) mean we don't have to decide what data to run our functionality on until we run the function.
  - But this isn't just limited to data: We can leave some of our functionality TBD &rarr; higher-order functions.

## [Repeating Functionality](https://frontendmasters.com/courses/javascript-hard-parts-v2/repeating-functionality/)

## [Higher Order Functions](https://frontendmasters.com/courses/javascript-hard-parts-v2/higher-order-functions/)

- A higher-order function: Passing functionality as a parameter

## [Higher Order Functions Example](https://frontendmasters.com/courses/javascript-hard-parts-v2/higher-order-functions-example/)

- We left a placeholder for *what we're going to do* for each item in the array.
- We made the function *general, reusable*. We can't edit functions, but we can adjust their behavior this way.

## [Higher Order Functions Q&A](https://frontendmasters.com/courses/javascript-hard-parts-v2/higher-order-functions-q-a/)

- We're passing in a *reference to where it's originally saved in global memory* &rarr; which is why we don't want to change the array.
- Any function, array, or object, when we save it and use it elsewhere, we're using the original reference.
- A protected namespace (such as inside a `for` loop) is different than a new execution context.

## [Callbacks & Higher Order Functions](https://frontendmasters.com/courses/javascript-hard-parts-v2/callbacks-higher-order-functions/)

- Functions in JavaScript are first-class objects.
  - They have all the features of objects and can be treated just like any other object.
    - Behind the scenes, arrays and functions are just objects.
    - So they can be:
      - Assigned to variables and properties of other objects.
        - Function stored as a property of another object: A method.
      - Passed as arguments into functions.
      - Returned as values from functions.
        - Decalred, defined inside the function, and passed out. This gives us *closure*.
- ![Learn Higher Order Functions Example – JavaScript/ The Hard Parts, v2 2020-02-02 19-27-20](./Learn&#32;Higher&#32;Order&#32;Functions&#32;Example&#32;–&#32;JavaScript:&#32;The&#32;Hard&#32;Parts,&#32;v2&#32;2020-02-02&#32;19-27-20.png)
  - The outer function that takes in a function is our *higher-order function*.
    - Any function that *takes in* or *returns out* a function is a higher-order function in JavaScript.
  - The function we insert is our *callback function*.
  - Higher-order functions and callback functions keep our code DRY.
    - Because we can 'edit' the function after we create it, making our code much more re-usable.
    - So we can write more declarative, more readable code.
    - Note that the `copyArrayAndManipulate` function is equivalent to `map`.
      - `filter`, `map`, etc. is much more *declarative* - you're not defining how it has to happen.
- Passing a function into another function is going to be core to asynchronous programming (regardless of whether we're using async/await, promises, etc.)

## [Arrow Functions](https://frontendmasters.com/courses/javascript-hard-parts-v2/arrow-functions/)

- The designers of JavaScript love to reduce code.
  - Perhaps making it more *legible* (less code on the page), but less readable (more difficult to intuit at a glance).
- Arrow function
  - Inserts the `return` keyword and the curly braces behind the scenes.
- It's easier to *track* what's happening when we have a separately-defined function.
- Under-the-hood differences for arrow functions:
  - The `this` keyword assignment is treated differently.
- Are there any memory saving considerations when inlining a function?
  - Very small, in this context. But if we're saving a hundred functions to a thousand objects and dealing with recursion, yes. But, usually, the scarcest resource is a developer's understanding and time.

## [Pair Programming](https://frontendmasters.com/courses/javascript-hard-parts-v2/pair-programming/)

- What it means to be an engineer: To be able to hit a hard block, and figure out some way to resolve through it.
  - Debugging: Going through the code line-by-line and understanding the data (the state). But we try *very* hard to avoid doing this.
- There are two traps when seeking to grow as a software engineer:
  - The researcher
    - Avoids blocks by reading everything they can find on their block/bug.
  - The Stackoverflower
    - Uses code snippets to fix bug without knowing how they work.
- Pair programming avoids these traps:
  - Tackle blocks with a partner
  - Stay focused on the problem
  - Refine technical communication
  - Collaborate to solve problem
- Pair programming process:
  - Navigator talks the driver through the strategy of writing code to solve the problem at hand.
