# JavaScript for Complete Beginners

## What is JavaScript?

Think of a website like a house:
- **HTML** = the walls and structure
- **CSS** = the paint and decoration
- **JavaScript** = the electricity (makes things work!)

JavaScript makes websites **interactive** — buttons click, forms submit, popups appear.

---

## 1. Your First JavaScript

Open browser → Press **F12** → Click **Console** → Type this:

```javascript
console.log("Hello World");
```

Hit Enter → You'll see `Hello World` printed!

> 💡 `console.log()` is like telling JavaScript **"print this on screen"**

---

## 2. Variables — Storing Information

Think of a variable like a **box with a label** on it. You put something inside the box and use the label to find it later.

```javascript
// Creating boxes (variables)
let name = "Alice";
let age  = 25;

// Looking inside the box
console.log(name);   // Alice
console.log(age);    // 25
```

```
 ___________        ___________
|           |      |           |
|  "Alice"  |      |    25     |
|___________|      |___________|
    name                age
```

**3 ways to create variables:**

```javascript
let   age  = 25;       // ✅ use this — can change later
const PI   = 3.14;     // ✅ use this — cannot change
var   name = "old";    // ❌ avoid — old way
```

---

## 3. Data Types — Types of Information

Just like in real life — a name is different from a number:

```javascript
// Text (called String) — always in quotes
let firstName = "John";
let lastName  = 'Doe';       // single or double quotes both work

// Number — no quotes
let age    = 30;
let price  = 9.99;

// True or False (called Boolean)
let isLoggedIn = true;
let isAdmin    = false;

// Nothing / Empty
let nothing  = null;         // intentionally empty
let missing  = undefined;    // not given a value yet
```

> 💡 **Simple rule:** Text → use quotes. Numbers → no quotes. Yes/No → true/false

---

## 4. Console.log — Your Best Friend

Use it to **see what's happening** in your code:

```javascript
let name = "Alice";
let age  = 25;

console.log(name);           // Alice
console.log(age);            // 25
console.log("My name is", name, "and I am", age);
// My name is Alice and I am 25
```

---

## 5. Math Operations

JavaScript can work like a calculator:

```javascript
let a = 10;
let b = 3;

console.log(a + b);    // 13  (add)
console.log(a - b);    // 7   (subtract)
console.log(a * b);    // 30  (multiply)
console.log(a / b);    // 3.3 (divide)
console.log(a % b);    // 1   (remainder — what's left over)
```

```javascript
// You can also do math with variables
let price    = 100;
let discount = 20;
let total    = price - discount;

console.log(total);    // 80
```

---

## 6. Joining Text Together (Strings)

```javascript
let firstName = "John";
let lastName  = "Doe";

// Old way — using +
let fullName = firstName + " " + lastName;
console.log(fullName);    // John Doe

// New way — using backticks ` ` (recommended)
let greeting = `Hello, my name is ${firstName} ${lastName}`;
console.log(greeting);    // Hello, my name is John Doe
```

> 💡 The backtick ` way is called a **template literal**. Use `${}` to insert variables inside text.

---

## 7. If / Else — Making Decisions

Just like in real life — **IF** it's raining, take umbrella. **ELSE** don't.

```javascript
let age = 20;

if (age >= 18) {
    console.log("You can vote!");
} else {
    console.log("Too young to vote.");
}
```

**Multiple conditions:**

```javascript
let score = 75;

if (score >= 90) {
    console.log("Grade: A");
} else if (score >= 75) {
    console.log("Grade: B");
} else if (score >= 60) {
    console.log("Grade: C");
} else {
    console.log("Grade: F");
}
```

**Comparison symbols:**

```javascript
>    // greater than
<    // less than
>=   // greater than or equal
<=   // less than or equal
===  // exactly equal      ✅ use this
!==  // not equal
```

---

## 8. Functions — Reusable Instructions

A function is like a **recipe**. You write it once and use it many times.

```javascript
// Writing the recipe (defining the function)
function greet(name) {
    console.log(`Hello, ${name}!`);
}

