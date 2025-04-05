# NASSCOM_VSD_SOC_DESIGN_PROGRAM  
🔧 *Open-source RTL to GDSII Implementation using OpenLane*

---

## 🗓️ Sky130 Day 1: Inception of Open-Source EDA, OpenLANE, and Sky130 PDK  
**Date:** March 26–27, 2025  

---

### 🌐 SKY130_D1_SK1 - How to Talk to Computers

- Embedded systems use **chips** placed in **packages** for easy handling and mounting.
- **Wire bonding** is a common packaging method to connect the chip to the board.
- Inside the chip:  
  - **I/O ring** – for I/O pads  
  - **Core area** – for logic  
  - Both sit on the **die**
- **Foundries** manufacture chips and may provide IPs:
  - *Soft macros* (flexible RTL-based)
  - *Hard macros* (fixed layouts)
- **ISA (Instruction Set Architecture)**:  
  Defines processor instructions.  
  **Flow:** `C code → ASM → Machine Code`
- **RTL (Register Transfer Level)** models hardware that executes the ISA.

---

### 🧩 SKY130_D1_SK2 - SoC Design and OpenLANE

- Open-source ASIC design requires:
  - RTL Designs  
  - EDA Tools  
  - PDK Data  
- OpenLane integrates these tools to implement the ASIC design flow:

#### 📈 RTL to GDSII Flow
1. **Synthesis** – Converts RTL to gate-level netlist using PDK library  
2. **Floorplan & Powerplan** – Defines die size, pin placement, and power  
3. **Placement** – Places standard cells  
4. **CTS (Clock Tree Synthesis)** – Distributes clock to sequential elements  
5. **Routing** – Connects all signals  
6. **Signoff** – Final checks (DRC, LVS, Timing); generates GDSII

---

### 🧪 LAB: SKY130_D1_SK3 - Using OpenLane

**Navigate to:**  
```bash
~/Desktop/work/tools/openlane_working_dir/openlane
