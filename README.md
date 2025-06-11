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



## ✅ **Control Structures and Loops**



### 🔹 **21. What are conditional statements in JavaScript?**

Conditional statements **control the flow of code execution** based on conditions (true/false).

#### ✅ Types:

* `if`
* `else if`
* `else`
* `switch`

🧠 **Example:**

```js
let age = 20;

if (age >= 18) {
  console.log("You are an adult.");
} else {
  console.log("You are a minor.");
}
```



### 🔹 **22. Difference between if, else if, and switch**

| Feature     | `if` / `else if` / `else`                  | `switch`                       |
| ----------- | ------------------------------------------ | ------------------------------ |
| Conditions  | Works with any expression (range, boolean) | Works with fixed values only   |
| Readability | Better for complex conditions              | Better for multiple values     |
| Fallthrough | No fallthrough                             | Can fall through if no `break` |

🧠 **Example:**

```js
let grade = "B";

switch (grade) {
  case "A": console.log("Excellent"); break;
  case "B": console.log("Good"); break;
  default: console.log("Try again");
}
```



### 🔹 **23. What are loops in JavaScript?**

Loops are used to **execute a block of code multiple times**, either a set number of times or while a condition is true.



### 🔹 **24. Explain for, while, and do...while loops**

#### ✅ `for` loop:

Used when the **number of iterations is known**.

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

#### ✅ `while` loop:

Used when the **condition is checked before each iteration**.

```js
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

#### ✅ `do...while` loop:

Executes the code **at least once**, even if the condition is false.

```js
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);
```



### 🔹 **25. What is the difference between for...in and for...of?**

| Loop       | Iterates over           | Use Case              |
| ---------- | ----------------------- | --------------------- |
| `for...in` | Keys / Indexes          | Objects               |
| `for...of` | Values (iterables only) | Arrays, strings, etc. |

🧠 **Example:**

```js
let arr = ["a", "b", "c"];

for (let index in arr) {
  console.log(index); // 0, 1, 2
}

for (let value of arr) {
  console.log(value); // "a", "b", "c"
}
```



### 🔹 **26. How do break and continue work?**

* **`break`**: Terminates the loop completely.
* **`continue`**: Skips the current iteration and goes to the next.

🧠 **Example:**

```js
for (let i = 0; i < 5; i++) {
  if (i === 2) continue;
  if (i === 4) break;
  console.log(i); // 0, 1, 3
}
```



### 🔹 **27. What is a label in JavaScript loops?**

A **label** gives a name to a loop and allows `break` or `continue` to affect outer loops.

🧠 **Example:**

```js
outer: for (let i = 0; i < 3; i++) {
  for (let j = 0; j < 3; j++) {
    if (i === 1 && j === 1) break outer;
    console.log(i, j);
  }
}
```



## ✅ **Functions and Closures**



### 🔹 **28. What is a function in JavaScript?**

A function is a **reusable block of code** that performs a task or returns a value.

🧠 **Example:**

```js
function greet(name) {
  return `Hello, ${name}`;
}
console.log(greet("Alice"));
```

 

### 🔹 **29. What are the types of functions in JavaScript?**

* Function Declarations
* Function Expressions
* Arrow Functions
* Anonymous Functions
* Constructor Functions
* IIFE (Immediately Invoked Function Expressions)

 

### 🔹 **30. What is an IIFE?**

**Immediately Invoked Function Expression** — runs immediately after it's defined.

🧠 **Syntax:**

```js
(function() {
  console.log("IIFE runs!");
})();
```

Used for:

* Creating a new scope
* Avoiding global pollution


### 🔹 **31. What is the difference between function declaration and expression?**

| Type     | Function Declaration | Function Expression |
| -------- | -------------------- | ------------------- |
| Hoisted? | Yes                  | No                  |
| Named?   | Required             | Optional            |

🧠 **Example:**

```js
// Declaration
function greet() {
  return "Hello";
}

