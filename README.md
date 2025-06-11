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



## ✅ Asynchronous JavaScript



### 🔹 **54. What is synchronous vs asynchronous code?**

| Synchronous              | Asynchronous                          |
| ------------------------ | ------------------------------------- |
| Executes line-by-line    | Can skip waiting tasks and move ahead |
| Blocks further execution | Non-blocking; uses callbacks/promises |
| Easier to read/debug     | More powerful for web tasks           |

🧠 **Example (Synchronous):**

```js
console.log("Start");
console.log("Middle");
console.log("End");

// Output:
// Start
// Middle
// End
```

🧠 **Example (Asynchronous):**

```js
console.log("Start");

setTimeout(() => {
  console.log("Inside setTimeout");
}, 1000);

console.log("End");

// Output:
// Start
// End
// Inside setTimeout
```

> 💡 Asynchronous code allows JavaScript to continue running without waiting for long-running operations like API calls, timers, etc.



### 🔹 **55. What is the event loop?**

The **event loop** is the mechanism that allows JavaScript to handle **asynchronous operations** by managing the **call stack** and **callback queue**.

#### ✅ Flow:

1. Executes code in the **call stack**.
2. When an async operation (like `setTimeout`, `fetch`) is done, its callback goes to the **callback queue**.
3. **Event loop** checks if the stack is empty and moves the callback into the stack.

🧠 **Visual Diagram:**

```
[Call Stack]  <- main thread executes code
[Web APIs]    <- handles setTimeout, fetch, etc.
[Callback Queue] <- stores completed async tasks
[Event Loop]  <- Moves tasks to Call Stack when it's free
```



### 🔹 **56. What is the call stack?**

The **call stack** is a data structure that tracks function calls in JavaScript.

```js
function greet() {
  console.log("Hello");
}
greet();
```

* `greet()` is pushed onto the stack.
* After execution, it’s popped off the stack.

> Stack = LIFO (Last In, First Out)



### 🔹 **57. What is a callback?**

A **callback** is a function passed as an argument to another function and called later.

🧠 **Example:**

```js
function greet(name, callback) {
  console.log("Hi " + name);
  callback();
}

function sayBye() {
  console.log("Bye!");
}

greet("Alice", sayBye);
```



### 🔹 **58. What is a promise?**

A **Promise** is an object that represents the eventual result (or failure) of an **asynchronous operation**.

🧠 **Syntax:**

```js
const promise = new Promise((resolve, reject) => {
  // async task
  const success = true;
  if (success) {
    resolve("Task done!");
  } else {
    reject("Error occurred");
  }
});

promise
  .then(result => console.log(result))
  .catch(error => console.log(error));
```



### 🔹 **59. What are the states of a promise?**

1. **Pending** – Initial state, not yet fulfilled or rejected.
2. **Fulfilled** – Operation completed successfully (`resolve()`).
3. **Rejected** – Operation failed (`reject()`).


### 🔹 **60. What is async and await?**

* `async` makes a function return a **Promise**.
* `await` pauses execution until a promise is resolved.

🧠 **Example:**

```js
async function fetchData() {
  try {
    let response = await fetch("https://api.example.com/data");
    let data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error:", error);
  }
}
```



### 🔹 **61. What is the difference between `setTimeout()` and `setInterval()`?**

| `setTimeout()`            | `setInterval()`                     |
| ------------------------- | ----------------------------------- |
| Executes once after delay | Executes repeatedly after intervals |
| Can simulate delay        | Can create periodic tasks           |

🧠 **Example:**

```js
setTimeout(() => console.log("Runs once"), 2000);
setInterval(() => console.log("Runs every 2 sec"), 2000);
```



### 🔹 **62. What is `clearTimeout()` and `clearInterval()`?**

These are used to **cancel timers** set by `setTimeout()` or `setInterval()`.

🧠 **Example:**

```js
const id = setTimeout(() => {
  console.log("This will not run");
}, 3000);

clearTimeout(id); // cancels the timeout

const intervalId = setInterval(() => console.log("Looping"), 1000);
clearInterval(intervalId); // cancels the interval
```



### 🔹 **63. How to handle errors in promises?**

✅ Use `.catch()` or `try...catch` with async/await.

🧠 **Example with `.catch()`:**

```js
fetch("https://wrong-url.com")
  .then(response => response.json())
  .catch(error => console.error("Caught:", error));
```

🧠 **With async/await:**

```js
async function getData() {
  try {
    const res = await fetch("https://wrong-url.com");
    const data = await res.json();
  } catch (err) {
    console.error("Error:", err);
  }
}
```



### 🔹 **64. What is a race condition?**

A **race condition** occurs when multiple async operations run in parallel and the outcome depends on which completes first — often resulting in **unpredictable behavior**.

🧠 **Example:**

```js
let data;
fetch("api1.com").then(res => data = res);
fetch("api2.com").then(res => data = res); // overwrites data
```

> ❗Use `Promise.race()` or design logic to handle priorities.



### 🔹 **65. What is `Promise.all()` and `Promise.race()`?**

| Feature       | `Promise.all()`          | `Promise.race()`                              |
| ------------- | ------------------------ | --------------------------------------------- |
| Resolves when | **All promises resolve** | **First promise (resolve or reject)** settles |
| Rejects if    | **Any one rejects**      | First one to settle decides the result        |

🧠 **Example:**

```js
const p1 = Promise.resolve("A");
const p2 = Promise.resolve("B");

// Promise.all
Promise.all([p1, p2])
  .then(values => console.log(values)); // ['A', 'B']

// Promise.race
Promise.race([p1, p2])
  .then(value => console.log(value)); // 'A' or 'B', whichever is faster
```




## ✅ DOM (Document Object Model) Manipulation



### 🔹 **66. What is the DOM?**

**DOM (Document Object Model)** is a programming interface for HTML and XML documents. It represents the **structure of a webpage as a tree of objects**, where each element (like `<div>`, `<p>`, etc.) becomes a node.

🧠 **Example structure:**

```html
<html>
  <body>
    <h1>Hello</h1>
    <button>Click Me</button>
  </body>
</html>
```

🧩 In the DOM, this becomes a **tree**:

```
Document
 └── html
      ├── body
           ├── h1
           └── button
```

* You can **access, change, add, or remove** elements using JavaScript.



### 🔹 **67. How to select elements in the DOM?**

You can use various methods to **select DOM elements**.

🧠 **Examples:**

```js
// Select by ID
const title = document.getElementById("main-title");

// Select by class
const items = document.getElementsByClassName("item");

// Select by tag name
const paragraphs = document.getElementsByTagName("p");

// Select using CSS selectors
const firstItem = document.querySelector(".item");
const allItems = document.querySelectorAll(".item");
```



### 🔹 **68. What are DOM methods?**

DOM methods are functions provided by the browser to interact with the page.

🧠 **Common Methods:**

| Method                     | Description                                        |
| -------------------------- | -------------------------------------------------- |
| `getElementById()`         | Selects one element by ID                          |
| `getElementsByClassName()` | Selects all elements with a class (HTMLCollection) |
| `querySelector()`          | Selects **first** element matching a CSS selector  |
| `querySelectorAll()`       | Selects **all** elements (NodeList)                |
| `createElement()`          | Creates a new HTML element                         |
| `appendChild()`            | Adds element as a child                            |
| `removeChild()`            | Removes a child element                            |
| `setAttribute()`           | Sets an attribute                                  |
| `classList.add()`          | Adds a class                                       |



### 🔹 **69. Difference between getElementById, querySelector, and querySelectorAll**

| Feature       | `getElementById` | `querySelector`        | `querySelectorAll`    |
| ------------- | ---------------- | ---------------------- | --------------------- |
| Return type   | Element (single) | First matching element | NodeList (array-like) |
| Selector type | ID only          | CSS selector           | CSS selector          |
| Usage         | Simpler, faster  | Flexible               | For multiple elements |

