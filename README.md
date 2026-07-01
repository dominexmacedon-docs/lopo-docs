<p align="center">
  <img src="lopo.png" width="320" alt="Lopo Programming Language"/>
</p>

<h1 align="center">Lopo Programming Language</h1>

<p align="center">
A lightweight, interpreted programming language focused on simplicity, readability, and productivity.
</p>

---

# Introduction

Lopo is a modern interpreted programming language designed to make programming approachable while remaining powerful enough for real-world applications.

Its syntax is intentionally clean and expressive, allowing developers to write readable code with minimal boilerplate. Whether you are learning programming for the first time or building small utilities and applications, Lopo provides a straightforward development experience.

To complement the language, **Lopo Editor** offers a dedicated editing environment with syntax highlighting, tabs, and native support for `.lopo` files.

---

# Features

* Clean and beginner-friendly syntax
* Lightweight interpreter
* Variables and expressions
* Conditional statements
* Loops
* Functions
* Entities (object-oriented programming)
* Arrays and objects
* Built-in utility functions
* Modular design
* Command-line interface
* Native Windows editor
* Syntax highlighting
* Multiple document tabs
* Fast startup

---

# Hello World

```lopo
show("Hello World!");
```

---

# Installing Lopo

Download and install the Lopo language:

**Language Installer**

https://github.com/dominexmacedon-docs/lopo-docs/releases/download/lopo-v1.0.0/Lopo-v1.0.0.exe

The installer automatically:

* Installs the Lopo interpreter
* Registers the `lopo` command
* Adds Lopo to the Windows PATH
* Associates the `.lopo` file extension
* Enables running Lopo programs from Command Prompt

After installation, verify it by opening Command Prompt and running:

```bash
lopo
```

---

# Installing Lopo Editor

Download the official editor:

**Lopo Editor Installer**

https://github.com/dominexmacedon-docs/lopo-docs/releases/download/lopo-editor-v1.0.0/LopoEditor-installer.exe

Lopo Editor includes:

* Native desktop application
* Syntax highlighting
* Multiple editor tabs
* Open and save `.lopo` files
* Create new Lopo programs
* Run the currently opened program directly
* Right-click "Edit with Lopo" integration (when enabled)

The editor is designed specifically for developing Lopo applications.

---

# Writing Your First Program

Create a file named:

```text
hello.lopo
```

Example:

```lopo
define language = "Lopo";

show("Welcome to " + language + "!");
```

Run it from Command Prompt:

```bash
lopo hello.lopo
```

Or open it directly in **Lopo Editor**.

---

# Example

```lopo
entity Person {

    init(name, age) {

        self.name = name;
        self.age = age;

    }

    greet() {

        show("Hello " + self.name);

    }

}

define person = new Person("Alice", 20);

person.greet();
```

---

# Why Choose Lopo?

Lopo aims to provide an enjoyable programming experience by balancing simplicity and functionality.

It is suitable for:

* Students
* Beginners learning programming
* Educational environments
* Rapid scripting
* Small applications
* Language experimentation

Its readable syntax makes programs easy to understand while still supporting practical programming concepts such as entities, functions, collections, and reusable modules.

---

# Documentation

Complete documentation, examples, tutorials, release notes, and source code are available here:

https://github.com/dominexmacedon-docs/lopo-docs

---

# System Requirements

* Windows 10 or later
* Approximately 100 MB of free disk space
* Command Prompt or Windows Terminal (for CLI usage)

---

# Version

Current Release

* Lopo Programming Language v1.0.0
* Lopo Editor v1.0.0

---

# License

MIT License

Copyright © Dominex Macedon. All rights reserved.
