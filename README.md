<p align="center">
  <img src="lopo.png" width="320" alt="Lopo Programming Language"/>
</p>

<h1 align="center">Lopo — a tiny language for real projects</h1>

<p align="center">
  <a href="https://github.com/dominexmacedon-docs/lopo-docs/releases">
    <img src="https://img.shields.io/github/v/release/dominexmacedon-docs/lopo-docs?color=brightgreen&label=Release&style=for-the-badge" alt="Latest Release"/>
  </a>
  <a href="https://github.com/dominexmacedon-docs/lopo-docs">
    <img src="https://img.shields.io/badge/Docs-Premium-blueviolet?style=for-the-badge&logo=readthedocs" alt="Docs"/>
  </a>
  <a href="https://github.com/dominexmacedon-docs/lopo-docs">
    <img src="https://img.shields.io/badge/Repo-Premium%20Quality-gold?style=for-the-badge&logo=github" alt="Premium Repo"/>
  </a>
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/License-MIT-orange?style=for-the-badge" alt="License"/>
  </a>
</p>

---

## Why Lopo?

- **Learn fast** → Simple, readable syntax that’s friendly for beginners and productive for experienced developers.  
- **Embed & extend** → Built on Node.js, so integration patterns (worker threads, subprocess IPC, N-API) are straightforward.  
- **Practical** → Small footprint, fast startup, and features that let you build scripts, tools, or tiny apps quickly.  

> [!NOTE]
> **Syntax Flexibility:** Semicolons are optional! You do not strictly need to end your statements with a semicolon (`;`). The parser will gracefully evaluate statements split by standard newlines.

---

## Quick Links
- [Releases](https://github.com/dominexmacedon-docs/lopo-docs/releases)  
- [Docs & Examples](https://github.com/dominexmacedon-docs/lopo-docs)  
- [License: MIT](https://opensource.org/licenses/MIT)  

---

## Features
- Clean, easy-to-read syntax  
- Lightweight interpreter with fast startup  
- Variables, expressions, conditionals, loops, functions  
- Entities (OOP-style objects), arrays, objects  
- Built-in utility functions and modular design  
- Command-line interface and native Windows editor with syntax highlighting  
- Designed to be embeddable and interoperable with Node.js ecosystems  

---

## Try Lopo in 60 Seconds

1. **Download the installer** [Lopo v1.0.1 Installer](https://github.com/dominexmacedon-docs/lopo-docs/releases/download/Lopo-v1.0.1/Lopo-v1.0.1.exe)  

2. **Install and verify** ```bash
   lopo --v

```

3. **Create hello.lopo** ```lopo
# Both syntax structures are perfectly valid:


show("Hello, Lopo!")
show("Hello, Lopo!");
