# Project 1 – Boolean Logic

> **Navigation**
>
> **Home:** [System-Hardware](../README.md)  
> **Next Project:** [Project 2 – Boolean Arithmetic](../Project2-Boolean_Arithmetic/README.md)

---

# Overview

Boolean Logic forms the foundation of all digital computers.

In this project, the objective is to build a collection of basic logic gates using **Hardware Description Language (HDL)**. Every chip is ultimately constructed from the primitive **NAND** gate, demonstrating that NAND is a **Universal Gate**.

These basic chips will later be reused to build arithmetic circuits, memory elements, and eventually a complete computer.

---

# Learning Objectives

After completing this project, you should be able to:

- Understand Boolean Algebra
- Write HDL programs
- Build combinational logic circuits
- Design reusable hardware components
- Understand hierarchical chip design

---

# Chips Implemented

| Chip | Description | Status |
|-------|-------------|:------:|
| Not | Inverts a single input bit | Complete |
| And | Logical AND operation | Complete |
| Or | Logical OR operation | Complete |
| Xor | Exclusive OR operation | Complete |
| Mux | 2-way Multiplexer | Complete |
| DMux | 2-way Demultiplexer | Complete |
| Not16 | 16-bit NOT operation | Complete |
| Mux4Way16 | 4-way 16-bit Multiplexer | Complete |
| Or8Way | OR across eight inputs | Complete |

---

# Boolean Logic

Boolean Logic operates on only two values.

```
0 → LOW → FALSE

1 → HIGH → TRUE
```

Every digital circuit is constructed using combinations of logic gates that manipulate these binary values.

---

# Chip Documentation

---

# NOT Gate

## Theory

The NOT gate produces the complement of its input.

If the input is **0**, the output becomes **1**.

If the input is **1**, the output becomes **0**.

### Boolean Expression

```
OUT = ¬A
```

### HDL Design Idea

Constructed using a single NAND gate whose inputs are tied together.

---

### Truth Table

> **Insert Truth Table Here**

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# AND Gate

## Theory

The AND gate outputs **HIGH** only when **both inputs are HIGH**.

It is commonly used whenever multiple conditions must be satisfied simultaneously.

### Boolean Expression

```
OUT = A • B
```

### HDL Design Idea

Built by combining NAND and NOT gates.

---

### Truth Table

> **Insert Truth Table Here**

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# OR Gate

## Theory

The OR gate outputs HIGH whenever at least one input is HIGH.

### Boolean Expression

```
OUT = A + B
```

### HDL Design Idea

Implemented using De Morgan's Law together with NAND gates.

---

### Truth Table

> **Insert Truth Table Here**

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# XOR Gate

## Theory

The XOR gate outputs HIGH only when the two inputs are different.

This gate becomes one of the most important building blocks for arithmetic circuits, especially the Half Adder.

### Boolean Expression

```
OUT = A ⊕ B
```

### HDL Design Idea

Constructed by combining previously implemented gates.

---

### Truth Table

> **Insert Truth Table Here**

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# MUX (Multiplexer)

## Theory

A Multiplexer selects one of two input signals depending on the value of the selector bit.

```
sel = 0

Output = A

sel = 1

Output = B
```

### HDL Design Idea

The selector determines which input reaches the output using NOT, AND, and OR gates.

---

### Truth Table

> **Insert Truth Table Here**

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# DMUX (Demultiplexer)

## Theory

A Demultiplexer performs the opposite operation of a Multiplexer.

It routes one input to one of two outputs depending on the selector.

### HDL Design Idea

The selector controls which output receives the input signal.

---

### Truth Table

> **Insert Truth Table Here**

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# NOT16

## Theory

NOT16 extends the single-bit NOT gate to a 16-bit bus.

Each bit is independently inverted.

### HDL Design Idea

Use sixteen NOT gates operating in parallel.

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# MUX4Way16

## Theory

MUX4Way16 selects one of four 16-bit input buses.

Two selector bits determine which input is forwarded to the output.

### HDL Design Idea

Constructed hierarchically using multiple MUX chips.

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# OR8Way

## Theory

OR8Way computes the logical OR of eight separate inputs.

If any one of the eight inputs is HIGH, the output becomes HIGH.

### HDL Design Idea

Combine several OR gates in a tree structure until a single output remains.

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# Common Mistakes

- Confusing Multiplexer with Demultiplexer.
- Treating XOR the same as OR.
- Forgetting that selector bits determine routing.
- Mixing up the order of selector inputs in MUX4Way16.
- Not building chips hierarchically using previously implemented components.

---

# Key Takeaways

By the end of this project, you will have learned:

- Fundamental Boolean operations
- Combinational circuit design
- HDL syntax and chip construction
- Hierarchical hardware design
- The role of logic gates in building larger digital systems

These chips serve as the foundation for **Project 2 – Boolean Arithmetic**, where they are combined to build adders and, eventually, the Arithmetic Logic Unit (ALU).

---

# References

- *The Elements of Computing Systems* — Noam Nisan & Shimon Schocken
- NAND2Tetris Project 1 Documentation

---

# Navigation

**Previous:** [Home](../README.md)

**Next:** [Project 2 – Boolean Arithmetic](../Project2-Boolean_Arithmetic/README.md)