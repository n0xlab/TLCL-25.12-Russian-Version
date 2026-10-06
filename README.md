# The Linux Command Line — Russian Translation

<p align="center">
  <img src="https://img.shields.io/badge/Author-William%20Shotts-blue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Edition-25.12-orange?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Language-Russian-d62828?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Shell-Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white"/>
  <img src="https://img.shields.io/badge/License-CC%20BY--NC--ND-16a34a?style=for-the-badge&logo=creativecommons"/>
</p>

> **The Linux Command Line** by William Shotts teaches not a set of magic spells, but a way of thinking in the shell. It takes you from the first `$` prompt to complete Bash scripts: files and directories, permissions, processes, redirection, regular expressions, text processing and shell programming. No GUI and no "magic" recipes — only what works on any Linux and UNIX system.

This repository contains an unofficial, non-commercial Russian translation of edition 25.12 (`TLCL-25.12-ru-book.pdf`).

---

## What Makes This Book Different

- **Concepts, not commands** — you understand *why* a pipeline works instead of memorizing it
- **One continuous story** — chapters build strictly on each other, from `cd` to `for` loops
- **Standard tools only** — Bash and GNU coreutils, nothing exotic
- **Focus on Bash** — the default shell on almost every distribution
- **A full scripting part** — more than a dozen chapters on shell programming
- **Practical examples** — real administration tasks instead of synthetic exercises
- **Free to share** — the online edition is available as a free PDF
- **Up to date** — the text is checked against modern distributions and tool versions

---

## Book Structure

```
The Linux Command Line (edition 25.12)
│
├── Part 1. Learning the Shell
│   ├── 01. What Is the Shell?
│   ├── 02. Navigation
│   ├── 03. Exploring the System
│   ├── 04. Manipulating Files and Directories
│   ├── 05. Working with Commands
│   ├── 06. Redirection
│   ├── 07. Seeing the World as the Shell Sees It (expansion)
│   ├── 08. Advanced Keyboard Tricks
│   ├── 09. Permissions
│   └── 10. Processes
│
├── Part 2. Configuration and the Environment
│   ├── 11. The Environment
│   ├── 12. A Gentle Introduction to vi
│   └── 13. Customizing the Prompt
│
├── Part 3. Common Tasks and Essential Tools
│   ├── 14. Package Management
│   ├── 15. Storage Media
│   ├── 16. Networking
│   ├── 17. Searching for Files
│   ├── 18. Archiving and Backup
│   ├── 19. Regular Expressions
│   ├── 20. Text Processing
│   ├── 21. Formatting Output
│   ├── 22. Printing
│   └── 23. Compiling Programs
│
└── Part 4. Writing Shell Scripts
    ├── 24. Writing Your First Script
    ├── 25. Starting a Project
    ├── 26. Top-Down Design
    ├── 27. Flow Control: Branching with if
    ├── 28. Reading Keyboard Input
    ├── 29. Flow Control: Looping with while / until
    ├── 30. Troubleshooting
    ├── 31. Flow Control: Branching with case
    ├── 32. Positional Parameters
    ├── 33. Flow Control: Looping with for
    ├── 34. Strings and Numbers
    ├── 35. Arrays
    └── 36. Exotica
```

---

## Requirements

```
Any Linux distribution  (Ubuntu, Debian, Fedora, Arch — any will do)
Bash 4.x or newer
A terminal
About an hour a day and the will to type by hand
```

Check your shell:

```bash
echo $SHELL && bash --version
```

> **Tip:** No Linux at hand? WSL2 on Windows, macOS (keep the BSD utilities in mind) or an Ubuntu virtual machine will do.

---

## Quick Start

### 1. Open a terminal

```bash
# Ubuntu / GNOME
Ctrl + Alt + T
```

### 2. Make sure the shell responds

```bash
whoami && pwd && date
```

### 3. Create a sandbox for experiments

```bash
mkdir -p ~/tlcl/playground && cd ~/tlcl/playground
```

### 4. Try the first chapter right now

```bash
# list the directory contents
ls -l
# go to another directory
cd /usr/share
# go back
cd -
# find out the file type
file /bin/bash
# help for a shell builtin
help cd
# full manual for a program
man ls
```