// Expression
const greet = function() {
  return "Hi";
};
```


### 🔹 **32. What are arrow functions?**

A **concise way** to write functions using the `=>` syntax.

🧠 **Example:**

```js
const add = (a, b) => a + b;
console.log(add(2, 3)); // 5
```

**Arrow functions do not have their own `this`** — they inherit from the parent scope.



### 🔹 **33. What are first-class functions?**

Functions in JavaScript are **first-class citizens**, meaning:

* Can be **assigned to variables**
* Passed as **arguments**
* Returned from **other functions**

🧠 **Example:**

```js
const sayHello = () => "Hello";
const greet = (fn) => console.log(fn());
greet(sayHello);
```



### 🔹 **34. What is a callback function?**

A **function passed as an argument** to another function and called later.

🧠 **Example:**

```js
function fetchData(callback) {
  setTimeout(() => {
    callback("Data loaded");
  }, 1000);
}

fetchData((data) => console.log(data));
```



### 🔹 **35. What is a higher-order function?**

A function that **takes another function as an argument** or **returns another function**.

🧠 **Example:**

```js
function multiplyBy(factor) {
  return function (x) {
    return x * factor;
  };
}

const double = multiplyBy(2);
console.log(double(5)); // 10
```



### 🔹 **36. What is recursion?**

Recursion is a technique where a **function calls itself**.

🧠 **Example:**

```js
function factorial(n) {
  if (n === 0) return 1;
  return n * factorial(n - 1);
}
console.log(factorial(5)); // 120
```



### 🔹 **37. What is a closure in JavaScript?**

A **closure** is when a function **remembers its lexical scope**, even when executed outside its scope.

🧠 **Example:**

```js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    return count;
  };
}

const counter = outer();
console.log(counter()); // 1
console.log(counter()); // 2
```


### 🔹 **38. Explain the use cases of closures**

* **Data privacy / Encapsulation**
* **Creating private variables**
* **Partial application and currying**
* **Memoization / Caching**

🧠 **Use Case:**

```js
function createBankAccount(initialBalance) {
  let balance = initialBalance;
  return {
    deposit: (amount) => balance += amount,
    getBalance: () => balance
  };
}
```



### 🔹 **39. How to avoid memory leaks with closures?**

Closures can **hold references** to outer variables — preventing garbage collection if not handled properly.

✅ Best practices:

* Don’t create unnecessary closures
* Remove event listeners when no longer needed
* Avoid large variables inside closures
* Use tools like Chrome DevTools memory profiler

🧠 **Example of leak:**

```js
function attachEvent() {
  let largeData = new Array(100000).fill("leak");
  document.getElementById("btn").addEventListener("click", () => {
    console.log(largeData[0]);
  });
}
// Solution: remove listener when not needed
```




## ✅ **Objects and Arrays**


### 🔹 **40. What is an object in JavaScript?**

An **object** is a non-primitive data type that allows you to **store collections of key-value pairs**.

* Keys (also called properties) are always strings (or symbols).
* Values can be any type: string, number, array, object, function, etc.

🧠 **Example:**

```js
const person = {
  name: "Alice",
  age: 25,
  isStudent: false
};
```



### 🔹 **41. How do you create an object?**

✅ **Different ways:**

```js
// Object Literal
const car = { brand: "Toyota", model: "Corolla" };

// Using `new Object()`
const user = new Object();
user.name = "John";

// Using a constructor function
function Person(name, age) {
  this.name = name;
  this.age = age;
}
const p1 = new Person("Bob", 30);

// Using class (ES6)
class Animal {
  constructor(name) {
    this.name = name;
  }
}
const dog = new Animal("Buddy");
```


### 🔹 **42. What are object methods?**

Object methods are **functions stored as properties** inside an object.

🧠 **Example:**

```js
const person = {
  name: "Alice",
  greet: function() {
    return `Hi, I'm ${this.name}`;
  }
};

console.log(person.greet()); // Hi, I'm Alice
```



### 🔹 **43. What is `this` in JavaScript?**

`this` refers to the **context** in which a function is executed.

#### ✅ Depends on:

* Whether it's in **global**, **object**, **class**, or **event handler** context.
* Whether it's a **normal function** or **arrow function**.

🧠 **Example:**

```js
const obj = {
  name: "Bob",
  sayName: function() {
    console.log(this.name); // refers to obj
  }
};
obj.sayName();
```



### 🔹 **44. How is `this` handled in arrow functions?**

Arrow functions **do not have their own `this`**. They **inherit it from their lexical scope** (parent function or object).

🧠 **Example:**

```js
const person = {
  name: "Sam",
  greet: () => {
    console.log(this.name); // undefined (this is from global scope)
  }
};
person.greet();
```



### 🔹 **45. What is object destructuring?**

Destructuring is a **syntax to extract properties** from objects into variables.

🧠 **Example:**

```js
const person = { name: "Alice", age: 25 };
const { name, age } = person;
console.log(name); // Alice
```

### 🔹 **46. What is array destructuring?**

Similar to object destructuring but works on arrays by **position**.

🧠 **Example:**

```js
const colors = ["red", "green", "blue"];
const [first, second] = colors;
console.log(first); // red
```


### 🔹 **47. How do you iterate over objects?**

✅ Ways to iterate:

```js
const user = { name: "Tom", age: 30 };