// Using the recipe (calling the function)
greet("Alice");    // Hello, Alice!
greet("Bob");      // Hello, Bob!
greet("Charlie");  // Hello, Charlie!
```

**Function that gives back a result:**

```javascript
function addNumbers(a, b) {
    return a + b;     // return sends the result back
}

let result = addNumbers(5, 3);
console.log(result);    // 8
```

> 💡 Think of a function like a machine:
> - You put something **in** (parameters)
> - It does some work
> - It gives something **out** (return value)

---

## 9. Arrays — Lists of Things

An array is like a **shopping list** — multiple items in one place.

```javascript
// Creating a list
let fruits = ["apple", "banana", "mango", "grape"];

// Getting items (counting starts from 0!)
console.log(fruits[0]);    // apple   (1st item)
console.log(fruits[1]);    // banana  (2nd item)
console.log(fruits[2]);    // mango   (3rd item)

// How many items?
console.log(fruits.length);    // 4

// Add item to end
fruits.push("orange");
console.log(fruits);    // ["apple", "banana", "mango", "grape", "orange"]

// Remove last item
fruits.pop();
console.log(fruits);    // ["apple", "banana", "mango", "grape"]
```

> ⚠️ **Important:** Counting starts at **0**, not 1!
> ```
> ["apple", "banana", "mango"]
>     0         1        2       ← index numbers
> ```

---

## 10. Loops — Repeating Things

Instead of writing the same thing 100 times, use a loop.

```javascript
// Without loop — bad!
console.log("Hello 1");
console.log("Hello 2");
console.log("Hello 3");

// With loop — good!
for (let i = 1; i <= 3; i++) {
    console.log("Hello " + i);
}
// Hello 1
// Hello 2
// Hello 3
```

**Loop through a list:**

```javascript
let fruits = ["apple", "banana", "mango"];

for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
// apple
// banana
// mango

// Easier way
fruits.forEach(function(fruit) {
    console.log(fruit);
});
```

---

## 11. Objects — Grouping Related Information

An object groups related info together — like a **person's profile card**.

```javascript
// A person object
let person = {
    name:  "Alice",
    age:   30,
    city:  "Amsterdam",
    email: "alice@example.com"
};

// Getting information
console.log(person.name);    // Alice
console.log(person.age);     // 30
console.log(person.city);    // Amsterdam

// Changing information
person.age = 31;
console.log(person.age);     // 31

// Adding new information
person.phone = "123-456";
```

```
person = {
  name:  "Alice"       ← key: value
  age:   30
  city:  "Amsterdam"
}
```

---

## 12. Putting It All Together

```javascript
// A simple student grade checker

let students = [
    { name: "Alice", score: 92 },
    { name: "Bob",   score: 67 },
    { name: "Carol", score: 78 }
];

function getGrade(score) {
    if (score >= 90) {
        return "A";
    } else if (score >= 75) {
        return "B";
    } else if (score >= 60) {
        return "C";
    } else {
        return "F";
    }
}

students.forEach(function(student) {
    let grade = getGrade(student.score);
    console.log(`${student.name} scored ${student.score} → Grade: ${grade}`);
});

// Output:
// Alice scored 92 → Grade: A
// Bob scored 67 → Grade: C
// Carol scored 78 → Grade: B
```

---

## Summary — What You Learned

| Concept | What it does | Example |
|---|---|---|
| Variable | Stores information | `let name = "Alice"` |
| String | Stores text | `"Hello World"` |
| Number | Stores numbers | `25` or `9.99` |
| Boolean | Stores yes/no | `true` or `false` |
| If/Else | Makes decisions | `if (age > 18)` |
| Function | Reusable code block | `function greet(name){}` |
| Array | List of items | `["a", "b", "c"]` |
| Loop | Repeats actions | `for (let i = 0; ...)` |
| Object | Groups related data | `{name: "Alice", age: 30}` |

---

## Your Next Steps

```
1. Variables & Data Types    ✅ Done
2. If / Else                 ✅ Done
3. Functions                 ✅ Done
4. Arrays & Loops            ✅ Done
5. Objects                   ✅ Done
        ↓
