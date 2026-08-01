# NAND2Tetris HDL Solutions & Logic Explanations

> A collection of HDL implementations for the **NAND2Tetris** course along with the logic behind each chip to help students understand *how* and *why* each solution works.

---

## About

This repository contains my solutions for the **NAND2Tetris** course projects.

The purpose of this repository is **not only to provide working HDL implementations**, but also to explain the logic behind each chip so that beginners can understand the design process instead of simply copying the code.

As I progress through the course, I will continuously update this repository with:

-  HDL implementations
-  Logic explanations
-  Circuit design intuition
-  Notes and tips
-  Future project solutions

---

## Goals

- Help beginners understand NAND2Tetris HDL.
- Explain the reasoning behind every implementation.
- Provide clean and readable HDL code.
- Serve as a reference while studying the course.

---

# Repository Structure

```
.
├── Project1-Boolean_Logic
│   ├── And.hdl
│   ├── Or.hdl
│   ├── Not.hdl
│   ├── Xor.hdl
│   ├── mux.hdl
│   ├── dmux.hdl
│   ├── Not16.hdl
│   ├── Mux4Way16.hdl
│   └── Or8Way.hdl
│
├── Project2-Boolean_Arithmetic
│   ├── HalfAdder.hdl
│   └── FullAdder.hdl
│
└── README.md
```

---

# Completed Projects

## Project 1 – Boolean Logic

| Chip | Status | Description |
|------|:------:|-------------|
| Not | ✅ | Inverts a single bit |
| And | ✅ | Logical AND gate |
| Or | ✅ | Logical OR gate |
| Xor | ✅ | Exclusive OR gate |
| Mux | ✅ | 2-way Multiplexer |
| DMux | ✅ | 2-way Demultiplexer |
| Not16 | ✅ | 16-bit NOT |
| Mux4Way16 | ✅ | 4-way 16-bit Multiplexer |
| Or8Way | ✅ | OR across 8 inputs |

---

## Project 2 – Boolean Arithmetic

| Chip | Status | Description |
|------|:------:|-------------|
| HalfAdder | ✅ | Adds two bits |
| FullAdder | ✅ | Adds three bits (including carry) |

More chips will be added soon.

---

# Upcoming Projects

- [ ] Add16
- [ ] Inc16
- [ ] ALU
- [ ] Sequential Logic
- [ ] Memory
- [ ] CPU
- [ ] Computer
- [ ] Machine Language
- [ ] Assembler
- [ ] VM Translator
- [ ] Compiler
- [ ] Operating System

---

# Explanation Format( in progress )

Every chip will eventually include:

- Problem Statement
- Logic Used
- Truth Table (where applicable)
- Circuit Idea
- HDL Implementation
- Step-by-step Explanation
- Common Mistakes
- Time-saving Tips

Example:

```
Chip: HalfAdder

Inputs:
A
B

Outputs:
Sum
Carry

Logic:

Sum   = A XOR B
Carry = A AND B
```

This makes it easier to understand the implementation rather than memorizing the code.

---

# Requirements

- NAND2Tetris Hardware Simulator
- HDL files provided in the course

Download from the official NAND2Tetris website.

---

# How to Use

1. Clone the repository

```bash
git clone https://github.com/Skyu2231/NAND2Tetris-Hardware.git
```

2. Open the Hardware Simulator.

3. Load the required `.hdl` file.

4. Run the corresponding `.tst` file from the NAND2Tetris project.

5. Compare your implementation or study the logic provided.

---

# Learning Resources

- Official NAND2Tetris Course
- NAND2Tetris Book:
  *The Elements of Computing Systems*

---

# Note for Students

This repository is intended as a **learning resource**.

I strongly encourage you to:

- Try solving each project on your own first.
- Use this repository only after making your own attempt.
- Focus on understanding the logic instead of copying the implementation.

You'll learn much more that way.

---

# Contributions

Suggestions, improvements, and corrections are always welcome.

If you find:

- Better HDL implementations
- Simpler logic
- Bugs
- Typographical errors

Feel free to open an issue or submit a pull request.

---



# Progress

| Project | Status |
|----------|:------:|
| Boolean Logic |  Complete |
| Boolean Arithmetic |  In Progress |
| Sequential Logic |  Upcoming |
| Machine Language |  Upcoming |
| Computer Architecture |  Upcoming |
| Assembler |  Upcoming |
| VM Translator |  Upcoming |
| Compiler |  Upcoming |
| Operating System |  Upcoming |

---

## License

This repository is released under the MIT License.

---

### Lesss Go!!!