🧠 **Example:**

```html
<div id="box" class="container box"></div>
```

```js
document.getElementById("box");           // ✅ ID only
document.querySelector(".box");           // ✅ First element with class 'box'
document.querySelectorAll(".box");        // ✅ All elements with class 'box'
```



### 🔹 **70. What is event bubbling and capturing?**

These define the **order of event propagation** in the DOM.

🧩 **Event Bubbling** (Default):

* The event starts at the **target element** and bubbles **up** to the root.

🧩 **Event Capturing**:

* The event is captured from the **root** down to the **target**.

🧠 **Example:**

```html
<div id="outer">
  <button id="inner">Click Me</button>
</div>
```

```js
document.getElementById("outer").addEventListener("click", () => {
  console.log("Outer clicked");
});

document.getElementById("inner").addEventListener("click", () => {
  console.log("Inner clicked");
});
```

👉 Output:

```
Inner clicked
Outer clicked
```

(⬆️ bubbling happens by default)



### 🔹 **71. What is `addEventListener()`?**

It attaches an **event handler** to an element without overwriting existing ones.

🧠 **Syntax:**

```js
element.addEventListener("event", callback, useCapture);
```

🧠 **Example:**

```js
const btn = document.querySelector("button");
btn.addEventListener("click", () => {
  alert("Button clicked!");
});
```

> ✅ Can attach multiple listeners of the same type.


### 🔹 **72. What is event delegation?**

Event delegation is a technique where you **attach a single event listener to a parent element** to handle events for multiple children.

✅ Efficient for **dynamic elements**.

🧠 **Example:**

```html
<ul id="list">
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

```js
document.getElementById("list").addEventListener("click", function(e) {
  if (e.target.tagName === "LI") {
    console.log("You clicked: " + e.target.textContent);
  }
});
```


### 🔹 **73. What are DOM events?**

DOM events are **signals** that something has happened in the document.

🧠 **Common DOM events:**

| Event Type   | Trigger                           |
| ------------ | --------------------------------- |
| `click`      | User clicks on an element         |
| `submit`     | Form is submitted                 |
| `change`     | Form element value is changed     |
| `keydown`    | Key is pressed down               |
| `keyup`      | Key is released                   |
| `mouseenter` | Cursor enters element             |
| `mouseleave` | Cursor leaves element             |
| `load`       | Page or resource finishes loading |
| `scroll`     | User scrolls the document         |



### 🔹 **74. How to prevent default behavior?**

Use `event.preventDefault()` to prevent the browser’s default action.

🧠 **Example:**

```html
<a href="https://google.com" id="link">Go</a>
```

```js
document.getElementById("link").addEventListener("click", function(e) {
  e.preventDefault(); // stops navigation
  alert("Link clicked but not navigated!");
});
```



### 🔹 **75. How to stop event propagation?**

Use `event.stopPropagation()` to **stop bubbling** or **capturing**.

🧠 **Example:**

```js
document.getElementById("outer").addEventListener("click", () => {
  console.log("Outer clicked");
});

document.getElementById("inner").addEventListener("click", (e) => {
  e.stopPropagation(); // prevent bubbling
  console.log("Inner clicked");
});
```

👉 Output:

```
Inner clicked
```



## ✅ ERROR HANDLING & DEBUGGING


### 🔹 76. **What is error handling in JavaScript?**

**Error handling** is the process of catching and responding to **runtime errors** so that your application doesn’t crash and can handle exceptions gracefully.

🧠 **Goal:** Improve robustness and user experience.

### 🔹 77. **What is try...catch...finally?**

Used to catch and handle exceptions.

🧠 **Syntax:**

```js
try {
  // Code that may throw an error
} catch (error) {
  // Handle the error
} finally {
  // Always executes, even if there's an error
}
```

🧠 **Example:**

```js
try {
  let x = y + 1; // y is not defined
} catch (err) {
  console.log("Caught an error:", err.message);
} finally {
  console.log("This runs no matter what");
}
```

> ✅ `finally` is often used to **clean up resources**, like closing files or ending DB connections.



### 🔹 78. **What is `throw`?**

You can use `throw` to **manually create custom errors**.

🧠 **Example:**

```js
function divide(a, b) {
  if (b === 0) {
    throw new Error("Cannot divide by zero");
  }
  return a / b;
}

