
# 🏗️ Multicycle RISC-V Processor in Verilog (ECE 154A Final Project)

This project implements a multicycle RISC-V CPU using Verilog HDL, dividing instruction execution across multiple clock cycles for improved hardware efficiency. The design separates control and datapath logic, with a finite state machine (FSM) managing sequential operations. It is developed as part of UCSB’s ECE 154A course on computer architecture.

## 🧠 Features

- Supports core RISC-V base integer instructions (RV32I)
- Multicycle control: fetch, decode, execute, memory, and write-back phases
- Control FSM implemented using Moore machine principles
- Parametrized datapath with mux-controlled ALU inputs
- Uses program counter enable (PCEn), address source mux, and write-back logic
- Read/Write signals issued only in correct states to shared memory

## 📁 File Structure

| File Name                     | Description                                    |
|-------------------------------|------------------------------------------------|
| `ucsbece154a_datapath (1).v`  | Datapath module with control signal decoding   |
| `ucsbece154a_controller (1).v`| FSM-based controller generating sequenced control signals |

## 🛠 How to Simulate

1. Use ModelSim, Vivado, or Verilator to compile both files.
2. Connect a testbench with instruction memory and register file.
3. Track cycle-by-cycle behavior to validate:
   - State transitions (IF, ID, EX, MEM, WB)
   - ALU result flow
   - Control signal timing
   - Correct memory and register access

## 📦 Requirements

- Verilog HDL simulator (ModelSim, Verilator, etc.)
- GTKWave or waveform viewer (optional)
- Understanding of RISC-V datapath and FSM design

## 👤 Author

Yiguang Zhu — ECE 154A Multicycle CPU Project (2024)
