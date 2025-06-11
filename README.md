# 200 + JavaScript-Interview-Questions-with-Answer 🔥

## ✅ **Basic JavaScript Concepts (Beginner - Intermediate)**
### 🔹 **1. What is JavaScript?**

**JavaScript** is a **high-level, interpreted programming language** primarily used to create **dynamic and interactive content** on websites.

* **Runs in the browser** (and on servers via Node.js)
* Follows **ECMAScript** standards
* Can manipulate HTML/CSS, handle events, validate forms, and interact with APIs

🧠 **Example:**

```html
<button onclick="alert('Hello World!')">Click Me</button>
```



### 🔹 **2. What are the features of JavaScript?**

* **Lightweight** and **interpreted**
* **Object-oriented**
* **First-class functions** (functions can be treated like variables)
* **Event-driven**
* **Platform-independent**
* **Asynchronous and single-threaded** (with support for promises/async-await)



### 🔹 **3. How is JavaScript different from Java?**

| Feature     | JavaScript                  | Java             |
| ----------- | --------------------------- | ---------------- |
| Type System | Dynamically typed           | Statically typed |
| Platform    | Runs in browser and Node.js | Runs on JVM      |
| Syntax      | Simple, scripting           | Strict, OOP      |
| Compilation | Interpreted                 | Compiled         |
| Inheritance | Prototype-based             | Class-based      |

🧠 Example:

```js
// JavaScript
let x = 5;
```

```java
// Java
int x = 5;
```



### 🔹 **4. Explain the data types in JavaScript**

JavaScript has **8 data types**:

#### ✅ Primitive (immutable):

1. **String** - e.g., `"Hello"`
2. **Number** - e.g., `10`, `3.14`
3. **BigInt** - large integers (`123n`)
4. **Boolean** - `true`, `false`
5. **Undefined** - uninitialized variables
6. **Null** - explicitly empty
7. **Symbol** - unique identifiers

#### ✅ Non-primitive:

8. **Object** - arrays, functions, dates, etc.

🧠 Example:

```js
let name = "John"; // String
let age = 25; // Number
let active = true; // Boolean
let user = { name: "John", age: 25 }; // Object
```


### 🔹 **5. What are variables in JavaScript?**

Variables are used to **store data** that can be reused or modified later.

🧠 Example:

```js
let name = "Alice";
const PI = 3.14;
```



### 🔹 **6. Difference between var, let, and const**

| Keyword | Scope    | Redeclare | Reassign | Hoisted                   |
| ------- | -------- | --------- | -------- | ------------------------- |
| var     | Function | Yes       | Yes      | Yes (but undefined)       |
| let     | Block    | No        | Yes      | Yes (but not initialized) |
| const   | Block    | No        | No       | Yes (but not initialized) |

🧠 Example:

```js
var x = 10;
let y = 20;
const z = 30;
```


### 🔹 **7. What is hoisting in JavaScript?**

**Hoisting** means variable and function declarations are **moved to the top** of their scope **during the compilation phase**, but only `var` is initialized as `undefined`.

🧠 Example:

```js
console.log(x); // undefined
var x = 5;

console.log(y); // ReferenceError
let y = 10;
```



### 🔹 **8. What are JavaScript reserved keywords?**

These are **predefined words** that have special meaning and **cannot be used as identifiers**.

🧠 Examples:

```js
var, let, const, if, else, while, return, function, class, new, this, typeof, etc.
```



### 🔹 **9. What are primitive vs non-primitive data types?**

| Type          | Mutable? | Stored by | Examples            |
| ------------- | -------- | --------- | ------------------- |
| Primitive     | No       | Value     | String, Number      |
| Non-Primitive | Yes      | Reference | Object, Array, Func |

🧠 Example:

```js
let str = "Hello"; // primitive
let obj = { name: "John" }; // non-primitive
```



### 🔹 **10. What is type coercion?**

**Type coercion** is the automatic or implicit conversion of values from one data type to another.

🧠 Example:

```js
console.log("5" + 1); // "51" (Number to String)
console.log("5" - 1); // 4 (String to Number)
```



### 🔹 **11. Explain NaN property**

**NaN** stands for "**Not-a-Number**" and indicates an **invalid number result**.

🧠 Example:

```js
console.log("abc" - 2); // NaN
console.log(typeof NaN); // "number"
```



### 🔹 **12. What is the typeof operator?**

Used to **check the data type** of a variable.

🧠 Example:

```js
typeof "hello" // "string"
typeof 42      // "number"
typeof true    // "boolean"
typeof {}      // "object"
typeof null    // "object" (quirk in JS)
```



### 🔹 **13. What are truthy and falsy values?**

JavaScript treats values as **truthy or falsy** in boolean contexts (like `if` statements).

#### ✅ Falsy values:

* `false`
* `0`, `-0`
* `""` (empty string)
* `null`
* `undefined`
* `NaN`

#### ✅ Everything else is **truthy**

🧠 Example:

```js
if ("hello") { console.log("Truthy"); }
if (0) { console.log("Falsy"); } // won't run
```


### 🔹 **14. What is the difference between == and ===?**

| Operator | Name            | Compares     | Example           |
| -------- | --------------- | ------------ | ----------------- |
| `==`     | Loose Equality  | Value        | "5" == 5 → true   |
| `===`    | Strict Equality | Value + Type | "5" === 5 → false |

🧠 Example:

```js
console.log(0 == false);  // true
console.log(0 === false); // false
```



### 🔹 **15. What is null vs undefined?**

| Type        | Meaning                         | Default |
| ----------- | ------------------------------- | ------- |
| `undefined` | Variable declared, not assigned | Yes     |
| `null`      | Intentional absence of value    | No      |

🧠 Example:

```js
let a;
console.log(a); // undefined

let b = null;
console.log(b); // null
```



### 🔹 **16. What is the scope of a variable?**

**Scope** refers to the **accessibility** of variables.

* **Global Scope** – available everywhere
* **Function Scope** – available within a function
* **Block Scope** – available within `{}` (with `let` & `const`)

🧠 Example:

```js
var x = 10; // global

function test() {
  let y = 20; // function scope
  if (true) {
    const z = 30; // block scope
  }
}
```



### 🔹 **17. What is lexical scope?**

Lexical scope means a function has access to variables in its **outer (parent) scope** during **definition time**, not invocation time.

🧠 Example:

```js
function outer() {
  let outerVar = "I am outside!";
  function inner() {
    console.log(outerVar);
  }
  inner();
}
outer(); // Output: I am outside!
```



### 🔹 **18. What is a block scope?**

Block scope means variables declared with `let` or `const` inside `{}` are only accessible within that block.

🧠 Example:

```js
{
  let a = 5;
  const b = 10;
  // both a and b are block-scoped
}
// console.log(a); // Error
```


### 🔹 **19. What is a global scope?**

Variables declared **outside any function or block** have global scope and can be accessed anywhere.

🧠 Example:

```js
let globalVar = "Hello";

function greet() {
  console.log(globalVar);
}

greet(); // Hello
```



### 🔹 **20. What are template literals?**

Template literals are string literals **enclosed in backticks (`` ` ``)** that allow:

* Multi-line strings
* String interpolation using `${}`

🧠 Example:

```js
let name = "Alice";
let message = `Hello, ${name}!
Welcome to JavaScript.`;
console.log(message);
```