try {
  divide(5, 0);
} catch (e) {
  console.log(e.message);
}
```



### 🔹 79. **Difference between `TypeError`, `ReferenceError`, and `SyntaxError`**

| Error Type       | When it occurs                          | Example                                |
| ---------------- | --------------------------------------- | -------------------------------------- |
| `TypeError`      | Using a value in an invalid way         | `"abc".toFixed(2)`                     |
| `ReferenceError` | Refers to a variable that doesn't exist | `console.log(x)` when `x` is undefined |
| `SyntaxError`    | Invalid code syntax                     | `if (a === ) {`                        |



### 🔹 80. **How do you debug JavaScript code?**

🧰 Common Debugging Techniques:

* **`console.log()`**
* **Browser DevTools** (Elements, Console, Network, Sources tab)
* **Breakpoints**
* **Debugger keyword**
* **Linting tools** (ESLint)
* **Using `try...catch`**

🧠 **Tip:** Add logs at multiple points to understand data flow.



### 🔹 81. **What are breakpoints in browser DevTools?**

A **breakpoint** is a marker you set in the **DevTools “Sources” tab** to **pause code execution** at a specific line.

🧠 **How to use:**

1. Open Chrome DevTools → “Sources” tab.
2. Click the line number in your JS file to add a breakpoint.
3. Interact with the page.
4. Execution will pause at the breakpoint, allowing inspection.

🎯 Helpful for:

* Inspecting variable values.
* Stepping through code line-by-line.
* Watching call stack changes.



## ✅ JAVASCRIPT IN THE BROWSER



### 🔹 82. **What is the `window` object?**

The **`window`** object is the **global object** in the browser.

🧠 It represents the **browser window/tab** and provides methods and properties like:

```js
console.log(window.innerHeight);   // Height of the window
window.alert("Hi!");              // Alert popup
```

> All global variables/functions are properties of `window`:

```js
var a = 10;
console.log(window.a); // 10
```



### 🔹 83. **What is the `document` object?**

The `document` object represents the **webpage loaded** in the browser (DOM). It’s part of the `window` object:

```js
console.log(window.document === document); // true
```

🧠 **Common usages:**

```js
document.getElementById("id");
document.querySelector(".class");
document.title = "New Page Title";
```



### 🔹 84. **What are cookies?**

Cookies are **small key-value pairs** stored in the browser to **maintain session state**.

🧠 **Use Cases:**

* Login sessions
* Tracking user activity
* Storing preferences

🧠 **Example:**

```js
document.cookie = "username=John; expires=Fri, 31 Dec 2025 23:59:59 GMT";
console.log(document.cookie); // "username=John"
```

> ❗ Cookies are **automatically sent to the server** with HTTP requests.



### 🔹 85. **What is localStorage vs sessionStorage?**

| Feature    | `localStorage`                     | `sessionStorage`         |
| ---------- | ---------------------------------- | ------------------------ |
| Lifetime   | Until manually cleared             | Until tab is closed      |
| Scope      | Shared across tabs                 | Only for the current tab |
| Size Limit | \~5MB                              | \~5MB                    |
| API        | `setItem`, `getItem`, `removeItem` | Same                     |

🧠 **Example:**

```js
// localStorage
localStorage.setItem("theme", "dark");
console.log(localStorage.getItem("theme")); // "dark"

// sessionStorage
sessionStorage.setItem("user", "John");
```



### 🔹 86. **How do you manipulate the DOM with JavaScript?**

✅ You can **create**, **select**, **update**, or **delete** elements dynamically.

🧠 **Example:**

```js
const heading = document.createElement("h1");
heading.textContent = "Welcome!";
document.body.appendChild(heading);

// Change existing
document.querySelector("p").style.color = "blue";
```



### 🔹 87. **What are `alert`, `confirm`, and `prompt`?**

These are **modal dialogs** provided by the `window` object.

| Method      | Description                                 |
| ----------- | ------------------------------------------- |
| `alert()`   | Displays a simple popup with a message      |
| `confirm()` | Shows Yes/No popup and returns true/false   |
| `prompt()`  | Takes user input and returns it as a string |

🧠 **Example:**

```js
alert("Hello!");

const agree = confirm("Do you agree?");
if (agree) console.log("User agreed");

const name = prompt("What is your name?");
console.log("Hi", name);
```

> ❗ These methods are **blocking** and **pause JavaScript execution** until user action.




# ✅ Advanced JavaScript Concepts



### 🔹 88. **What is strict mode?**

**`"use strict"`** is a **pragma** that tells JavaScript to run in a **strict variant** of JavaScript.

🧠 **Benefits:**

* Prevents use of undeclared variables.
* Throws errors for silent bugs.
* Prevents use of reserved words.

🧠 **Example:**

```js
"use strict";

x = 5; // ❌ ReferenceError: x is not defined
```

✅ Use it at the **top of a script or function**:

```js
function demo() {
  "use strict";
  // strict mode active here
}
```



### 🔹 89. **What is the prototype chain?**

JavaScript uses **prototype-based inheritance**. Every object has an internal property `[[Prototype]]` (accessible via `__proto__`) pointing to another object.

🔗 This forms a **chain** — the **Prototype Chain** — ending with `null`.

🧠 **Example:**

```js
let arr = [1, 2, 3];
console.log(arr.__proto__ === Array.prototype); // true
console.log(arr.__proto__.__proto__ === Object.prototype); // true
```

So: `arr → Array.prototype → Object.prototype → null`



### 🔹 90. **What is prototypal inheritance?**

Objects in JavaScript can **inherit properties and methods** from other objects via the prototype chain.

🧠 **Example:**

```js
const animal = {
  speak() {
    return "I can speak";
  }
};

const dog = Object.create(animal);
dog.bark = () => "Woof";

console.log(dog.speak()); // Inherited
console.log(dog.bark());  // Own method
```



### 🔹 91. **Difference between `.call()`, `.apply()`, and `.bind()`**

| Method    | Invokes immediately? | Pass args          | Binds `this` |
| --------- | -------------------- | ------------------ | ------------ |
| `call()`  | ✅ Yes                | As comma-separated | ✅ Yes        |
| `apply()` | ✅ Yes                | As array           | ✅ Yes        |
| `bind()`  | ❌ No (returns func)  | As comma-separated | ✅ Yes        |

🧠 **Example:**

```js
function greet(greeting) {
  return `${greeting}, ${this.name}`;
}

const user = { name: "Vikash" };

console.log(greet.call(user, "Hello"));         // "Hello, Vikash"
console.log(greet.apply(user, ["Hi"]));         // "Hi, Vikash"

const greetUser = greet.bind(user);
console.log(greetUser("Welcome"));              // "Welcome, Vikash"
```



### 🔹 92. **Difference between deep and shallow copy**

| Copy Type    | What it copies               | Shared nested objects? |
| ------------ | ---------------------------- | ---------------------- |
| Shallow Copy | Top-level only               | ✅ Yes                  |
| Deep Copy    | Entire structure recursively | ❌ No (fully cloned)    |

🧠 **Example of Shallow Copy:**

```js
const original = { name: "Vikash", skills: ["JS", "React"] };
const shallow = { ...original };

shallow.skills.push("Node");
console.log(original.skills); // Modified too ❗
```

🧠 **Example of Deep Copy:**

```js
const deep = JSON.parse(JSON.stringify(original));
deep.skills.push("MongoDB");
console.log(original.skills); // ✅ Unchanged
```



### 🔹 93. **How to clone an object?**

✅ **Shallow Clone:**

```js
const clone1 = Object.assign({}, obj);
const clone2 = { ...obj };
```

✅ **Deep Clone:**

```js
const deepClone = JSON.parse(JSON.stringify(obj)); // Simple but has limitations
// Or use lodash:
import _ from 'lodash';
const deepClone = _.cloneDeep(obj);
```



### 🔹 94. **What is the `new` keyword?**

Used to create **instances of objects** from constructor functions or classes.

🧠 **Steps when `new` is used:**

1. Creates a new empty object.
2. Sets the `this` of the constructor to point to the new object.
3. Inherits from the constructor's prototype.
4. Returns the object.

🧠 **Example:**

```js
function User(name) {
  this.name = name;
}
const u = new User("Vikash");
```



### 🔹 95. **What are constructors?**

**Constructor functions** are templates for creating objects.

🧠 **Example:**

```js
function Car(make, model) {
  this.make = make;
  this.model = model;
}

const car1 = new Car("Toyota", "Camry");
```

🧠 Constructors + `new` = instance



### 🔹 96. **What is object-oriented programming (OOP) in JavaScript?**

OOP is a programming paradigm where you structure code around **objects** (data + methods).

JavaScript supports OOP through:

* Prototypes
* Constructor functions
* ES6 Classes

🧠 **Pillars of OOP:**

1. **Encapsulation** – data hiding via closures or private fields
2. **Inheritance** – reuse via prototypes or `extends`
3. **Polymorphism** – same method, different behaviors
4. **Abstraction** – simplify interfaces


### 🔹 97. **What are classes?**

**ES6 classes** are syntactic sugar over prototypal inheritance.

🧠 **Example:**

```js
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    return `${this.name} makes a sound`;
  }
}

const dog = new Animal("Dog");
console.log(dog.speak());
```



### 🔹 98. **What are getters and setters?**

They are **special methods** that define accessors for properties.

🧠 **Example:**

```js
class Person {
  constructor(name) {
    this._name = name;
  }

  get name() {
    return this._name.toUpperCase();
  }

  set name(value) {
    this._name = value.trim();
  }
}

const p = new Person("vikash");
console.log(p.name);      // VIKASH
p.name = "  Kumar ";
console.log(p.name);      // KUMAR
```



### 🔹 99. **What are static methods?**

Static methods belong to the **class itself**, not instances.

🧠 **Example:**

```js
class MathUtil {
  static square(x) {
    return x * x;
  }
}

console.log(MathUtil.square(5));  // 25
```

You cannot call `MathUtil.square()` from an instance — only from the class.



# ✅ ES6+ Features



### 🔹 100. **What’s new in ES6?**

**ES6 (ECMAScript 2015)** introduced major syntax improvements and features:

✅ Highlights:

* `let`, `const`
* Arrow functions
* Template literals
* Destructuring
* Default parameters
* Classes
* Modules (`import`/`export`)
* Promises
* Symbols
* Generators
* `Map`, `Set`, `WeakMap`, `WeakSet`
* Spread & Rest operators



### 🔹 101. **What are arrow functions?**

Arrow functions are a **shorter syntax** for writing functions and **do not have their own `this`**.

🧠 **Syntax:**

```js
const add = (a, b) => a + b;
```

✅ Useful for:

* One-liners
* Callbacks
* Preserving outer `this`

🧠 **Example:**

```js
const user = {
  name: "Vikash",
  greet: function () {
    setTimeout(() => {
      console.log("Hi " + this.name); // 'this' is preserved
    }, 1000);
  }
};
user.greet();
```



### 🔹 102. **What are default parameters?**

You can assign **default values to function parameters**.

🧠 **Example:**

```js
function greet(name = "Guest") {
  return `Hello, ${name}`;
}