### 5. Exit

```bash
exit
```

---

## How to Read

```
Read the chapters in order — the book builds step by step
              ↓
Type every command from the text into the terminal yourself
              ↓
Don't copy and paste: muscle memory is part of learning
              ↓
Break and rebuild the ~/tlcl/playground sandbox
              ↓
After each chapter, read man for two or three new commands
              ↓
Start Part 4 only after finishing Parts 1–3
```

---

## Key Tools by Topic

| Topic | Commands and tools |
|---|---|
| **Navigation** | `pwd`, `cd`, `ls` |
| **Files and directories** | `cp`, `mv`, `rm`, `mkdir`, `ln` |
| **Viewing files** | `cat`, `less`, `head`, `tail`, `file` |
| **Redirection** | `>`, `>>`, `<`, `\|`, `tee` |
| **Expansion** | `*`, `?`, `{}`, `$(...)`, quoting and escaping |
| **Permissions** | `chmod`, `chown`, `umask`, `su`, `sudo` |
| **Processes** | `ps`, `top`, `jobs`, `bg`, `fg`, `kill` |
| **Environment** | `printenv`, `set`, `alias`, `export`, `.bashrc` |
| **Searching** | `locate`, `find`, `xargs` |
| **Regular expressions** | `grep`, metacharacters, POSIX character classes |
| **Text processing** | `sort`, `uniq`, `cut`, `paste`, `join`, `tr`, `sed` |
| **Archiving** | `tar`, `gzip`, `bzip2`, `zip`, `rsync` |
| **Networking** | `ping`, `traceroute`, `ip`, `ssh`, `scp`, `sftp`, `curl`, `wget` |
| **Storage media** | `mount`, `umount`, `fdisk`, `mkfs`, `dd`, `df`, `du` |
| **Scripting** | `#!/bin/bash`, `if`, `case`, `while`, `until`, `for`, functions, arrays |

---

## What Part 4 Teaches

| Technique | Why |
|---|---|
| **Shebang and execute permission** | Turn a text file into a program |
| **Top-down design** | Split a task into functions instead of one long wall of code |
| **`if` and `[[ ]]`** | Test conditions, files and strings without surprises |
| **`read`** | Take input from the user and validate it |
| **`while` / `until`** | Process streams and files line by line |
| **`trap`, `set -u`, `set -x`** | Exit cleanly and track down bugs |
| **`case`** | Handle menus and options instead of an `elif` ladder |
| **Positional parameters, `getopts`** | Give scripts a proper command-line interface |
| **Arithmetic and `printf`** | Calculate and print results readably |
| **Arrays** | Store sets of values instead of gluing strings together |

---

## Important Warnings

```bash
# never
rm -rf /
# check of= three times first
dd if=... of=/dev/sda
# won't "fix" anything — it will break the system
chmod -R 777 /
```

Practice all destructive operations in a virtual machine or a sandbox directory. In Linux, `rm` does not ask for confirmation and there is no Recycle Bin.

---

## Resources

- Official book site and free PDFs: **linuxcommand.org**
- `man bash` — the complete shell reference
- `info coreutils` — GNU core utilities documentation
- GNU Bash manual: **gnu.org/software/bash/manual**

---

## License

The online edition is distributed under the **Creative Commons Attribution-NonCommercial-NoDerivatives** license (CC BY-NC-ND): free copying and sharing, without changes and without commercial use. Copyright © William Shotts. The print edition is published by No Starch Press; the Russian print edition is published separately by the holder of the translation rights.

---

## Colophon

<p align="center">
  <img src="https://img.shields.io/badge/2%20Timothy-3%3A16--17-6b4f2a?style=for-the-badge"/>
</p>

<blockquote align="center">
  <p><em>All scripture is given by inspiration of God, and is profitable for doctrine,<br/>
  for reproof, for correction, for instruction in righteousness:<br/>
  That the man of God may be perfect,<br/>
  throughly furnished unto all good works.</em></p>
  <p><strong>— 2 Timothy 3:16–17</strong><br/>
  <sub>King James Version</sub></p>
</blockquote>