6. Learn DOM (control webpage)
7. Learn Async / Await
8. Then start Playwright! 🎭
```

> 💡 **Practice tip:** Open your browser console (F12) and type every example above yourself. Typing it — not copying — is how you truly learn!

**easy method to understand :-----
**

---

# 📚 LESSON 1: Variables & Data Types

## What is a Variable?

Imagine you have **labeled boxes** at home:
- A box labeled **"Name"** contains a piece of paper with "Alice" written on it
- A box labeled **"Age"** contains the number 25
- You can open any box, read what's inside, or replace it with something new

That's exactly what a variable is in programming!

---

## Creating Variables

```javascript
// Syntax: let  boxName = value;

let name = "Alice";
let age  = 25;
let city = "Amsterdam";

// Reading the box
console.log(name);    // Alice
console.log(age);     // 25
console.log(city);    // Amsterdam
```

---

## 3 Keywords — let, const, var

```javascript
// LET — value can change later
let score = 0;
score = 10;      // ✅ allowed — score changed from 0 to 10
score = 50;      // ✅ allowed again
console.log(score);   // 50

// CONST — value can NEVER change
const country = "Netherlands";
country = "France";   // ❌ ERROR! Cannot change a const

// VAR — old way, avoid it
var oldStyle = "don't use this";
```

> 💡 **Simple Rule:**
> - Use `const` by default
> - Use `let` only if the value needs to change
> - Never use `var`

---

## Types of Data

### 1. String — Text

```javascript
let firstName = "John";          // double quotes
let lastName  = 'Doe';           // single quotes — both work!
let message   = "Hello World";

console.log(firstName);    // John
console.log lastName);     // Doe

// Check the type
console.log(typeof firstName);   // "string"
```

### 2. Number

```javascript
let age    = 25;        // whole number
let price  = 9.99;      // decimal number
let temp   = -5;        // negative number

console.log(age);      // 25
console.log(price);    // 9.99

// Check the type
console.log(typeof age);    // "number"
```

### 3. Boolean — Yes or No

```javascript
let isLoggedIn  = true;
let isAdmin     = false;
let hasTicket   = true;

console.log(isLoggedIn);    // true
console.log(isAdmin);       // false

// Check the type
console.log(typeof isLoggedIn);    // "boolean"
```

### 4. Null & Undefined

```javascript
// null — box exists but is intentionally EMPTY
let selectedColor = null;
console.log(selectedColor);    // null

// undefined — box exists but NO value was put in
let userName;
console.log(userName);    // undefined

// Difference
let a = null;        // you chose to leave it empty
let b;               // you forgot to give it a value
```

---

## Real Life Example

```javascript
// A user profile
const firstName   = "Sarah";
const lastName    = "Johnson";
let   age         = 28;
let   isLoggedIn  = false;
let   score       = 0;

console.log(firstName);     // Sarah
console.log(age);           // 28
console.log(isLoggedIn);    // false

// User logs in
isLoggedIn = true;
score      = 100;

console.log(isLoggedIn);    // true
console.log(score);         // 100
```

---

## Common Mistakes Beginners Make

```javascript
// ❌ Mistake 1 — forgetting quotes around text
let name = Alice;      // ERROR! Alice is not defined
let name = "Alice";    // ✅ correct

// ❌ Mistake 2 — using quotes around numbers
let age = "25";        // This is TEXT not a number!
let age = 25;          // ✅ correct number