console.log(greet());         // Hello, Guest
console.log(greet("Vikash")); // Hello, Vikash
```



### 🔹 103. **What is destructuring?**

Destructuring allows you to **extract values** from arrays or objects into variables.

🧠 **Object Destructuring:**

```js
const user = { name: "Vikash", age: 25 };
const { name, age } = user;
```

🧠 **Array Destructuring:**

```js
const [a, b] = [10, 20];  // a=10, b=20
```


### 🔹 104. **What is the spread operator (`...`)?**

The **spread operator** is used to **expand** arrays or objects.

🧠 **Example:**

```js
const arr = [1, 2, 3];
const copy = [...arr];         // [1, 2, 3]

const obj = { a: 1 };
const newObj = { ...obj, b: 2 };  // {a: 1, b: 2}
```


### 🔹 105. **What is the rest parameter (`...`)?**

The **rest operator** collects **all remaining elements** into an array.

🧠 **Example:**

```js
function sum(...numbers) {
  return numbers.reduce((acc, val) => acc + val, 0);
}
console.log(sum(1, 2, 3)); // 6
```


### 🔹 106. **What are template literals?**

Template literals are **string literals** that allow:

* Interpolation (`${}`)
* Multiline strings

🧠 **Syntax:**

```js
const name = "Vikash";
const msg = `Hello, ${name}!
Welcome to ES6.`;
```



### 🔹 107. **What are classes in JavaScript?**

Introduced in ES6, classes are a **syntactical sugar** over prototype-based inheritance.

🧠 **Example:**

```js
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    return `Hi, I'm ${this.name}`;
  }
}
```

> Use `extends` and `super()` for inheritance.



### 🔹 108. **What are modules?**

JavaScript ES6 supports **modules** to break code into reusable pieces using `export` and `import`.

🧠 **Syntax:**

```js
// math.js
export function add(a, b) { return a + b; }

// app.js
import { add } from './math.js';
console.log(add(2, 3)); // 5
```



### 🔹 109. **What are `let` and `const`?**

| Keyword | Reassignment | Scope       | Hoisted | Temporal Dead Zone |
| ------- | ------------ | ----------- | ------- | ------------------ |
| `let`   | ✅ Yes        | Block Scope | ❌ No    | ✅ Yes              |
| `const` | ❌ No         | Block Scope | ❌ No    | ✅ Yes              |

```js
let a = 10;
const b = 20;
```

> `var` is function-scoped and hoisted. Prefer `let` and `const` in modern JS.



### 🔹 110. **What are Promises?**

A **Promise** is an object representing the **eventual completion (or failure)** of an asynchronous operation.

🧠 **States:**

* `pending`
* `fulfilled`
* `rejected`

🧠 **Example:**

```js
const promise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Done!"), 1000);
});

promise.then(console.log).catch(console.error);
```



### 🔹 111. **What is Symbol?**

A **Symbol** is a **unique, immutable primitive value** used as an object key.

🧠 **Example:**

```js
const sym = Symbol("id");
const obj = {
  [sym]: 123
};
console.log(obj[sym]); // 123
```

> Symbols help avoid property name collisions.


### 🔹 112. **What are generators?**

A **generator function** can pause execution and resume later using `yield`.

🧠 **Syntax:**

```js
function* count() {
  yield 1;
  yield 2;
  yield 3;
}

const gen = count();
console.log(gen.next()); // {value: 1, done: false}
```

Use Case: Custom iterators, async workflows, infinite sequences.



### 🔹 113. **What is `Map` and `Set`?**

#### ✅ Map:

* Key-value pairs
* Keys can be any type (including objects)

```js
const map = new Map();
map.set("name", "Vikash");
console.log(map.get("name")); // Vikash
```

#### ✅ Set:

* Stores unique values

```js
const set = new Set([1, 2, 2, 3]);
console.log(set); // Set(3) {1, 2, 3}
```


### 🔹 114. **What is `WeakMap` and `WeakSet`?**

✅ They store **weak references** to objects, meaning they don’t prevent garbage collection.

#### WeakMap:

* Keys must be **objects**
* Not iterable

```js
let obj = {};
let wm = new WeakMap();
wm.set(obj, "data");
```

#### WeakSet:

* Values must be **objects**
* Not iterable

```js
let ws = new WeakSet();
ws.add({});
```

> ⚠️ Useful for **private data storage** in classes.



## ✅ Memory & Performance



### 🔹 115. **What causes memory leaks?**

A **memory leak** occurs when memory is **no longer needed** but **not released**, causing the app to consume more memory over time.

#### Common causes:

1. **Global variables**

   ```js
   myVar = []; // no `let`, `const` – becomes global unintentionally
   ```

2. **Uncleared timers or intervals**

   ```js
   setInterval(() => {
     console.log("Running...");
   }, 1000); // Never cleared
   ```

3. **Event listeners not removed**

   ```js
   element.addEventListener('click', handler); // Not removed with removeEventListener
   ```

4. **Closures holding references**

   ```js
   function outer() {
     let bigData = new Array(10000).fill("memory");
     return function inner() {
       console.log(bigData[0]);
     };
   }
   ```

5. **Detached DOM elements**

   * When you remove a DOM element visually, but JavaScript still holds a reference to it.



### 🔹 116. **How do you prevent memory leaks?**

✅ Best practices:

* Use `let`/`const` to avoid global vars.
* Use `removeEventListener`.
* Clear intervals and timeouts:

  ```js
  const id = setInterval(() => {}, 1000);
  clearInterval(id);
  ```
* Nullify unused object references.
* Use **weak collections** like `WeakMap`, `WeakSet` for temporary object storage.
* Avoid excessive closure usage with large data.



### 🔹 117. **What is garbage collection?**

**Garbage Collection (GC)** is the process by which the JS engine **automatically frees up memory** used by unreferenced variables or objects.

✅ JS uses **Mark-and-Sweep**:

* It "marks" objects that are still reachable and **removes the rest** from memory.

🧠 Example:

```js
let user = { name: "Vikash" };
user = null; // The object becomes unreachable -> garbage collected
```



### 🔹 118. **How to optimize JavaScript performance?**

✅ Performance optimization techniques:

1. **Minimize DOM manipulation**

   * Use DocumentFragment or batch updates.

2. **Debounce & throttle expensive operations**

   ```js
   const debounce = (fn, delay) => {
     let timeout;
     return (...args) => {
       clearTimeout(timeout);
       timeout = setTimeout(() => fn(...args), delay);
     };
   };
   ```

3. **Use async/await instead of nested callbacks**

4. **Avoid memory leaks**

5. **Use web workers for heavy processing**

6. **Lazy loading for resources**

7. **Efficient data structures (Map, Set)**

8. **Minimize reflows and repaints in the DOM**

9. **Compress and bundle JS files**


## ✅ Web APIs and Fetch



### 🔹 119. **What is the Fetch API?**

The **Fetch API** is a modern **promise-based** way to make HTTP requests in JavaScript.

✅ Replaces `XMLHttpRequest`.



### 🔹 120. **How does `fetch()` work?**

`fetch(url, options)` returns a **Promise** that resolves to a **Response object**.

🧠 Example:

```js
fetch('https://api.example.com/data')
  .then(response => {
    if (!response.ok) throw new Error('Error');
    return response.json();
  })
  .then(data => console.log(data))
  .catch(err => console.error(err));
