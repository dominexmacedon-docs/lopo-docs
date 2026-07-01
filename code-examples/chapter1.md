# Chapter 1 — Getting Started

Welcome to **Lopo**, a simple, modern, and beginner-friendly programming language. In this chapter, you'll learn the basic building blocks of every Lopo program.

By the end of this chapter, you'll be able to:

- Print text to the screen
- Write comments
- Create variables using `define`
- Work with numbers and strings
- Use boolean values and `null`
- Perform basic calculations

---

# Syntax Highlighting

The examples in this book use the official Lopo CodeMirror color scheme.

| Token | Color | Example |
|-------|-------|---------|
| **Keyword** | <span style="color:#4ea5ff">Blue</span> | `define`, `if`, `show`, `func` |
| **String** | <span style="color:#22c55e">Green</span> | `"Hello"` |
| **Number** | <span style="color:#f59e0b">Orange</span> | `100`, `3.14` |
| **Comment** | <span style="color:#7f848e">Gray</span> | `# comment` |
| **Variable** | <span style="color:#e5e7eb">White</span> | `name`, `age` |
| **Function** | <span style="color:#a78bfa">Purple</span> | `show()`, `ask()` |
| **Operator** | <span style="color:#f43f5e">Red</span> | `+`, `-`, `*`, `==` |
| **Brackets** | <span style="color:#38bdf8">Cyan</span> | `() [] {}` |
| **Punctuation** | <span style="color:#94a3b8">Light Gray</span> | `; , . :` |

---

# 1.1 Hello, World

Every programming language begins with a simple program.

```lopo
show("Hello, World!");
```

Output

```
Hello, World!
```

The `show()` function prints values to the console.

---

# 1.2 Comments

Comments are ignored by the interpreter.

Use comments to explain your code.

Single-line comment

```lopo
# This is a comment
show("Hello");
```

Another example

```lopo
# Calculate total price
define price = 100;
show(price);
```

Comments make programs easier to understand.

---

# 1.3 Variables with `define`

Variables store data.

Create a variable using the `define` keyword.

```lopo
define name = "Alice";
show(name);
```

Output

```
Alice
```

Variables can also store numbers.

```lopo
define age = 20;
show(age);
```

Output

```
20
```

Variables may be reassigned later.

```lopo
define score = 10;

score = 25;

show(score);
```

Output

```
25
```

---

# 1.4 Numbers

Lopo supports integers and decimal numbers.

Integer

```lopo
define apples = 12;

show(apples);
```

Decimal

```lopo
define pi = 3.14159;

show(pi);
```

Numbers can be used in calculations.

```lopo
define a = 15;
define b = 5;

show(a + b);
show(a - b);
show(a * b);
show(a / b);
```

Output

```
20
10
75
3
```

---

# 1.5 Strings

Strings store text.

Use either double quotes or single quotes.

```lopo
define first = "Lopo";
define second = 'Language';

show(first);
show(second);
```

Output

```
Lopo
Language
```

Strings can be joined together.

```lopo
define first = "Hello";
define second = "World";

show(first + " " + second);
```

Output

```
Hello World
```

---

# 1.6 Booleans

A boolean has only two values.

- `true`
- `false`

```lopo
define isStudent = true;
define isOnline = false;

show(isStudent);
show(isOnline);
```

Output

```
true
false
```

Booleans are commonly used in conditions.

```lopo
define loggedIn = true;

if loggedIn {
    show("Welcome!");
}
```

---

# 1.7 null

`null` represents the absence of a value.

```lopo
define user = null;

show(user);
```

Output

```
null
```

Later, the variable can hold another value.

```lopo
define user = null;

user = "Alice";

show(user);
```

Output

```
Alice
```

---

# 1.8 Basic Calculations

Lopo supports the standard arithmetic operators.

| Operator | Meaning |
|----------|---------|
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `%` | Remainder |

Example

```lopo
define a = 20;
define b = 6;

show(a + b);
show(a - b);
show(a * b);
show(a / b);
show(a % b);
```

Output

```
26
14
120
3.3333333333333335
2
```

---

# Practice

Try writing the following programs yourself.

### Exercise 1

Print your name.

```lopo
show("Your Name");
```

---

### Exercise 2

Create a variable for your age.

```lopo
define age = 18;

show(age);
```

---

### Exercise 3

Calculate the area of a rectangle.

```lopo
define width = 12;
define height = 8;

define area = width * height;

show(area);
```

---

### Exercise 4

Join two strings.

```lopo
define first = "Lopo";
define second = "Book";

show(first + " " + second);
```

---

# Summary

In this chapter you learned how to:

- Print output with `show()`
- Write comments
- Create variables using `define`
- Store numbers
- Store strings
- Use `true`, `false`, and `null`
- Perform arithmetic calculations
