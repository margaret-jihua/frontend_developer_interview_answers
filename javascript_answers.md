1. Explain event delegation.

    - Event delegation is away you can add an event listener once for multiple elements with support for adding extra children.

    - Attaching event listeners to parent node, instead of every child, present or newly created, is event delegation. It makes use of event bubbling, where the event on a child bubbles up to the parent. So instead of adding an event listener to a child, and adding one every time a new child is added, we add the listener on parent.

    - [Source](https://www.youtube.com/watch?v=pKzf80F3O0U)

2. Explain how `this` works in JavaScript.
  * Can you give an example of one of the ways that working with `this` has changed in ES6?

    - `this` references the object that is executing the current function

    - [Source](https://www.youtube.com/watch?v=gvicrj31JOM)

3. Explain how prototypal inheritance works.

    - JavaScript only has one construct: objects. Each object has an internal link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. null, by definition, has no prototype, and acts as the final link in this prototype chain.

    - [Source](https://medium.com/@nupoor_neha/javascript-front-end-interview-questions-1cbc5e32792b)

4. What's the difference between a variable that is: `null`, `undefined` or undeclared?
  * How would you go about checking for any of these states?

    - undefined is a variable that has been declared but no value exists and is a type of itself ‘undefined’.
    - null is a value of a variable and is a type of object.
    - We can use ‘console.log();’ and ‘type of’ to check if a variable is undefined or null.
    - undeclared variables is a variable that has been declared without ‘var’ keyword.

5. What is a closure, and how/why would you use one?

    - A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function.

    - Closures are inner functions inside of an outer function. They have their own local scope and has access to outer function’s scope, parameters (but NOT arguments object), and they also have access to global variables.
    - Closures is a neat way to deal with scope issues. Reasons we use Closures is because Javascript is a function-level scope rather than as with other languages, block-level scope and Javascript is an asynchronous/event driven language. Example that Closure is frequently used is jQuery (ex. click()).

    - [Source](https://medium.com/@rlynjb/js-interview-question-what-is-a-closure-and-how-why-would-you-use-one-b6fd45ea95f6)

6. What language constructions do you use for iterating over object properties and array items?

    -   for loop, for..in, forEach, map, filter 

7. Can you describe the main difference between the `Array.forEach()` loop and `Array.map()` methods and why you would pick one versus the other?

    - forEach() — executes a provided function once for each array element.
    - map() — creates a new array with the results of calling a provided function on every element in the calling array.
    - The forEach() method doesn’t return anything. It simply calls a provided function on each element in the array. This callback is allowed to mutate the calling array.Meanwhile, the map() method will also call a provided function on every element in the array. The difference is that map() returns a new Array of the same size.

8. What's a typical use case for anonymous functions?

    - Anonymous Functions are function expressions (rather than the regular function declaration which are statements. Function expressions are more flexible.) We can assign functions to variables, object properties, pass them as arguments to other functions, and even write a simple one line code enclosed in an anonymous functions.

    `var squaredArray = inputArray.map(function(x) { return x * x; });`

    `var squaredArray = inputArray.map(x => x * x);`

9. What's the difference between host objects and native objects?

    - [Source](https://medium.com/@rlynjb/js-interview-question-what-s-the-difference-between-host-objects-and-native-objects-b395f7c5fbf1)

10. Explain the difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?

    - 

11. Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`

    - first one is declaration defined at parse time while the other is expression defined at run time.

* Can you explain what `Function.call` and `Function.apply` do? What's the notable difference between the two?
* Explain `Function.prototype.bind`.
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain "hoisting".
* Describe event bubbling.
* Describe event capturing.
* What's the difference between an "attribute" and a "property"?
* What are the pros and cons of extending built-in JavaScript objects?
20. What is the difference between `==` and `===`?

    - `=` is called as assignment operator, `==` is called as comparison operator whereas It is also called as comparison operator. `=` does not return true or false, `==` Return true only if the two operands are equal while `===` returns true only if both values and data types are the same for the two variables

* Explain the same-origin policy with regards to JavaScript.
* Why is it called a Ternary operator, what does the word "Ternary" indicate?
* What is strict mode? What are some of the advantages/disadvantages of using it?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* What are the differences between variables created using `let`, `var` or `const`?
* What are the differences between ES6 class and ES5 function constructors?
* Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions?
* What advantage is there for using the arrow syntax for a method in a constructor?
* What is the definition of a higher-order function?
* Can you give an example for destructuring an object or an array?
* Can you give an example of generating a string with ES6 Template Literals?
* Can you give an example of a curry function and why this syntax offers an advantage?
* What are the benefits of using `spread syntax` and how is it different from `rest syntax`?
* How can you share code between files?
* Why you might want to create static class members?
* What is the difference between `while` and `do-while` loops in JavaScript?
* What is a promise? Where and how would you use promise?

## Coding questions
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
* What will be returned by each of these?
```javascript
console.log("hello" || "world")
console.log("foo" && "bar")
```
* Write an immediately invoked function expression (IIFE)
```
(function() {
  console.log("I am an IIFE!")
  console.log("You cannot call me again because I am anonymous function.")
  console.log("BUT, I still am going to run because I have been immediately called after I was defined.")
})();
```
(https://www.freecodecamp.org/news/learn-these-core-javascript-concepts-in-just-a-few-minutes-f7a16f42c1b0/)