```

✅ Supports:

* GET, POST, PUT, DELETE
* Headers
* Body (string, JSON, FormData)
* CORS



### 🔹 121. **Difference between Fetch and XMLHttpRequest**

| Feature           | Fetch API           | XMLHttpRequest        |
| ----------------- | ------------------- | --------------------- |
| Modern            | ✅ Yes               | ❌ No                  |
| Promise-based     | ✅ Yes               | ❌ No (uses callbacks) |
| Chaining          | ✅ Elegant `.then()` | ❌ Complex logic       |
| Streaming support | ✅ Yes               | ❌ No                  |
| Simpler API       | ✅ Yes               | ❌ No                  |



### 🔹 122. **What is CORS (Cross-Origin Resource Sharing)?**

**CORS** is a security feature that restricts **cross-origin HTTP requests** unless the target server explicitly allows it.

🧠 Browser blocks requests from `origin A` to `origin B` **unless B’s server** adds:

```http
Access-Control-Allow-Origin: https://originA.com
```

✅ Solved via:

* Server-side headers
* Proxy servers
* CORS middleware in Node.js (e.g., `cors` package)



### 🔹 123. **What is JSONP?**

**JSONP (JSON with Padding)** is an old workaround for CORS using `<script>` tag.

🧠 Example:

```html
<script src="https://example.com/api?callback=myFunction"></script>
```

```js
function myFunction(data) {
  console.log(data);
}
```

⚠️ Security risk. Not used today. Use `CORS` or `proxy` instead.



### 🔹 124. **How to parse JSON in JavaScript?**

✅ Convert JSON string to JavaScript object:

```js
const jsonStr = '{"name":"Vikash"}';
const obj = JSON.parse(jsonStr);
```

✅ Convert object to JSON string:

```js
const str = JSON.stringify({ name: "Vikash" });
```



### 🔹 125. **What are API calls?**

**API calls** are requests made from client-side JS to a server to **fetch or send data**.

🧠 Example (GET request):

```js
fetch("https://api.example.com/products")
  .then(res => res.json())
  .then(data => console.log(data));
```

🧠 Example (POST request):

```js
fetch("https://api.example.com/products", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ name: "New Product" }),
})
.then(res => res.json())
.then(data => console.log(data));
```

✅ APIs often return data in **JSON** format.




## ✅ JavaScript Design Patterns



### 🔹 126. **What is a Design Pattern?**

A **design pattern** is a reusable, best-practice solution to a **common problem** in software design. These patterns are templates you can apply to write more **modular, scalable, and maintainable** code.

🔧 Categories:

* **Creational** – Object creation (e.g., Singleton, Factory)
* **Structural** – Composition of classes/objects (e.g., Decorator, Adapter)
* **Behavioral** – Communication between objects (e.g., Observer, Mediator)



### 🔹 127. **What is the Module Pattern?**

The **Module Pattern** allows you to **encapsulate logic** and expose only public methods/variables using **closures**.

📦 Example:

```js
const CounterModule = (function () {
  let count = 0; // private

  function increment() {
    count++;
    console.log(count);
  }

  function reset() {
    count = 0;
  }

  return {
    increment,
    reset
  };
})();

CounterModule.increment(); // 1
CounterModule.increment(); // 2
CounterModule.reset();
```

✅ Use case: Code organization, encapsulation, reusable modules.



### 🔹 128. **What is the Singleton Pattern?**

The **Singleton Pattern** ensures a class has **only one instance** and provides a global point of access to it.

👤 Example:

```js
const Singleton = (function () {
  let instance;

  function createInstance() {
    return { name: "I am the only instance" };
  }

  return {
    getInstance: function () {
      if (!instance) instance = createInstance();
      return instance;
    }
  };
})();

const a = Singleton.getInstance();
const b = Singleton.getInstance();
console.log(a === b); // true
```

✅ Use case: App settings, DB connections, logging services.


### 🔹 129. **What is the Factory Pattern?**

The **Factory Pattern** creates objects **without exposing the instantiation logic**.

🏭 Example:

```js
function Car(type) {
  if (type === "sedan") {
    return { brand: "Toyota", seats: 5 };
  } else if (type === "truck") {
    return { brand: "Ford", seats: 2 };
  }
}

const myCar = Car("sedan");
console.log(myCar); // { brand: "Toyota", seats: 5 }
```

✅ Use case: When object creation is complex or dynamic.



### 🔹 130. **What is the Observer Pattern?**

The **Observer Pattern** is a pub-sub system where multiple observers **subscribe** to changes in an object and are **notified** when it changes.

👁️ Example:

```js
class Subject {
  constructor() {
    this.observers = [];
  }

  subscribe(fn) {
    this.observers.push(fn);
  }

  notify(data) {
    this.observers.forEach(fn => fn(data));
  }
}

const subject = new Subject();
subject.subscribe((msg) => console.log(`Received: ${msg}`));
subject.notify("Hello Observers!");
```

✅ Use case: Event systems, data-binding (React, Vue, Angular).



### 🔹 131. **What is the Revealing Module Pattern?**

The **Revealing Module Pattern** is a variation of the Module Pattern where all methods are defined privately and then **revealed via return**.

🔍 Example:

```js
const Calculator = (function () {
  let add = (a, b) => a + b;
  let subtract = (a, b) => a - b;

  return {
    add,
    subtract
  };
})();

console.log(Calculator.add(5, 3)); // 8
```

✅ Benefit: Clear separation of public/private logic.



## ✅ Testing in JavaScript



### 🔹 132. **What is Unit Testing?**

**Unit Testing** involves testing **individual units** (functions or components) in isolation to ensure they behave as expected.

✅ Example:

```js
function add(a, b) {
  return a + b;
}

// Test
console.assert(add(2, 3) === 5, "add() should return 5");
```



### 🔹 133. **Popular JavaScript Testing Frameworks**

🧪 Widely used frameworks:

* **Jest** – Built by Facebook, great for React
* **Mocha** – Flexible and widely adopted
* **Chai** – Assertion library often used with Mocha
* **Jasmine** – Older, BDD style
* **Cypress** – For end-to-end testing
* **Testing Library** – DOM testing with React, Vue, etc.


### 🔹 134. **What is Jest?**

[Jest](https://jestjs.io) is a **testing framework** for JavaScript with:

* Zero config
* Built-in assertions
* Snapshot testing
* Code coverage

🧠 Example:

```js
// math.js
export function add(a, b) {
  return a + b;
}

// math.test.js
import { add } from './math';

test('adds two numbers', () => {
  expect(add(2, 3)).toBe(5);
});
```

Run using: `npx jest`



### 🔹 135. **What is Mocha?**

[Mocha](https://mochajs.org/) is a flexible test framework for Node and browser-based apps. It supports:

* Asynchronous testing
* BDD/TDD interfaces
* Custom reporters

🧠 Example:

```js
const assert = require('assert');

describe('Math Tests', () => {
  it('should return sum', () => {
    assert.strictEqual(2 + 3, 5);
  });
});
```

Run using: `npx mocha`



### 🔹 136. **How to write a test case in JavaScript?**

✅ Generic format:

```js
describe('FunctionName', () => {
  it('should return expected value', () => {
    const result = myFunction(input);
    expect(result).toBe(expected);
  });
});
```

✅ With Jest:

```js
function isEven(n) {
  return n % 2 === 0;
}

test('isEven returns true for even numbers', () => {
  expect(isEven(4)).toBe(true);
});
```

✅ With Mocha + Chai:

```js
const chai = require('chai');
const expect = chai.expect;

describe('isEven', () => {
  it('should return true for even numbers', () => {
    expect(isEven(4)).to.be.true;
  });
});
```


## ✅ JavaScript and TypeScript

### 137. **What is TypeScript?**

**TypeScript** is a superset of JavaScript developed by Microsoft. It adds **static typing** to JavaScript.

#### Example:

```typescript
// TypeScript
let name: string = "Anti Killer";
name = 123; // ❌ Error: Type 'number' is not assignable to type 'string'
```

* Compiles to plain JavaScript (`.ts` ➝ `.js`).
* Helps in **large-scale application development**.
* Detects errors at **compile time** rather than runtime.


### 138. **What are the benefits of using TypeScript?**

✅ **Benefits:**

1. **Static Typing** – Helps catch type-related errors at compile time.
2. **IDE Support** – Intelligent code completion, inline docs, and refactoring.
3. **Better Code Maintenance** – Self-documented code with types.
4. **Improved Collaboration** – Easier to understand APIs for large teams.
5. **Early Bug Detection** – Errors are caught before runtime.
6. **ES6+ Support** – Write modern JavaScript that compiles to ES5 for older browsers.



### 139. **How is TypeScript different from JavaScript?**

| Feature                | JavaScript             | TypeScript                            |
| ---------------------- | ---------------------- | ------------------------------------- |
| Typing                 | Dynamically typed      | Statically typed                      |
| Compilation            | Interpreted at runtime | Compiled to JavaScript before running |
| Error Checking         | Runtime                | Compile-time                          |
| Support for Interfaces | ❌ No                   | ✅ Yes                                 |
| Community/Adoption     | Widely adopted         | Rapidly growing                       |



### 140. **What are interfaces in TypeScript?**

Interfaces define the **structure of an object** — like a contract. They ensure consistency in objects used throughout the code.

#### Example:

```typescript
interface Person {
  name: string;
  age: number;
  greet(): void;
}

