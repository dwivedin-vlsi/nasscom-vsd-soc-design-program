# Sky130 Day 1 - Introduction to Open-Source EDA, OpenLANE, and Sky130 PDK  

📅 **Date:** April 1 , 2025 - April 2, 2025  

## SKY130_D1_SK1 - Understanding How Computers Work  

Every embedded system contains **chips** that perform various tasks. These chips are placed inside a **package**, which makes them easier to handle and mount onto a circuit board.  

To connect the chip with other components, different packaging methods are used. One common method is **Wire Bonding**, where tiny wires connect the chip’s pads to external circuits.  

### 🔍 Inside the Chip  
- **I/O Ring**: Where input/output pads are placed.  
- **Core Area**: Contains the main logic of the chip.  
- **Die Area**: The actual silicon part of the chip, which holds the I/O ring and core area.  

### 🏭 Chip Manufacturing & IPs  
A **foundry** (chip manufacturer) produces these chips and can also provide **IP blocks** (pre-designed components) that designers can use in their circuits. These IPs can be:  
- **Soft macros** – Customizable, written in RTL code.  
- **Hard macros** – Pre-designed, fixed layouts.  

### ⚙️ Understanding ISA (Instruction Set Architecture)  
The **Instruction Set Architecture (ISA)** is the set of machine instructions a processor understands. Before a program runs on hardware, it goes through several steps:  
1. **C code** (written by programmers).  
2. **Compiler** converts C code into **Assembly (ASM) code**.  
3. **Assembler** translates ASM code into **machine code** (binary format).  

### 💡 Role of RTL Code  
In chip design, we use **RTL (Register Transfer Level) code** (written in Verilog or VHDL) to describe how the hardware will execute the ISA. This RTL code is later converted into an actual physical chip through a process called **synthesis**.  

This is the foundation of how software interacts with hardware in embedded systems! 🚀  