// ❌ Mistake 3 — wrong spelling of true/false
let active = True;     // ❌ ERROR
let active = true;     // ✅ lowercase always

// ❌ Mistake 4 — spaces in variable names
let first name = "Ali";    // ❌ ERROR
let firstName  = "Ali";    // ✅ use camelCase
let first_name = "Ali";    // ✅ this also works
```

---

## Practice Exercise 1

```javascript
// Try this yourself in browser console!

// Create variables for YOUR information
const name    = "Your Name Here";
const country = "Your Country";
let   age     = 0;           // your age
let   isStudent = true;      // are you a student?

// Print them all
console.log("Name:",    name);
console.log("Country:", country);
console.log("Age:",     age);
console.log("Student:", isStudent);
```

---

# 📚 LESSON 2: If / Else — Making Decisions

## What is If/Else?

Every day you make decisions:
- **IF** it's raining → take umbrella
- **ELSE** → leave umbrella at home

JavaScript does the same thing!

---

## Basic If / Else

```javascript
// Syntax
if (condition) {
    // runs if condition is TRUE
} else {
    // runs if condition is FALSE
}
```

```javascript
// Real example
let isRaining = true;

if (isRaining) {
    console.log("Take an umbrella!");
} else {
    console.log("No umbrella needed.");
}
// Output: Take an umbrella!
```

---

## Comparison Operators

These are used inside `if` conditions:

```javascript
let a = 10;
let b = 5;

console.log(a > b);     // true  — a is greater than b
console.log(a < b);     // false — a is NOT less than b
console.log(a >= 10);   // true  — a is greater than or equal to 10
console.log(a <= 10);   // true  — a is less than or equal to 10
console.log(a === 10);  // true  — a is exactly equal to 10
console.log(a !== b);   // true  — a is NOT equal to b
```

> ⚠️ **Very Important:**
> ```javascript
> =    means ASSIGN (put value in box)
> ===  means COMPARE (are they equal?)
>
> let age = 25;        // assign 25 to age
> if (age === 25)      // check if age equals 25
> ```

---

## If / Else If / Else

```javascript
let score = 75;

if (score >= 90) {
    console.log("Grade A — Excellent!");
} else if (score >= 75) {
    console.log("Grade B — Good job!");
} else if (score >= 60) {
    console.log("Grade C — Passed!");
} else {
    console.log("Grade F — Failed!");
}

// Output: Grade B — Good job!
```

**How it works step by step:**
```
Is score >= 90?  → 75 >= 90 → NO  → skip
Is score >= 75?  → 75 >= 75 → YES → run this block → STOP
```

---

## Logical Operators — AND, OR, NOT

```javascript
let age      = 20;
let hasID    = true;
let isSick   = false;

// AND (&&) — BOTH must be true
if (age >= 18 && hasID) {
    console.log("Welcome in!");    // ✅ runs — both are true
}

// OR (||) — at least ONE must be true
if (age < 18 || isSick) {
    console.log("Cannot enter");
} else {
    console.log("You may enter!");  // ✅ runs
}

// NOT (!) — flips true to false, false to true
if (!isSick) {
    console.log("Healthy person!");   // ✅ runs — isSick is false, !false = true
}
```

---

## Nested If — If inside If

```javascript
let age      = 20;
let hasTicket = true;

if (age >= 18) {
    console.log("Age is valid");

    if (hasTicket) {
        console.log("Has ticket — ENTER!");
    } else {
        console.log("No ticket — buy one first");
    }

} else {
    console.log("Too young — cannot enter");
}
```

---

## Short If — Ternary Operator

For simple yes/no decisions in one line:

```javascript
// Normal if/else
let age = 20;
let message;
if (age >= 18) {
    message = "Adult";
} else {
    message = "Minor";
}

// Same thing — ternary (one line!)
let message = age >= 18 ? "Adult" : "Minor";
//                      ↑ if true  ↑ if false