const user: Person = {
  name: "Anti Killer",
  age: 25,
  greet() {
    console.log(`Hello, ${this.name}`);
  }
};
```


### 141. **What are types and enums in TypeScript?**

#### `type`:

Used to define **custom types**.

```typescript
type UserID = string | number;

let id: UserID;
id = 123;  // ✅
id = "abc"; // ✅
```

#### `enum`:

Defines a set of **named constants**.

```typescript
enum Role {
  ADMIN,
  USER,
  GUEST
}

let role: Role = Role.ADMIN;
console.log(role); // 0
```

You can also assign custom values:

```typescript
enum Status {
  SUCCESS = 200,
  NOT_FOUND = 404
}
```



## ✅ Common Interview Coding Challenges



### 142. **Reverse a string**

```js
function reverseString(str) {
  return str.split('').reverse().join('');
}
console.log(reverseString("hello")); // "olleh"
```



### 143. **Check if a string is a palindrome**

```js
function isPalindrome(str) {
  return str === str.split('').reverse().join('');
}
console.log(isPalindrome("madam")); // true
```



### 144. **Find the factorial of a number**

```js
function factorial(n) {
  if (n === 0) return 1;
  return n * factorial(n - 1);
}
console.log(factorial(5)); // 120
```


### 145. **FizzBuzz Problem**

```js
for (let i = 1; i <= 100; i++) {
  let out = "";
  if (i % 3 === 0) out += "Fizz";
  if (i % 5 === 0) out += "Buzz";
  console.log(out || i);
}
```



### 146. **Find the largest/smallest number in an array**

```js
const arr = [5, 2, 9, 1];
console.log(Math.max(...arr)); // 9
console.log(Math.min(...arr)); // 1
```



### 147. **Remove duplicates from an array**

```js
const arr = [1, 2, 2, 3];
const unique = [...new Set(arr)];
console.log(unique); // [1, 2, 3]
```


### 148. **Flatten a nested array**

```js
function flatten(arr) {
  return arr.flat(Infinity);
}
console.log(flatten([1, [2, [3, [4]]]])); // [1, 2, 3, 4]
```



### 149. **Implement a debounce function**

```js
function debounce(fn, delay) {
  let timeout;
  return function (...args) {
    clearTimeout(timeout);
    timeout = setTimeout(() => fn.apply(this, args), delay);
  };
}
```

**Use case:** Limit API call while typing in input field.



### 150. **Implement a throttle function**

```js
function throttle(fn, delay) {
  let lastCall = 0;
  return function (...args) {
    const now = new Date().getTime();
    if (now - lastCall >= delay) {
      lastCall = now;
      fn.apply(this, args);
    }
  };
}
```



### 151. **Check if two arrays are equal**

```js
function arraysEqual(a, b) {
  return a.length === b.length && a.every((val, i) => val === b[i]);
}
```



### 152. **Find the missing number in a sequence**

```js
function findMissing(arr) {
  let n = arr.length + 1;
  let total = (n * (n + 1)) / 2;
  let sum = arr.reduce((acc, curr) => acc + curr, 0);
  return total - sum;
}
```



### 153. **Check for anagram**

```js
function isAnagram(str1, str2) {
  return str1.split('').sort().join('') === str2.split('').sort().join('');
}
```


### 154. **Count the number of vowels in a string**

```js
function countVowels(str) {
  return (str.match(/[aeiou]/gi) || []).length;
}
```


### 155. **Implement bind/call/apply manually**

```js
Function.prototype.myCall = function (ctx, ...args) {
  ctx.fn = this;
  ctx.fn(...args);
  delete ctx.fn;
};
```



### 156. **Create a deep clone of an object**

```js
function deepClone(obj) {
  return JSON.parse(JSON.stringify(obj));
}
```

> 🔥 For more robust cloning (including functions and Dates), use `structuredClone(obj)` in modern browsers.


### 157. **Find the longest word in a sentence**

```js
function longestWord(str) {
  return str.split(' ').reduce((longest, curr) =>
    curr.length > longest.length ? curr : longest, ""
  );
}
```



### 158. **Capitalize the first letter of each word**

```js
function capitalizeWords(str) {
  return str.replace(/\b\w/g, char => char.toUpperCase());
}
```



### 159. **Implement a custom Promise**

A simplified custom Promise constructor:

```js
class MyPromise {
  constructor(executor) {
    this.onResolve = null;
    executor(this.resolve.bind(this));
  }

  resolve(value) {
    if (this.onResolve) {
      this.onResolve(value);
    }
  }

  then(callback) {
    this.onResolve = callback;
  }
}

new MyPromise((res) => res("Resolved!")).then(console.log);
```



### 160. **Create a custom map or reduce**

#### Custom `map`:

```js
Array.prototype.myMap = function (cb) {
  let result = [];
  for (let i = 0; i < this.length; i++) {
    result.push(cb(this[i], i, this));
  }
  return result;
};
```

#### Custom `reduce`:

```js
Array.prototype.myReduce = function (cb, initial) {
  let acc = initial;
  for (let i = 0; i < this.length; i++) {
    acc = cb(acc, this[i], i, this);
  }
  return acc;
};
```


✅ **Miscellaneous JavaScript Questions**


### ✅ 161. **What is JSON?**

**JSON (JavaScript Object Notation)** is a lightweight **data-interchange format**, easy for humans to read and write, and easy for machines to parse and generate.

* Used for transmitting data between a server and web application.

#### Example:

```json
{
  "name": "Anti Killer",
  "age": 25,
  "isDeveloper": true
}
```

* JSON supports: strings, numbers, objects, arrays, booleans, and `null`.



### ✅ 162. **Difference between JSON and JavaScript object**

| Feature           | JSON                                  | JavaScript Object                       |
| ----------------- | ------------------------------------- | --------------------------------------- |
| Format            | String format                         | Native object                           |
| Quotes            | Keys & strings must use double quotes | Can use unquoted keys and single quotes |
| Data Type Support | Limited (no functions, `undefined`)   | Full JS support (functions, symbols)    |
| Usage             | Data transfer                         | Program logic                           |

#### Example:

```json
// JSON (used in APIs)
{ "name": "Anti" }

// JavaScript Object
{ name: "Anti" }
```



### ✅ 163. **What is `eval()`?**

`eval()` is a function that **executes a string of JavaScript code**.

#### Example:

```js
eval("console.log('Hello from eval')"); // Logs: Hello from eval
```



### ✅ 164. **Why is `eval()` considered dangerous?**

❌ **Security Risk**:

* Can execute **malicious code**.
* Allows **code injection attacks** (XSS).

❌ **Performance Hit**:

* Prevents JavaScript engine optimizations.

❌ **Hard to Debug**:

* Errors inside `eval()` are harder to track.

> 🔥 Avoid using `eval()` unless absolutely necessary. Use `JSON.parse()` or safer alternatives.



### ✅ 165. **What is a polyfill?**

A **polyfill** is a piece of JavaScript code used to provide modern functionality in **older browsers** that do not natively support it.

#### Example: `Array.prototype.includes()`

```js
if (!Array.prototype.includes) {
  Array.prototype.includes = function (searchElement) {
    return this.indexOf(searchElement) !== -1;
  };
}
```



### ✅ 166. **What is transpilation?**

**Transpilation** is the process of converting source code from one language to another **at the same level of abstraction**.

🔄 Example: TypeScript ➝ JavaScript or ES6 ➝ ES5

Used to:

* Ensure compatibility with older environments
* Use modern language features



### ✅ 167. **What is Babel?**

[Babel](https://babeljs.io) is a **JavaScript compiler** used to transpile **modern JS (ES6+) to older versions (ES5)** for browser compatibility.

🛠 Features:

* Converts arrow functions, classes, async/await
* Works with React JSX
* Has a plugin system

#### Example:

```js
// ES6 input
const greet = () => console.log("Hi");

