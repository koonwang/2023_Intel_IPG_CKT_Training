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
| - Creating the design                                                       | - Entering various geometries | - Functional                                  |
| - Verifying the design                                                      | - Follows DRC                 | - Parametric                                  |
| - Determining the robustness of the design                                  | - Check LVS                   | - Static                                      |         |                                                                             | - Extract parasitic           | - Dynamic                                     |        
<br>
 
2. **Analog IC Design Process and its Relation with CAD and PDK**  

![image](https://user-images.githubusercontent.com/121998024/214637527-2c857592-546d-4888-b321-9e022169a75a.png)
<br>

3. **Role of Circuit Designer**

The reason why it is so important that a VLSI circuit designer need to have a deeper understading on a CMOS manufacturing process:
- Instead of an ideal circuit, a circuit designer should always design a practical circuit based on the device
limits, technology constraints and physical implementations as the physical implementation of the circuit has a major impact on performance,
power and cost.
- Circuit designer need to have a very good understanding of layout design, so that in less iterations the design can be fridged.
- Circuit designer should always discuss with the layout designer for better and efficient circuit design and physical implementation. 
<br>

4. **CMOS Technology**

Why We Use CMOS Technology In IC Design ?
<br>  
Please refer to the comparison of MOSFET and BJT from an analog viewpoint [Allen-Holberg]

| Comparison Feature                   | BJT                                         | MOSFET                                |
| -------------------------------------|:-------------------------------------------:| -------------------------------------:|
| Cut-off Frequency (FT)               | High                                        | Less                                  |
| Noise (at same thermal noise)        | Less 1/f                                    | More 1/f                              |
| DC Range of Operation                | 9 decades of exponential current versus VBE | 2-3 decades of square law behaviour   |
| Transconductance (Same Current)      | Larger by 10X                               | Smaller by 10X                        |
| Small Signal Output Resistance       | Slightly larger                             | Smaller for short channel             |
| Switch Implementation                | Poor                                        | Good                                  |
| Capacitor                            | Voltage dependent                           | More option                           |
| Performance/Power Ratio              | High                                        | Low                                   |
| Technology Improvement               | Slower                                      | Faster                                |

- Almost every comparison favours BJT, however a similar comparison made from digital viewpoint would come up on the side of CMOS. Since large volume mixed-mode technology will be driven by digital demands, CMOS is an obvious choice.
<br>

**Categorization of the CMOS Technology**
- Submicron Technology: Lmin ≥ 0.35 µm
- Deep Submicron Technology (DSM): 0.1 µm ≤ Lmin ≤ 0.35 µm
- Ultra-Deep Submicron Technology (UDSM): Lmin ≤ 0.1 µm
- BiCMOS Technology: Lmin = 0.5 µm  
<br>

5. **CMOS Fabrication Process**  
 
Process Steps:  

<details>
<summary>1. Wafer Formation (Sand-to-Silicon)</summary>

- The raw material used in CMOS fabs is a wafer or disk of silicon, roughly 75mm to 300mm (12 inch) in diameter and less than 1mm thick.

![image](https://user-images.githubusercontent.com/121998024/215015972-565ed30e-ef4a-4e7c-86cb-ea0ce3f6cd87.png)
    
- Wafers are cut from boules, cylindrical ingots of singlecrystal silicon, that have been pulled from a crucible of pure molten silicon.
- Controlled amounts of impurities are added to the melt to provide the crystal with the required electrical properties.
- A seed crystal is dipped into the melt to initiate crystal growth.
- The seed is gradually withdrawn vertically from the melt while simultaneously being rotated, as shown in Figure below.

![image](https://user-images.githubusercontent.com/121998024/215014614-80bdaeb4-05a4-4b4a-9345-c9196570c605.png)

- The molten silicon attaches itself to the seed and recrystallizes as it is withdrawn.
- The seed withdrawal and rotation rates determine the diameter of the ingot.
- Growth rates vary from 30 to 180 mm/hour.  
<br>
</details>

<details>
<summary>2. Photolithography</summary>

- The patterning is achieved by a process called photolithography.
- The primary method for defining areas of interest (i.e., where we want material to be present or absent) on a wafer is by the use of photoresists.
- The wafer is coated with the photoresist and subjected to selective illumination through the photomask.
- A photomask is constructed with chromium (chrome) covered quartz glass. A UV light source is used to expose the photoresist.
- A developer solvent is then used to dissolve the soluble unexposed photoresist, leaving islands of insoluble exposed photoresist.
  
![image](https://user-images.githubusercontent.com/121998024/215020673-3184bad6-3f3e-420b-9461-bbf630fe5b4d.png)
<br>
</details>

<details>
<summary>3. Well and Channel Formation</summary>

- There are 4 CMOS technology processes
  - **N-well process**: In a n-well process, the pMOS transistors are built in a n-well and the nMOS transistor is placed in the p-type substrate.
  - **P-well process**: In a p-well process, the nMOS transistors are built in a p-well and the pMOS transistor is placed in the n-type substrate. p-well processes were used to optimize the pMOS transistor performance.
  - **Twin-well process**: Twin-well processes accompanied the emergence of n-well processes. A twinwell process allows the optimization of each transistor type.
  - **Triple-well process**: The triple-well process has emerged to provide good isolation between analog and digital blocks in mixed-signal chips; it is also used to    isolate high-density dynamic memory from logic.

![image](https://user-images.githubusercontent.com/121998024/215021729-239e5132-6b99-4a19-802a-e5b6c0b027cc.png)
<br>
</details>  

<details>
<summary>4. Silicon Dioxide (Sio2)</summary>

- Oxidation of silicon is achieved by heating silicon wafers in an oxidizing atmosphere. The following are some common approaches:
  - Wet Oxidation: when the oxidizing atmosphere contains water vapor.
    - The temperature is usually between 900 °C and 1000 °C.
    - Wet oxidation is a rapid process.
  
  - Dry Oxidation: when the oxidizing atmosphere is pure oxygen.
    - Temperatures are in the region of 1200 °C to achieve an acceptable growth rate.
    - Dry oxidation forms a better quality oxide than wet oxidation.
    - It is used to form thin, highly controlled gate oxides, while wet oxidation may be used to form thick field oxides.
  
- Atomic Layer Deposition (ALD): when a thin chemical layer (material A) is attached to a surface and then a chemical (material B) is introduced to produce a thin layer of the required layer (i.e., SiO2––this can also be used for other various dielectrics and metals).
<br>
</details>

<details>
<summary>5. Isolation</summary>  

- Individual devices in a CMOS process need to be isolated from one another so that they do not have unexpected interactions.  
- The transistor gate consists of a thin gate oxide layer.
- The thick oxide used to be formed by a process called Local Oxidation of Silicon (LOCOS).
- A problem with LOCOS-based processes is the transition between thick andthin oxide, which extended some distance laterally to form a so-called bird’s beak.
- Starting around the 0.35 µm node, shallow trench isolation (STI) was introduced to avoid the problems with LOCOS.
- STI forms insulating trenches of SiO2 surrounding the transistors (everywhere except the active area).
<br>
</details>  

<details>
<summary>6. Gate Oxide</summary>

- This is the process is to form the gate oxide for the transistors. As mentioned, this is most commonly in the form of silicon dioxide (SiO2).The transistor gate consists of a thin gate oxide layer.
<br>
</details>
  
<details>
<summary>7. Gate and Source/Drain Formations</summary>

- Grow gate oxide wherever transistors are required (area = source + drain + gate)––elsewhere there will be thick oxide or trench isolation.
- Deposit polysilicon on chip.
- Pattern polysilicon (both gates and interconnect)
- Etch exposed gate oxide—i.e., the area of gate oxide where transistors are required that was not covered by polysilicon; at this stage, the chip has windows down to the well or substrate wherever a source/drain diffusion is required.
- Implant pMOS and nMOS source/drain regions.
<br>
</details>

<details>
<summary>8. Contacts and Metallization</summary>  

- Contact cuts are made to source, drain, and gate according to the contact mask. These are holes etched in the dielectric after the source/drain formation.
- Older processes commonly use aluminum (Al) for wires, although newer ones offer copper (Cu) for lower resistance.
- Tungsten (W) can be used as a plug to fill the contact holes (to alleviate problems of aluminum not conforming to small contacts).
<br>
</details>

<details>
<summary>9. Passivation</summary>
  
- The final processing step is to add a protective glass layer called passivation or over glass that prevents the ingress of contaminants.
- Openings in the passivation layer, called overglass cuts, allow connection to I/O pads and test probe points if needed.
<br>
</details>
  
<details>
<summary>10. Metrology</summary>

- Metrology is the science of measuring. Everything that is built in a semiconductor process has to be measured to give feedback to the manufacturing process.
<br>
</details>

<details>
<summary>CMOS Fabrication Process Steps Illustration</summary>  

1. **Substrate Creation**
![image](https://user-images.githubusercontent.com/121998024/215072649-8dc2d5e5-9d0d-4eae-b580-06836e0667c5.png)

  
<br>
</details>

<details>
<summary>Lab</summary>
<br>

<br>
</details>