console.log(message);    // Adult
```

---

## Real Life Example

```javascript
// ATM Machine logic
const balance    = 500;
const withdrawal = 200;
const pin        = 1234;
const enteredPin = 1234;

if (enteredPin !== pin) {
    console.log("Wrong PIN!");
} else if (withdrawal > balance) {
    console.log("Not enough money!");
} else if (withdrawal <= 0) {
    console.log("Invalid amount!");
} else {
    const newBalance = balance - withdrawal;
    console.log(`Success! New balance: $${newBalance}`);
}
// Output: Success! New balance: $300
```

---

## Practice Exercise 2

```javascript
// Try this! Traffic light program
let light = "red";   // change to "yellow" or "green" and see what happens

if (light === "red") {
    console.log("STOP!");
} else if (light === "yellow") {
    console.log("GET READY...");
} else if (light === "green") {
    console.log("GO!");
} else {
    console.log("Invalid traffic light color");
}
```

---

# 📚 LESSON 3: Functions

## What is a Function?

Think of a **function like a recipe**:
- Recipe has a **name** (Chocolate Cake)
- Recipe needs **ingredients** (flour, sugar, eggs)
- Recipe gives you a **result** (a delicious cake!)

You write the recipe once → use it many times!

---

## Creating and Using Functions

```javascript
// STEP 1 — Define (write the recipe)
function greet() {
    console.log("Hello! Welcome!");
}

// STEP 2 — Call (use the recipe)
greet();    // Hello! Welcome!
greet();    // Hello! Welcome!
greet();    // Hello! Welcome!
```

---

## Functions with Parameters (Ingredients)

```javascript
// name is a PARAMETER — like an ingredient slot
function greet(name) {
    console.log(`Hello, ${name}! Welcome!`);
}

// Pass different ARGUMENTS each time
greet("Alice");    // Hello, Alice! Welcome!
greet("Bob");      // Hello, Bob! Welcome!
greet("Charlie");  // Hello, Charlie! Welcome!
```

**Multiple parameters:**

```javascript
function introduce(name, age, city) {
    console.log(`Hi! I'm ${name}, ${age} years old, from ${city}.`);
}

introduce("Alice", 25, "Amsterdam");
// Hi! I'm Alice, 25 years old, from Amsterdam.

introduce("Bob", 30, "London");
// Hi! I'm Bob, 30 years old, from London.
```

---

## Return — Getting a Result Back

```javascript
// Without return — does something but gives nothing back
function sayHello(name) {
    console.log(`Hello ${name}`);
    // no return — like a machine that works but gives nothing back
}

// With return — gives a result back
function addNumbers(a, b) {
    return a + b;    // sends the result back to whoever called it
}

let result = addNumbers(5, 3);
console.log(result);    // 8

// You can use result in calculations
let total = addNumbers(10, 20) + addNumbers(5, 5);
console.log(total);    // 40
```

---

## Default Parameters

```javascript
// If no value given, use default
function greet(name = "Stranger") {
    console.log(`Hello, ${name}!`);
}

greet("Alice");    // Hello, Alice!
greet();           // Hello, Stranger!  ← uses default
```

---

## Arrow Functions — Shorter Way to Write

```javascript
// Regular function
function add(a, b) {
    return a + b;
}

// Same thing — arrow function
const add = (a, b) => {
    return a + b;
};

// Even shorter — one line
const add = (a, b) => a + b;

// Using it
console.log(add(5, 3));    // 8
```

---

## Real Life Function Examples

```javascript
// Calculate total price with tax
function calculateTotal(price, taxRate) {
    const tax   = price * taxRate;
    const total = price + tax;
    return total;
}

console.log(calculateTotal(100, 0.21));    // 121
console.log(calculateTotal(50, 0.21));     // 60.5

// Check if person can vote
function canVote(age) {
    if (age >= 18) {
        return true;
    } else {
        return false;
    }
}

