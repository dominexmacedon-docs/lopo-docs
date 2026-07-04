# Installation Guide for Lopo

This document explains how to install and run **Lopo**, the lightweight interpreted programming language built on Node.js.

---

## Prerequisites
- **Operating System:** Windows, macOS, or Linux
- **Node.js:** Version 16 or higher
- **Git:** For cloning the repository (optional if downloading ZIP)

---

## Installing the Lopo Editor (Windows)
1. Download the latest release from the [Releases page](../../releases).
2. Locate the installer file:  
   `Lopo-v1.0.0.exe`
3. Run the installer and follow the on‑screen instructions.
4. Once installed, launch the **Lopo Editor** from your Start Menu.
5. The editor includes syntax highlighting and a built‑in runner.

---

## Installing from Source
1. Clone the repository:
   ```bash
   git clone https://github.com/dominexmacedon-docs/lopo-docs.git
   cd lopo-docs
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the interpreter:
   ```bash
   lopo
   ```
4. Test with an example:
   ```bash
   lopo examples/hello.lopo
   ```

---

## Verifying Installation
- Run `lopo -v` to check the interpreter version.
- Open the editor and run a sample program to confirm everything works.

---

## Troubleshooting
- **Node.js not found:** Ensure Node.js is installed and added to your PATH.
- **Permission issues (Linux/macOS):** Use `chmod +x` on the installer or run with `sudo`.
- **Editor crashes:** Delete config files in `~/.lopo` and restart.

---

## Next Steps
- Read the `[Looks like the result wasn't safe to show. Let's switch things up and try something else!]` for writing your first Lopo program.
- Explore the `examples/` directory for sample code.
- Join discussions via Issues to share feedback or request features.
