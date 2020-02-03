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