console.log(canVote(20));    // true
console.log(canVote(15));    // false
```

---

## Practice Exercise 3

```javascript
// Write a function that:
// 1. Takes a temperature in Celsius
// 2. Converts it to Fahrenheit
// 3. Returns the result
// Formula: (celsius × 9/5) + 32

function celsiusToFahrenheit(celsius) {
    // write your code here
    return (celsius * 9/5) + 32;
}

console.log(celsiusToFahrenheit(0));     // 32
console.log(celsiusToFahrenheit(100));   // 212
console.log(celsiusToFahrenheit(37));    // 98.6
```

---

# 📚 LESSON 4: Arrays & Loops

## Arrays — Shopping Lists

```javascript
// Without array — messy!
let fruit1 = "apple";
let fruit2 = "banana";
let fruit3 = "mango";

// With array — clean!
let fruits = ["apple", "banana", "mango", "grape", "orange"];
```

## Accessing Items

```javascript
let fruits = ["apple", "banana", "mango"];
//  index:       0         1        2

console.log(fruits[0]);    // apple   (1st)
console.log(fruits[1]);    // banana  (2nd)
console.log(fruits[2]);    // mango   (3rd)
console.log(fruits[3]);    // undefined (doesn't exist!)

// Last item
console.log(fruits[fruits.length - 1]);    // mango
```

## Adding and Removing Items

```javascript
let fruits = ["apple", "banana"];

// Add to END
fruits.push("mango");
console.log(fruits);    // ["apple", "banana", "mango"]

// Remove from END
fruits.pop();
console.log(fruits);    // ["apple", "banana"]

// Add to START
fruits.unshift("kiwi");
console.log(fruits);    // ["kiwi", "apple", "banana"]

// Remove from START
fruits.shift();
console.log(fruits);    // ["apple", "banana"]
```

## Useful Array Methods

```javascript
let fruits = ["apple", "banana", "mango", "grape"];

// Does it include something?
console.log(fruits.includes("mango"));     // true
console.log(fruits.includes("pizza"));     // false

// Where is the item?
console.log(fruits.indexOf("banana"));     // 1

// How many items?
console.log(fruits.length);               // 4

// Join into one string
console.log(fruits.join(", "));
// "apple, banana, mango, grape"
```

---

## Loops — Doing Things Repeatedly

### For Loop

```javascript
// Print numbers 1 to 5
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
// 1
// 2
// 3
// 4
// 5
```

**Breaking it down:**
```
for ( let i = 1  ;  i <= 5  ;  i++  )
       ↑ start      ↑ stop     ↑ step
       begin at 1   stop at 5  add 1 each time
```

### Loop Through an Array

```javascript
let fruits = ["apple", "banana", "mango"];

for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
// apple
// banana
// mango
```

### forEach — Easier Way

```javascript
let fruits = ["apple", "banana", "mango"];

fruits.forEach(function(fruit) {
    console.log(fruit);
});

// Same with arrow function
fruits.forEach(fruit => {
    console.log(fruit);
});
```

### While Loop

```javascript
// Keeps going WHILE condition is true
let count = 1;

while (count <= 5) {
    console.log(count);
    count++;    // ⚠️ don't forget this! or it runs forever
}
// 1 2 3 4 5
```

---

## Powerful Array Methods

```javascript
let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

// MAP — transform every item
let doubled = numbers.map(num => num * 2);
console.log(doubled);
// [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]

// FILTER — keep only matching items
let evens = numbers.filter(num => num % 2 === 0);
console.log(evens);
// [2, 4, 6, 8, 10]

// FIND — get first matching item
let firstOver5 = numbers.find(num => num > 5);
console.log(firstOver5);    // 6
```

---

## Practice Exercise 4

```javascript
let prices = [10, 25, 8, 42, 15, 3, 99, 17];

// 1. Print all prices
prices.forEach(price => console.log(price));

