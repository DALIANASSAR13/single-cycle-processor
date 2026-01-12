# Single-Cycle RISC-V Processor – CPU Design Project

A fully functional **Single-Cycle RISC-V Processor** implemented in **Verilog**, designed to execute a subset of RISC-V instructions in a single clock cycle. This project provides hands-on experience with CPU architecture, digital logic design, Verilog HDL, and hardware simulation using **Vivado**.

---

## 🔹 Project Overview

This project simulates a complete single-cycle CPU, helping students understand how a processor executes instructions internally—from fetching and decoding to arithmetic/logic execution and memory operations. The design merges the **ALU Control Unit** with the **Main Control Unit** to streamline control logic.

Key highlights:

* Execute RISC-V instructions including arithmetic, logic, shifts, memory access, and branching.
* Full single-cycle datapath with integrated modules.
* Simulation and verification of instruction execution using Vivado.
* Hands-on experience with modular Verilog design and testbench creation.
* Professional documentation in IEEE-style format.

---

## 🔹 Features

### Core Functionality

* **Instruction Execution**
  Supports R-Type, I-Type, memory access, shift, and branch instructions such as `add`, `sub`, `addi`, `slli`, `ld`, `sd`, and `beq`.

* **Single-Cycle Datapath**
  Fetch, decode, execute, memory access, and write-back occur in one clock cycle per instruction.

* **Register File**
  32 registers with two read ports, one write port, and x0 hardwired to 0.

* **Immediate Generator**
  Extracts and sign-extends immediates for arithmetic, shift, memory, and branch instructions.

* **ALU**
  Handles arithmetic and logic operations including addition, subtraction, AND, OR, XOR, and logical shifts.

* **Control Unit**
  Generates all control signals (RegWrite, MemWrite, MemRead, ALUSrc, MemToReg, Branch) and merged ALU control.

* **Memory Modules**
  Instruction memory preloaded with machine code; data memory supports 64-bit loads and stores.

* **Branch Logic & PC Update**
  Correctly calculates next instruction address based on branch decisions.

---

### Optional Stretch Features (For Advanced Testing)

* Run custom RISC-V programs in the simulator.
* Generate waveform outputs to visualize PC, ALU, and memory operations.
* Support for larger memory or additional RISC-V instruction types.

---

## 🔹 Technical Details

### Project Setup

* Implemented entirely in **Verilog HDL**.
* Simulated using **Vivado Design Suite**.
* Instruction memory initialized with machine code generated from a RISC-V assembler.

### Components

* **ALU** – Arithmetic and logic operations.
* **Control Unit** – Merged main and ALU control.
* **Register File & Immediate Generator** – Storage and immediate extraction.
* **PC & Branch Logic** – Instruction sequencing and branching.
* **Instruction & Data Memory** – Preloaded and word-aligned memories.
* **CPU Top-Level Module** – Integrates all components and connects internal signals.

### State Management & Verification

* Testbenches verify correct module behavior individually and as an integrated CPU.
* Simulation captures PC updates, instruction execution, ALU outputs, memory reads/writes, and branching decisions.

---

## 🔹 Installation & Setup

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/single-cycle-riscv-processor.git
   cd single-cycle-riscv-processor
   ```

2. **Open project in Vivado**:

   Import all Verilog files and create a simulation project.

3. **Run simulation**:

   * Run each module's testbench (ALU, Control Unit, Register File, etc.)
   * Run the top-level CPU testbench with machine code instructions.

4. **Analyze waveforms**:

   Verify instruction execution, ALU results, memory operations, and PC updates.

---


