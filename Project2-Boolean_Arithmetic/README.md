# Project 2 – Boolean Arithmetic

> **Navigation**
>
> **Home:** [System-Hardware](../README.md)  
> **Previous Project:** [Project 1 – Boolean Logic](../Project1-Boolean_Logic/README.md)  
> **Next Project:** [Project 3 – Sequential Logic](../Project3-Sequential_Logic/README.md)

---

# Overview

Project 2 builds upon the logic gates developed in **Project 1** to construct arithmetic circuits capable of performing binary computations.

Arithmetic operations in digital computers are implemented entirely using logic gates. This project introduces the fundamental building blocks required to perform binary addition and eventually construct the **Arithmetic Logic Unit (ALU)**, one of the most important components of a CPU.

---

# Learning Objectives

After completing this project, you should be able to:

- Understand binary addition.
- Design combinational arithmetic circuits.
- Learn carry propagation.
- Build larger circuits using smaller reusable components.
- Understand the architecture and functionality of an ALU.

---

# Chips Implemented

| Chip | Description | Status |
|-------|-------------|:------:|
| HalfAdder | Adds two binary bits | Complete |
| FullAdder | Adds three binary bits (including carry) | Complete |
| Add16 | Adds two 16-bit binary numbers | Complete |
| Inc16 | Increments a 16-bit value by one | Complete |
| ALU | Performs arithmetic and logical operations | Complete |

---

# Binary Arithmetic

Digital computers perform arithmetic using binary numbers.

```
Decimal : 0 1 2 3 4 5

Binary  : 0 1 10 11 100 101
```

Unlike decimal arithmetic, binary addition only involves two digits:

```
0

1
```

Whenever the sum exceeds **1**, a **Carry** is generated.

Example:

```
  1
+ 1
----
 10
```

This principle forms the basis of every arithmetic circuit.

---

# Chip Documentation

---

# Half Adder

## Theory

A Half Adder adds two single-bit binary inputs.

It produces:

- Sum
- Carry

### Boolean Expressions

```
Sum = A XOR B

Carry = A AND B
```

### HDL Design Idea

The Half Adder combines one XOR gate and one AND gate.

---

### Truth Table

> **Insert Truth Table Here**

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# Full Adder

## Theory

A Full Adder extends the Half Adder by including an additional **Carry-In** input.

Inputs:

- A
- B
- Carry-In

Outputs:

- Sum
- Carry-Out

This allows multiple adders to be connected together to perform multi-bit addition.

### Boolean Expressions

```
Sum = A XOR B XOR CarryIn

Carry = (A AND B)
      OR (CarryIn AND (A XOR B))
```

### HDL Design Idea

Constructed by connecting **two Half Adders** followed by an OR gate.

---

### Truth Table

> **Insert Truth Table Here**

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# Add16

## Theory

Add16 performs the addition of two **16-bit binary numbers**.

Instead of adding all bits simultaneously, the addition is carried out one bit at a time while propagating the carry to the next stage.

This architecture is known as a **Ripple Carry Adder**.

### HDL Design Idea

- Use one Half Adder for the least significant bit.
- Chain fifteen Full Adders.
- Carry propagates from the least significant bit to the most significant bit.

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# Inc16

## Theory

Inc16 increments a 16-bit binary number by **1**.

Mathematically,

```
Output = Input + 1
```

Incrementers are frequently used in processors for:

- Program Counters
- Memory Addresses
- Loop Counters

### HDL Design Idea

Implemented using the Add16 circuit by adding a constant value of one.

---

### Circuit Diagram

> **Insert Circuit Diagram Here**

---

# ALU (Arithmetic Logic Unit)

## Theory

The Arithmetic Logic Unit (ALU) is the computational core of the Hack CPU.

It performs both arithmetic and logical operations based on six control bits.

The ALU can:

- Zero an input
- Negate an input
- Perform bitwise AND
- Perform addition
- Negate the output
- Produce Zero and Negative status flags

Every arithmetic instruction executed by the CPU eventually passes through the ALU.

---

## ALU Control Bits

| Control Bit | Purpose |
|--------------|---------|
| zx | Zero the x input |
| nx | Negate x |
| zy | Zero the y input |
| ny | Negate y |
| f | Select AND or ADD |
| no | Negate output |

---

### HDL Design Idea

The ALU is constructed hierarchically using:

- Add16
- And16
- Mux16
- Not16
- Or8Way

Each control bit enables or disables specific operations, allowing a single circuit to perform multiple functions.

---

### ALU Architecture

> **Insert ALU Block Diagram Here**

---

### ALU Truth Table / Control Table

> **Insert ALU Control Table Here**

---

# Common Mistakes

- Forgetting to propagate the carry in Full Adders.
- Confusing Half Adders with Full Adders.
- Incorrect bit ordering in Add16.
- Misunderstanding the ALU control bits.
- Ignoring the Zero and Negative output flags.
- Mixing arithmetic addition with bitwise operations.

---

# Key Takeaways

By the end of this project, you will understand:

- Binary arithmetic
- Carry propagation
- Ripple Carry Adders
- Increment circuits
- Hierarchical chip design
- The architecture of the Hack ALU

These concepts prepare you for **Project 3 – Sequential Logic**, where memory elements such as registers, flip-flops, and counters are introduced.

---

# References

- *The Elements of Computing Systems* — Noam Nisan & Shimon Schocken
- NAND2Tetris Project 2 Documentation

---

# Navigation

**Home:** [System-Hardware](../README.md)

**Previous:** [Project 1 – Boolean Logic](../Project1-Boolean_Logic/README.md)

**Next:** [Project 3 – Sequential Logic](../Project3-Sequential_Logic/README.md)