// 2. Double all prices
let doubled = prices.map(price => price * 2);
console.log(doubled);

// 3. Find prices under $20
let cheap = prices.filter(price => price < 20);
console.log(cheap);    // [10, 8, 15, 3, 17]

// 4. Find first price over $40
let expensive = prices.find(price => price > 40);
console.log(expensive);    // 42
```

---

# 📚 LESSON 5: Objects

## What is an Object?

An object groups **related information** together — like a **profile card**:

```
┌─────────────────────────┐
│  👤 USER PROFILE        │
├─────────────────────────┤
│  Name:    Alice         │
│  Age:     30            │
│  City:    Amsterdam     │
│  Email:   alice@...     │
└─────────────────────────┘
```

In JavaScript:

```javascript
let user = {
    name:  "Alice",
    age:   30,
    city:  "Amsterdam",
    email: "alice@example.com"
};
```

---

## Accessing Object Data

```javascript
let user = {
    name: "Alice",
    age:  30,
    city: "Amsterdam"
};

// Dot notation (most common)
console.log(user.name);    // Alice
console.log(user.age);     // 30

// Bracket notation
console.log(user["city"]);    // Amsterdam
```

---

## Changing Object Data

```javascript
let user = {
    name: "Alice",
    age:  30
};

// Update existing
user.age = 31;
console.log(user.age);    // 31

// Add new property
user.phone = "123-456-789";
console.log(user.phone);    // 123-456-789

// Delete property
delete user.phone;
console.log(user.phone);    // undefined
```

---

## Objects with Functions (Methods)

```javascript
let user = {
    name: "Alice",
    age:  30,

    greet: function() {
        console.log(`Hi! I'm ${this.name}`);
        //                      ↑ 'this' means THIS object
    },

    isAdult: function() {
        return this.age >= 18;
    }
};

user.greet();              // Hi! I'm Alice
console.log(user.isAdult());    // true
```

---

## Array of Objects — Most Common Pattern

```javascript
// List of students
let students = [
    { name: "Alice", age: 20, grade: "A" },
    { name: "Bob",   age: 22, grade: "B" },
    { name: "Carol", age: 19, grade: "A" },
    { name: "Dave",  age: 21, grade: "C" }
];

// Loop through all students
students.forEach(student => {
    console.log(`${student.name} — Grade: ${student.grade}`);
});
// Alice — Grade: A
// Bob   — Grade: B
// Carol — Grade: A
// Dave  — Grade: C

// Find students with Grade A
let topStudents = students.filter(s => s.grade === "A");
console.log(topStudents);
// [{name: "Alice"...}, {name: "Carol"...}]
```

---

## Real Life Example — Shopping Cart

```javascript
// Shopping cart
let cart = [
    { name: "Laptop",  price: 999,  quantity: 1 },
    { name: "Mouse",   price: 29,   quantity: 2 },
    { name: "Keyboard",price: 79,   quantity: 1 }
];

// Print all items
cart.forEach(item => {
    let subtotal = item.price * item.quantity;
    console.log(`${item.name}: $${subtotal}`);
});

// Calculate total
let total = 0;
cart.forEach(item => {
    total += item.price * item.quantity;
});
console.log(`Total: $${total}`);    // Total: $1136
```

---

# 🗺️ Your Learning Path

```
✅ Lesson 1 — Variables & Data Types
✅ Lesson 2 — If / Else
✅ Lesson 3 — Functions
✅ Lesson 4 — Arrays & Loops
✅ Lesson 5 — Objects
        ↓
📌 Next Steps:
   6. DOM — Control webpage elements
   7. Events — React to clicks, typing
   8. Async/Await — Talk to servers
   9. Then → START PLAYWRIGHT! 🎭
```

---

> 💡 **Best way to learn:** Open your browser, press **F12**, click **Console**, and type every single example above by hand. Don't copy-paste — **type it yourself!**



