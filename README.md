 # Sky130 Day 1: Inception of Open-Source EDA, OpenLANE & Sky130 PDK  
📅 **Date:** April 3-4, 2025  

## SKY130_D1_SK1 - How to Talk to Computers

- Chips in embedded systems are packaged for easy mounting; **wire bonding** connects them to the board.
- Inside the chip:  
  - **I/O ring** → for pads  
  - **Core area** → main logic  
  - Both sit on the **die**

- **Foundries** make chips and offer **IP blocks**:  
  - *Soft macros* (RTL-based, flexible)  
  - *Hard macros* (pre-designed layout)

- **ISA (Instruction Set Architecture)**:  
  - Defines processor instructions  
  - Code flow: `C → ASM → Machine Code`

- **RTL code** models hardware to run the ISA and is used to design the chip before physical implementation.

---
🔧 Foundation of how software talks to silicon using open-source tools like OpenLANE and Sky130.