// Babel output (ES5)
var greet = function () {
  console.log("Hi");
};
```



### ✅ 168. **Difference between compilation and interpretation**

| Feature | Compilation            | Interpretation                     |
| ------- | ---------------------- | ---------------------------------- |
| Timing  | Before execution       | During execution                   |
| Output  | Machine code           | Executes line-by-line              |
| Speed   | Faster (once compiled) | Slower                             |
| Example | C, Java                | Python, JavaScript (traditionally) |

🔁 **JavaScript is both interpreted and compiled** — via Just-In-Time (JIT) compilation.


### ✅ 169. **What are JavaScript engines?**

A **JavaScript engine** is a program that interprets and executes JavaScript code.

| Engine Name    | Browser         |
| -------------- | --------------- |
| V8             | Chrome, Node.js |
| SpiderMonkey   | Firefox         |
| JavaScriptCore | Safari          |
| Chakra         | Edge (old)      |

📌 Most engines use **JIT compilation** for better performance.



### ✅ 170. **Stack vs Heap Memory**

| Feature      | Stack                         | Heap                           |
| ------------ | ----------------------------- | ------------------------------ |
| Usage        | Primitive values (fixed size) | Objects, arrays (dynamic size) |
| Memory Size  | Small                         | Large                          |
| Access Speed | Fast                          | Slower                         |
| Lifecycle    | Auto-managed (LIFO)           | Manual/GC-managed              |

#### Example:

```js
let x = 10;            // Stored in stack
let obj = { name: "A" }; // Stored in heap
```



### ✅ 171. **How does JavaScript handle concurrency?**

JS is **single-threaded**, but handles concurrency via the **event loop** using:

* **Call Stack**
* **Web APIs (Browser)**: `setTimeout`, `fetch`, DOM
* **Callback Queue (Macrotasks)**
* **Microtask Queue**: `Promise.then()`

🌀 Event Loop coordinates all tasks and ensures non-blocking behavior.



### ✅ 172. **What is debouncing and throttling?**

| Technique | Use Case             | Behavior                                     |
| --------- | -------------------- | -------------------------------------------- |
| Debounce  | Input fields, search | Runs **after a delay** since the last call   |
| Throttle  | Scroll/Resize events | Runs **at intervals**, ignoring excess calls |

#### Debounce Example:

```js
function debounce(fn, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}
```



### ✅ 173. **Microtask vs Macrotask Queue**

| Queue          | Examples                                    | Priority |
| -------------- | ------------------------------------------- | -------- |
| **Microtasks** | `Promise.then`, `MutationObserver`          | High     |
| **Macrotasks** | `setTimeout`, `setInterval`, `setImmediate` | Low      |

✅ **Microtasks are executed before any macrotasks**, after the current stack is cleared.

#### Example:

```js
console.log("Start");

setTimeout(() => console.log("Macrotask"), 0);

Promise.resolve().then(() => console.log("Microtask"));

console.log("End");

// Output:
// Start
// End
// Microtask
// Macrotask
```



### ✅ 174. **What is reflow and repaint in the browser?**

* **Reflow**: When the browser recalculates **layout and geometry** (e.g., DOM changes).
* **Repaint**: When the browser updates **pixels** (e.g., color, visibility).

#### Cost:

* Reflows are **expensive**. Try to **batch DOM changes**.
* Avoid triggering layout thrashing (`offsetHeight`, `getBoundingClientRect`).

 

### ✅ 175. **What are Web Workers?**

**Web Workers** run **JavaScript code in background threads**, separate from the main thread.

📌 Useful for:

* Long computations
* Keeping UI responsive

#### Example:

```js
const worker = new Worker('worker.js');
worker.postMessage("Hello");

worker.onmessage = function (e) {
  console.log("Message from worker: " + e.data);
};
```

> Inside `worker.js`:

```js
onmessage = function (e) {
  postMessage("Received: " + e.data);
};
```


## ✅ Latest ES Features (ES7 to ES13)


### 176. **What is `Array.prototype.includes()`?** (ES7 - ES2016)

Checks if an array **includes a specific element**. Returns `true` or `false`.

```js
const fruits = ['apple', 'banana', 'mango'];
console.log(fruits.includes('banana')); // true
console.log(fruits.includes('grape'));  // false
```

✔ More readable alternative to `indexOf()`.


### 177. **What is the Exponentiation Operator `**`?** (ES7 - ES2016)

Used to raise a number to a power.

```js
console.log(2 ** 3); // 8
// Equivalent to Math.pow(2, 3)
```



### 178. **What is `async/await`?** (ES8 - ES2017)

A **syntax sugar** over Promises for handling asynchronous operations in a cleaner way.

```js
async function fetchData() {
  const res = await fetch('https://api.example.com/data');
  const data = await res.json();
  console.log(data);
}
```

✔ Makes async code look synchronous.



### 179. **What is `Object.entries()` and `Object.values()`?** (ES8 - ES2017)

* `Object.entries()` → Returns array of key-value pairs.
* `Object.values()` → Returns array of values.

```js
const obj = { a: 1, b: 2 };

console.log(Object.entries(obj)); // [['a', 1], ['b', 2]]
console.log(Object.values(obj));  // [1, 2]
```



### 180. **What is Optional Chaining (`?.`)?** (ES11 - ES2020)

Safely access nested properties without throwing an error if a part is `undefined` or `null`.

```js
const user = { profile: { name: "Anti" } };

console.log(user.profile?.name);     // "Anti"
console.log(user.contact?.email);    // undefined (no error)
```



### 181. **What is Nullish Coalescing (`??`)?** (ES11 - ES2020)

Returns the **right-hand value only if the left-hand is `null` or `undefined`**.

```js
const val = null ?? "default";
console.log(val); // "default"

0 ?? 5           // returns 0 (because 0 is not null/undefined)
```

✔ Avoids unintended fallback for falsy values like 0, false.



### 182. **What are Private Class Fields?** (ES12 - ES2021)

Use `#` prefix to declare private variables inside classes.

```js
class Counter {
  #count = 0;

  increment() {
    this.#count++;
    console.log(this.#count);
  }
}

const c = new Counter();
c.increment(); // 1
// c.#count; ❌ SyntaxError: Private field '#count' must be declared
```



### 183. **What is Dynamic Import?** (ES11 - ES2020)

Loads a module **only when needed**, useful for **code splitting** and performance.

```js
button.addEventListener("click", async () => {
  const { showAlert } = await import("./utils.js");
  showAlert("Dynamic import loaded!");
});
```

✔ Reduces initial load time in web apps.

 

### 184. **What is the BigInt type?** (ES11 - ES2020)

`BigInt` allows working with integers **beyond 2<sup>53</sup> - 1**, which is the limit for regular numbers in JavaScript.

```js
const big = 1234567890123456789012345678901234567890n;
console.log(typeof big); // "bigint"
```

 

###  185. **What is `Promise.allSettled()`?** (ES11 - ES2020)

Waits for **all promises to settle** (either fulfilled or rejected), and returns their results.

```js
const promises = [
  Promise.resolve(1),
  Promise.reject("error"),
  Promise.resolve(3)
];

Promise.allSettled(promises).then(results => console.log(results));
```

