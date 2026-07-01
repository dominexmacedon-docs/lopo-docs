# Chapter 2 — Input & Output

In the previous chapter, you learned how to display text using `show()`. In this chapter, you'll learn how to interact with users by receiving input from the keyboard using `ask()`.

By the end of this chapter, you'll be able to:

* Display messages with `show()`
* Read user input with `ask()`
* Build a simple calculator
* Check a user's age
* Convert temperatures between Celsius and Fahrenheit

---

# Syntax Highlighting

The examples in this chapter use the official Lopo CodeMirror color scheme.

| Token           | Color                                         | Example                |
| --------------- | --------------------------------------------- | ---------------------- |
| **Keyword**     | <span style="color:#4ea5ff">Blue</span>       | `define`, `if`, `show` |
| **String**      | <span style="color:#22c55e">Green</span>      | `"Hello"`              |
| **Number**      | <span style="color:#f59e0b">Orange</span>     | `25`, `3.14`           |
| **Comment**     | <span style="color:#7f848e">Gray</span>       | `# comment`            |
| **Variable**    | <span style="color:#e5e7eb">White</span>      | `name`, `age`          |
| **Function**    | <span style="color:#a78bfa">Purple</span>     | `show()`, `ask()`      |
| **Operator**    | <span style="color:#f43f5e">Red</span>        | `+`, `-`, `*`, `/`     |
| **Brackets**    | <span style="color:#38bdf8">Cyan</span>       | `() [] {}`             |
| **Punctuation** | <span style="color:#94a3b8">Light Gray</span> | `; , . :`              |

---

# 2.1 Using `show()`

The `show()` function displays information on the console.

```lopo
show("Welcome to Lopo!");
```

Output

```
Welcome to Lopo!
```

You can display numbers.

```lopo
show(100);
show(3.14);
```

Output

```
100
3.14
```

You can also display variables.

```lopo
define language = "Lopo";

show(language);
```

Output

```
Lopo
```

---

# 2.2 Using `ask()`

The `ask()` function waits for the user to enter a value.

```lopo
define name = ask("What is your name? ");

show("Hello " + name);
```

Example

```
What is your name? Alice

Hello Alice
```

The value returned by `ask()` is a string.

If you need a number, convert it using `num()`.

```lopo
define age = num(ask("Age: "));

show(age);
```

---

# 2.3 Simple Calculator

Let's build a calculator that adds two numbers.

```lopo
define first = num(ask("First number: "));
define second = num(ask("Second number: "));

define result = first + second;

show("Result = " + str(result));
```

Example

```
First number: 15
Second number: 25

Result = 40
```

You can replace `+` with other operators.

| Operator | Description    |
| -------- | -------------- |
| `+`      | Addition       |
| `-`      | Subtraction    |
| `*`      | Multiplication |
| `/`      | Division       |
| `%`      | Remainder      |

---

# 2.4 Age Checker

This example asks for the user's age and prints a message.

```lopo
define age = num(ask("Enter your age: "));

if age >= 18 {
    show("You are an adult.");
}
else {
    show("You are a minor.");
}
```

Example

```
Enter your age: 20

You are an adult.
```

Another example

```
Enter your age: 14

You are a minor.
```

---

# 2.5 Temperature Converter

This program converts Celsius to Fahrenheit.

Formula

```
F = (C × 9 / 5) + 32
```

```lopo
define celsius = num(ask("Temperature in Celsius: "));

define fahrenheit = (celsius * 9 / 5) + 32;

show("Fahrenheit = " + str(fahrenheit));
```

Example

```
Temperature in Celsius: 25

Fahrenheit = 77
```

---

# Practice

### Exercise 1

Ask the user's name and greet them.

```lopo
define name = ask("Name: ");

show("Hello " + name);
```

---

### Exercise 2

Ask for two numbers and multiply them.

```lopo
define a = num(ask("First number: "));
define b = num(ask("Second number: "));

show(str(a * b));
```

---

### Exercise 3

Calculate the area of a rectangle using user input.

```lopo
define width = num(ask("Width: "));
define height = num(ask("Height: "));

define area = width * height;

show("Area = " + str(area));
```

---

### Exercise 4

Ask the user's first and last name.

```lopo
define first = ask("First name: ");
define last = ask("Last name: ");

show("Welcome " + first + " " + last);
```

---

# Challenge

Write a program that asks the user for:

* Product name
* Price
* Quantity

Then calculate and display the total price.

Example

```
Product: Apple
Price: 120
Quantity: 3

Total = 360
```

---

# Summary

In this chapter you learned how to:

* Display output using `show()`
* Read keyboard input using `ask()`
* Convert text input to numbers using `num()`
* Convert values to strings using `str()`
* Build simple interactive programs
* Create a calculator
* Check a user's age
* Convert temperatures
