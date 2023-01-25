# 2023 Intel IPG CKT Training

## Table of Contents
<a href="#one">Day 1 - Fundamentals of VLSI Design and Overview of Sand-to-Silicon</a>
<br>
<a href="#two">Day 2 - Details of IC Manufacturing Process</a>
<br>

<a name="user-content-one"></a>
### Day 1 - Fundamentals of VLSI Design and Overview of Sand-to-Silicon

<details>
<summary>Theory</summary>
<br>
  
1. **VLSI Circuit Design Course Details**

| Digital Logic Design                | Electric Circuit Design                                        | Semiconductor Devices                     |
| ------------------------------------|:--------------------------------------------------------------:| -----------------------------------------:|
| Logic gates                         | Resistor, capacitor, inductor, voltage source & current source | Conductor, semicondictor & insulator      |
| Truth table and K-Map               | Charge, current, voltage, power, & energy                      | Silicon & Germanium                       |
| Combinational Lofic Circuit         | KCL & KVL                                                      | Drift & Diffusion                         |
| Mux and Decoder based logic designs | Mesh and Nodal Analysis                                        | Intrinsic and Extrinsic Semiconductor     |
| Sequential Logic Circuits           | Circuit Theorem: Superposition, Thevenin's                     | Semiconductor Diode, BJT & MOSFET         |
| Logic states                        | RC circuits and Transients                                     | Operation, Characteristics & Band Diagram |
| Timing Diagrams                     | Assignment                                                     | Assignment                                |
| Assignment
<br>
  
2. **Overview of VLSI Design**

**Wafer and Die**
- Wafer diameter is approximate 12 inch (~300mm)
- Single wafer contails ~10k die.
- General die size is 1mm x 1mm or 2mm x 2mm
- All eletric components fabricated on each and every single die.

