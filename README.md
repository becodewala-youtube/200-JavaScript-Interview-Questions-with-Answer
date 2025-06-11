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


