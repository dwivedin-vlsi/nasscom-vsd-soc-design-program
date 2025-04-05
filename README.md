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
## 🧪 LAB: SKY130_D1_SK3 - Get Familiar with Open-Source EDA Tools

### 📁 Directory Structure
All OpenLane runs must happen from the following directory:
```bash
~/Desktop/work/tools/openlane_working_dir/openlane
```
## To open the openlane instance:
#### Step 1: Start Docker
docker

#### Step 2: Run OpenLane in interactive mode
./flow.tcl -interactive

#### Step 3: Load OpenLane 0.9
package require openlane 0.9

#### Step 4: Prepare picorv32a design
prep -design picorv32a

![VirtualBox_vsdworkshop_02_04_2025_17_13_33](https://github.com/user-attachments/assets/e58234b9-39ec-4f24-972e-339d83fd2ba8)


- after this runs dir will be created in the designs/picorv32a folder
- inside the run directory the folders will be created as the runs are done
- there is one config.tcl which is diffrent from the other config file discussed before, this one shows which default parameters are being taken bt=y the runs
### 🛠️ Running Synthesis

To run synthesis (using Yosys and ABC logic synthesis):

```bash
run_synthesis
# Runs synthesis and logic optimization using ABC
```
-  after the run we can check the run dir for the results, logs and reports. results folder must have the synthesized netlsit reports folder will have all the reports for synthesis step and logs will store all the run logs for synthesis. In the reports chronologically latest report is most accurate.
 ### 📊 DFF (Flip-Flop) Ratio Calculation
-  At this step we need to do DFF ratio calculation as follows:
-       **Formula:** FlipFlop Ratio = Number of D Flip-Flops / Total Number of Cells     Percentage of DFFs = FlipFlop Ratio × 100
