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



## JavaScript Call by Value and Call by Reference Interview Questions

1. **Explain the difference between call by value and call by reference in JavaScript. Can you give an example of each?**

   - **Answer:** 
     - **Call by value**: JavaScript passes primitive data types (like numbers, strings, booleans) by value. Changes inside the function do not affect the original variable.
     - **Call by reference**: JavaScript passes reference types (like objects and arrays) by reference, so changes inside the function affect the original object or array.

   - **Example:**
     ```js
     // Call by value
     let num = 10;
     function changeValue(x) {
       x = 20;
     }
     changeValue(num);
     console.log(num);  // Output: 10
     ```

     ```js
     // Call by reference
     let obj = { name: "Alice" };
     function modifyObject(o) {
       o.name = "Bob";
     }
     modifyObject(obj);
     console.log(obj);  // Output: { name: "Bob" }
     ```

2. **If JavaScript uses "call by value" for both primitive and reference types, why do objects behave as though they are passed by reference?**

   - **Answer:** 
     JavaScript passes a copy of the reference when dealing with objects. The reference itself is passed by value, but it allows modification of the object.

3. **What happens if you reassign an object parameter inside a function?**

   - **Answer:** 
     Reassigning an object parameter inside a function only changes the local reference, not the original object.

   - **Example:**
     ```js
     let obj = { name: "Alice" };
     function modifyObject(o) {
       o = { name: "Bob" };
     }
     modifyObject(obj);
     console.log(obj);  // Output: { name: "Alice" }
     ```

4. **Can you simulate pass by reference behavior for primitive types in JavaScript?**

   - **Answer:** 
     You can wrap primitives in an object to simulate pass by reference.

   - **Example:**
     ```js
     let value = { num: 5 };
     function modifyPrimitive(val) {
       val.num = 10;
     }
     modifyPrimitive(value);
     console.log(value.num);  // Output: 10
     ```

5. **What happens if you try to modify an object property inside a function but also reassign it?**

   - **Answer:** 
     Modifying an object's property affects the original object, but reassigning the object only affects the local reference.

   - **Example:**
     ```js
     let obj = { name: "Alice", details: { age: 25 } };
     function modifyObject(o) {
       o.name = "Bob";
       o = { name: "Charlie" };
     }
     modifyObject(obj);
     console.log(obj);  // Output: { name: "Bob", details: { age: 25 } }
     ```

6. **Are arrays passed by value or by reference in JavaScript? How can you prove it?**

   - **Answer:** 
     Arrays are passed by reference. Modifying the array inside the function affects the original array.

   - **Example:**
     ```js
     let arr = [1, 2, 3];
     function modifyArray(a) {
       a[0] = 10;
     }
     modifyArray(arr);
     console.log(arr);  // Output: [10, 2, 3]
     ```

7. **How can you prevent an object from being modified inside a function, despite JavaScript's call by reference behavior?**

   - **Answer:** 
     Use `Object.freeze()` to make an object immutable.

   - **Example:**
     ```js
     let obj = { name: "Alice" };
     Object.freeze(obj);
     function modifyObject(o) {
       o.name = "Bob";
     }
     modifyObject(obj);
     console.log(obj);  // Output: { name: "Alice" }
     ```

8. **How does the spread operator (`...`) behave in terms of call by value and reference?**

   - **Answer:** 
     The spread operator creates a shallow copy, meaning nested objects are still passed by reference.

   - **Example:**
     ```js
     let obj = { name: "Alice", details: { age: 25 } };
     let copy = { ...obj };
     copy.name = "Bob";
     copy.details.age = 30;
     console.log(obj.details.age);  // Output: 30
     ```

9. **Does JavaScript support true pass by reference, where the variable's reference can be changed from inside the function?**

   - **Answer:** 
     No, JavaScript does not support true pass by reference. You can modify the contents of an object, but not the reference itself.

10. **How does JavaScript handle the immutability of primitive data types when passed into functions?**

    - **Answer:** 
      Primitive types are immutable, so JavaScript passes a copy into the function, leaving the original variable unchanged.

    - **Example:**
      ```js
      let str = "Hello";
      function changeString(s) {
        s = "World";
      }
      changeString(str);
      console.log(str);  // Output: Hello
      ```

---
## Contributing

Feel free to contribute by adding more questions, improving answers, or suggesting new categories!

---

