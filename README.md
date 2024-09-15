# JavaScript Interview Questions Repository

This repository contains a collection of **JavaScript interview questions** categorized into **Basic, Medium**, and **Advanced** levels. These questions cover important topics to help you prepare for JavaScript interviews or sharpen your JS skills.

## Table of Contents
- [Easy Questions](#easy-questions)
- [Medium Questions](#medium-questions)
- [Advanced Questions](#advanced-questions)
- [Questions and Answers](#questions-and-answers)

---

## Easy Questions

| Category                 | Question                                                                 |
|--------------------------|-------------------------------------------------------------------------|
| Data Types and Variables  | What is the difference between `var`, `let`, and `const` in JavaScript?  |
| Basic Operators           | What is the difference between `==` and `===` in JavaScript?             |
| Control Flow              | How does the `switch` statement work in JavaScript?                      |
| Functions                 | What is an arrow function, and how does it differ from regular functions?|
| Arrays and Objects        | How does the `map()` method work in JavaScript arrays?                   |

---

## Medium Questions

| Category                 | Question                                                                 |
|--------------------------|-------------------------------------------------------------------------|
| Closures and Scope        | What is a closure in JavaScript, and how is it used?                     |
| Asynchronous JavaScript   | What are promises, and how do they help manage asynchronous code?        |
| Prototype and Inheritance | What is prototypal inheritance in JavaScript?                            |

---

## Advanced Questions

| Category                 | Question                                                                 |
|--------------------------|-------------------------------------------------------------------------|
| Design Patterns in JavaScript | What is the Singleton pattern in JavaScript?                             |
| Event Delegation and Bubbling  | How does event delegation work in JavaScript?                            |

---

## Questions and Answers

### Easy Questions

**1. What is the difference between `var`, `let`, and `const` in JavaScript?**  
`var` is function-scoped and can be redeclared. `let` and `const` are block-scoped; however, `const` is used to declare constants and cannot be reassigned after initial declaration.

**2. What is the difference between `==` and `===` in JavaScript?**  
`==` checks for value equality, allowing type coercion. `===` checks for both value and type equality, without type coercion.

**3. How does the `switch` statement work in JavaScript?**  
The `switch` statement evaluates an expression and matches the value to a case. If a match is found, the corresponding block of code is executed. The `break` statement is used to prevent fall-through to other cases.

**4. What is an arrow function, and how does it differ from regular functions?**  
Arrow functions provide a shorter syntax and do not bind their own `this` value. They are ideal for non-method functions, and their syntax omits the `function` keyword.

**5. How does the `map()` method work in JavaScript arrays?**  
The `map()` method creates a new array by applying a callback function to each element of the original array, without modifying the original array.

---

### Medium Questions

**6. What is a closure in JavaScript, and how is it used?**  
A closure is a function that retains access to its lexical scope even when the function is executed outside of that scope. It allows for data encapsulation and is often used in module patterns.

**7. What are promises, and how do they help manage asynchronous code?**  
Promises represent the eventual result of an asynchronous operation. They simplify the handling of async tasks by providing `then()` and `catch()` methods to handle resolved and rejected outcomes, replacing traditional callbacks.

**8. What is prototypal inheritance in JavaScript?**  
Prototypal inheritance allows objects to inherit properties and methods from other objects. Each object has an internal link to its prototype, which is shared among all instances created from the same constructor function.

---

### Advanced Questions

**9. What is the Singleton pattern in JavaScript?**  
The Singleton pattern ensures that a class has only one instance and provides a global point of access to that instance. It is used to maintain a single object across the application lifecycle.

**10. How does event delegation work in JavaScript?**  
Event delegation allows you to attach a single event listener to a parent element instead of multiple listeners on individual child elements. It works by utilizing event bubbling, where events propagate up the DOM tree.

---

## Contributing

Feel free to contribute by adding more questions, improving answers, or suggesting new categories!

---

**Follow Gajendra Gangwar for more insightful tech content.**