// Using for...in
for (let key in user) {
  console.log(key, user[key]);
}

// Using Object methods
Object.keys(user).forEach(key => {
  console.log(`${key}: ${user[key]}`);
});

Object.entries(user).forEach(([key, value]) => {
  console.log(`${key} => ${value}`);
});
```



### 🔹 **48. What are arrays in JavaScript?**

Arrays are **ordered collections of values**, where each value has an index (starting from 0).

```js
const fruits = ["apple", "banana", "cherry"];
```

* Can hold **mixed data types**
* Are zero-indexed



### 🔹 **49. How to loop through an array?**

✅ Methods to iterate:

```js
const numbers = [1, 2, 3];

// for loop
for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}

// for...of
for (let num of numbers) {
  console.log(num);
}

// forEach
numbers.forEach(n => console.log(n));
```



### 🔹 **50. What are common array methods?**

| Method       | Description                          | Example                             |
| ------------ | ------------------------------------ | ----------------------------------- |
| `map()`      | Transforms each item                 | `[1, 2].map(x => x * 2)` → `[2, 4]` |
| `filter()`   | Filters items based on condition     | `[1, 2, 3].filter(x => x > 1)`      |
| `reduce()`   | Reduces array to a single value      | `[1,2,3].reduce((a,b)=>a+b)` → `6`  |
| `forEach()`  | Executes a function for each element | `arr.forEach(x => console.log(x))`  |
| `find()`     | Finds the first match                | `[4, 5, 6].find(x => x > 5)` → `6`  |
| `includes()` | Checks if value exists               | `[1, 2].includes(2)` → `true`       |
| `indexOf()`  | Gets the index of an element         | `['a','b'].indexOf('b')` → `1`      |
| `sort()`     | Sorts array                          | `[3, 1, 2].sort()` → `[1,2,3]`      |
| `concat()`   | Combines arrays                      | `[1].concat([2,3])` → `[1,2,3]`     |
| `join()`     | Converts array to string             | `[1,2].join(',')` → `"1,2"`         |



### 🔹 **51. Difference between `slice()` and `splice()`**

| Feature    | `slice()`             | `splice()`                        |
| ---------- | --------------------- | --------------------------------- |
| Mutates?   | ❌ No                  | ✅ Yes                             |
| Returns    | A shallow copy        | Deleted elements                  |
| Parameters | `slice(start, end)`   | `splice(start, deleteCount, ...)` |
| Use Case   | Extract part of array | Add/remove items in-place         |

🧠 **Example:**

```js
const arr = [1, 2, 3, 4];
arr.slice(1, 3); // [2, 3]
arr.splice(1, 2); // [2, 3] and arr becomes [1, 4]
```



### 🔹 **52. What is the spread operator (`...`)**

It allows **expansion** of arrays/objects.

#### ✅ Uses:

* Cloning
* Combining
* Passing array as arguments

🧠 **Example:**

```js
const nums = [1, 2, 3];
const copy = [...nums]; // [1, 2, 3]

const obj = { a: 1, b: 2 };
const newObj = { ...obj, c: 3 }; // { a:1, b:2, c:3 }
```



### 🔹 **53. What is the rest operator (`...`)**

It allows **collecting** multiple elements into an array or object.

🧠 **Example in function parameters:**

```js
function sum(...args) {
  return args.reduce((acc, val) => acc + val, 0);
}
console.log(sum(1, 2, 3)); // 6
```

🧠 **Example in destructuring:**

```js
const [first, ...rest] = [10, 20, 30, 40];
console.log(rest); // [20, 30, 40]
```