![image](https://user-images.githubusercontent.com/121998024/211214116-faea14d9-052b-405f-ad9e-f4420f40e5ec.png)

**Packaged Chip**
- Central part of the chip is called die.
- Types of packaging are
  - SIP (Syatem in Packages)
  - DIP (Dual-in-Line Package)
  - QFN (Quad Flat No-Lead Package)
  - BGA (Ball Grid Array)

![image](https://user-images.githubusercontent.com/121998024/211214479-6a1c246d-f587-4969-a005-638e460e7bd8.png)

**Inside the Die**
<br>
![image](https://user-images.githubusercontent.com/121998024/211214585-0118cfb3-8977-467d-8853-54786fa3694f.png)

- **Memory and Memory Controller**:
  - Static Random Access Memory (SRAM) and SRAM controller
  
- **Digital**:
  - Made up of gates, muxes, decoders, counters, resistors, FSM, & etc...
  - All are made by standard cells and deigned by using semicustom VLSI design flow.

- **Analog & RF**:
  - Consists of:
    - Clock component (VCO and PLL)
    - Reference and registered voltage (Bandgap reference, LDO, DC-DC converter)
    - Data component (PRBS generator)
    - Amplifiers & Filters
    - Interfaces (ADC & DAC)
  - All are made and designed by custom VLSI design flow.
 <br>

3. **VLSI Design Methodology**
  
**Field Programming Gate Array (FPGA) Based Design**
  - Faster prototyping and cost-saving
  - FPGA chip consists of:
    - Input/output buffers
    - Array of configurable logic blocks (CLBs)
    - Programmable interconnect structures
  - The programming of interconnects is achieved by programming of RAM
  - Signal routing between the CLBs and the I/O blocks established by configurable switching matrices

![image](https://user-images.githubusercontent.com/121998024/211215820-e6b756cf-1b84-4ce0-b78f-fa22a2bc5551.png)

ASIC (Application Specific Integrated Circuit)  
**Standard Cell Based Design** (aka Semi Custom Design)
  - Develop a standard cell library which storing all the developed, characterized logic cells.
  - The height of all cells are always constant for a particular technology (eg: 14nm, 7nm technology)
  - Each cell is characterized according to several different categories, for example:
    - Delay time vs load capacitance and input transition
    - Circuit simulation model, Timing simulation model, Fault simulation model
    - Cell data for place-and route
    - Mask data

**Full Custom Design**
  - No library is using.
  - Designers has to take care of the geometry, orientation, & placement of every transistors in a full-custom layouts. Causing low profuctivity issue.
  - High development cost hence, rarely use in digital VLSI design.
  - All the analog and RF designs are full custom design.
<br>

4. **VLSI Design Quality**

**Testability**
  - Generation of good test vector.
  - Availability of good test fixture at speed.
  - Design of testable chip.
  
**Yield and Manufacturability**
  - Yield: No. of tested ok chips/Total no. of Chips
  - Functional Yield: Checks at lower speed.
  - Parametric Yield: Checks at required speed.

**Reliability**
  - ESD and EOS
  - Electromigration
  - Oxide breakdown
  - Power and ground bouncing
  - On-chip noise and cross-talk
  
**Technology Upgradability**
  - Design style should be chosen such that the technology update of the chip of functional module for design reuse can be achieved quickly with minimal cost.
<br>

5. **Types of Package**
  
**Pin-through-hole (PTH)**
  - Drill holes in PCB, high cost in soldering process.

![image](https://user-images.githubusercontent.com/121998024/211217332-e14672dc-a8eb-4b9e-a158-adb58bf94142.png)

**Surface Mount Technology (SMT)**
  - Solder the die directly on the PCB, cost and space saving,but expensive tools needed for soldering.
  
![image](https://user-images.githubusercontent.com/121998024/211217392-0a8c4590-da08-4486-83f3-cd6635968227.png)

**Plastic**
  - Dominant for many years but it has the disadvantage of being permeable to environmental moisture.
  
**Ceramic**
  - Power consumption, performance and environmental requirements.
<br>
  
6. **Evolution of Package Technology**

![image](https://user-images.githubusercontent.com/121998024/211217543-04bd2680-0a5f-4c29-b196-4c869a5e67b9.png)

![image](https://user-images.githubusercontent.com/121998024/211217561-8e0d2810-addc-4e7d-8f41-e20fce3f06c7.png)
 
<br>
</details>



<details>
<summary>Lab</summary>
<br>

<br>
</details>



<a name="user-content-two"></a>
### Day 2 - Details of IC Manufacturing Process

<details>
<summary>Theory</summary>
<br>

1. **Analog IC Design Process**

![image](https://user-images.githubusercontent.com/121998024/214596783-1040ff01-5b26-40a9-9fbf-8b29831627f6.png)

| Electrical Design                    | Physical Design                                                | Test Design                                         |
| -------------------------------------|:--------------------------------------------------------------:| ---------------------------------------------------:|
| Electrical design is a process of implementing the specifications to a circuit.| Physical design is a process of representing electrical design into a layout which consists of many distinct geometrical rectangle at various levels. | Test design is a process of coordinating, planning, and implementing the measurement of the analog integrated circuit performance. |
| Electrical design requires active and passive device electrical models for: | Physical design requires:     | Types of test:                                |         
| - Creating the desi                                                         | - Entering various geometries | - Functional                                  |
| - Verifying the design                                                      | - Follows DRC                 | - Parametric                                  |
| - Determining the robustness of the design                                  | - Check LVS                   | - Static                                      |         |                                                                             | - Extract parasitic           | - Dynamic                                     |        
<br>
 
2. **Analog IC Design Process and its Relation with CAD and PDK**  

![image](https://user-images.githubusercontent.com/121998024/214637527-2c857592-546d-4888-b321-9e022169a75a.png)

3. **Role of Circuit Designer**

The reason why it is so important that a VLSI circuit designer need to have a deeper understading on a CMOS manufacturing process:
- Instead of an ideal circuit, a circuit designer should always design a practical circuit based on the device
limits, technology constraints and physical implementations as the physical implementation of the circuit has a major impact on performance,
power and cost.
- Circuit designer need to have a very good understanding of layout design, so that in less iterations the design can be fridged.
- Circuit designer should always discuss with the layout designer for better and efficient circuit design and physical implementation. 
  
<br>
</details>

<details>
<summary>Lab</summary>
<br>

<br>
</details>