✔ Useful when you want to process all results, even if some fail.

 

## ✅ Front-End Framework Integration

 

### 186. **How does JavaScript integrate with HTML/CSS?**

* JavaScript **manipulates HTML (DOM)** and CSS (styles) dynamically.
* Integrates via:

  * Inline: `<script>alert("Hi")</script>`
  * External: `<script src="app.js"></script>`
* Used to:

  * Handle events (click, input)
  * Update styles
  * Create elements dynamically

```html
<button onclick="changeColor()">Click</button>
<script>
  function changeColor() {
    document.body.style.background = "skyblue";
  }
</script>
```

 

### 187. **What is the role of JavaScript in SPAs (Single Page Applications)?**

SPA = Web app that **loads a single HTML page** and dynamically updates it using JS (usually via frameworks like React, Vue, Angular).

🔧 JavaScript handles:

* **Routing** (via libraries like React Router)
* **Dynamic content rendering**
* **State management**
* **API communication (AJAX/fetch)**

✔ Faster UX, no full-page reloads.



### 188. **What is Virtual DOM?**

A **lightweight copy of the real DOM** used by libraries like React to optimize updates.

🔁 When state changes:

* React updates the Virtual DOM
* Compares with previous version (diffing)
* Applies **minimum real DOM changes** (reconciliation)

✔ Improves performance and efficiency.



### 189. **Difference between Vanilla JS and React**

| Feature          | Vanilla JS                 | React (Library)          |
| ---------------- | -------------------------- | ------------------------ |
| DOM Handling     | Manual                     | Declarative Virtual DOM  |
| Code Structure   | Imperative                 | Component-based          |
| Reusability      | Low                        | High (components)        |
| State Management | Custom code or global vars | useState, Redux, Context |
| Learning Curve   | Low                        | Medium                   |


### 190. **How is State Managed in JavaScript Apps?**

#### In Vanilla JS:

```js
let state = { count: 0 };

function increment() {
  state.count++;
  document.getElementById("count").innerText = state.count;
}
```

#### In React:

```jsx
function Counter() {
  const [count, setCount] = useState(0);
  return <button onClick={() => setCount(count + 1)}>{count}</button>;
}
```

#### Advanced State Management:

* **Redux**: Centralized global state (flux pattern)
* **Context API**: Lightweight built-in global state
* **Zustand / Recoil**: Lightweight alternatives

✔ State management is key to UI updates and reactivity in modern JS apps.



## ✅ Security & Best Practices



### 191. **What is XSS and how to prevent it?**

**XSS (Cross-Site Scripting)** is a type of security vulnerability where an attacker injects malicious scripts into webpages viewed by others.

#### ❌ Example (vulnerable):

```html
<div id="user"></div>
<script>
  const username = location.search.slice(1); // e.g., ?<script>alert(1)</script>
  document.getElementById('user').innerHTML = username;
</script>
```

#### ✅ Prevention:

* Use `textContent` instead of `innerHTML`.
* Sanitize user input.
* Use CSP (Content Security Policy).
* Escape dynamic values.

```js
document.getElementById('user').textContent = username;
```



### 192. **What is CSRF?**

**CSRF (Cross-Site Request Forgery)** forces a logged-in user to perform unwanted actions on a web application they are authenticated in.

#### Example:

* User logged into `bank.com`.
* Visits `evil.com` which sends a hidden request to `bank.com/transfer`.

#### ✅ Prevention:

* Use **CSRF tokens**.
* Use **SameSite cookies**.
* Validate **HTTP referers/origin headers**.



### 193. **How to write secure JavaScript code?**

✅ Tips:

* **Validate & sanitize inputs**.
* Never use `eval()`.
* Use `HTTPS`.
* Avoid exposing sensitive data in frontend.
* Use proper **authentication** (tokens, JWT, etc.).
* Use **CSP headers** and **security linters**.



### 194. **What are best practices for writing JavaScript?**

✅ Best Practices:

* Use `const` and `let` (not `var`).
* Keep functions small and reusable.
* Use strict mode: `"use strict";`.
* Prefer `===` over `==`.
* Avoid deep nesting; use early returns.
* Use meaningful names (`getUserData`, not `getData`).
* Comment where necessary (but avoid over-commenting).
* Follow consistent code style (Prettier, ESLint).



### 195. **Why should you avoid global variables?**

❌ Global variables:

* Cause **naming conflicts**.
* Make code **hard to maintain**.
* Leak across modules unintentionally.
* Are hard to debug.

✅ Use block scope (`let`, `const`) and modules (`import/export`) to contain variables.



### 196. **How to handle asynchronous errors?**

#### With Promises:

```js
fetch('/data.json')
  .then(res => res.json())
  .catch(err => console.error("Failed:", err));
```

#### With async/await:

```js
async function getData() {
  try {
    const res = await fetch('/data.json');
    const data = await res.json();
  } catch (error) {
    console.error("Error fetching data", error);
  }
}
```

✅ Always wrap async code in `try...catch`.



### 197. **What is input sanitization?**

Input sanitization means **cleaning and validating** user-provided input to ensure:

* No malicious characters/scripts are injected.
* Data is of expected format/type.

#### Example:

```js
function sanitize(input) {
  return input.replace(/[<>&"'\/]/g, "");
}

sanitize("<script>"); // ""
```

✅ Use libraries like **DOMPurify** for HTML sanitization.



### 198. **What are some anti-patterns in JavaScript?**

Anti-patterns = common but **bad programming practices**.

#### Examples:

* Using `var` instead of `let/const`.
* Modifying built-in objects like `Array.prototype`.
* Using global variables excessively.
* Deep nesting of conditionals.
* Callback hell:

  ```js
  doA(() => {
    doB(() => {
      doC(() => { /* ... */ });
    });
  });
  ```

✅ Prefer Promises/async functions to avoid callback hell.



## ✅ JavaScript in Interviews



### 199. **What are some tricky JS questions asked in interviews?**

✅ Examples:

* What is the output of:

  ```js
  console.log([] + []); // ""
  console.log([] + {}); // "[object Object]"
  ```

* Explain closure with example.

* Difference between `==` and `===`.

* Explain event loop, microtasks, macrotasks.

* What are `call`, `apply`, and `bind`?


### 200. **Difference between `Object.freeze()` and `Object.seal()`**

| Feature                        | `Object.freeze()` | `Object.seal()`                |
| ------------------------------ | ----------------- | ------------------------------ |
| Add properties                 | ❌ Not allowed     | ❌ Not allowed                  |
| Remove properties              | ❌ Not allowed     | ❌ Not allowed                  |
| Modify properties              | ❌ Not allowed     | ✅ Allowed (existing ones only) |
| Make property non-configurable | ✅                 | ✅                              |

```js
const obj = { name: "Anti" };

Object.freeze(obj);
obj.name = "New"; // ❌ No change

Object.seal(obj);
obj.name = "Updated"; // ✅ Works
```



### 201. **How would you optimize a web page using JavaScript?**

✅ Techniques:

* Lazy load images (`<img loading="lazy">`)
* Code splitting (dynamic import)
* Minify JavaScript (Terser, UglifyJS)
* Avoid memory leaks (detach listeners)
* Use throttling/debouncing
* Reduce DOM access
* Cache DOM queries
* Use Service Workers for caching
* Defer or async non-critical scripts


### 202. **What are some common JavaScript pitfalls?**

❌ Pitfalls and gotchas:

* **Falsy traps**: `0`, `""`, `null`, `undefined`, `NaN`, `false`
* Using `==` instead of `===`
* Forgetting `break` in `switch`
* Accidentally declaring globals:

  ```js
  function foo() {
    bar = 10; // global leak if `var/let/const` is missing
  }
  ```
* Mutating objects unintentionally (pass by reference)
* Incorrect `this` context
* Mixing async and sync code

