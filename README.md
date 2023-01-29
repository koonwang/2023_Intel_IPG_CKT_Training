# 2023 Intel IPG CKT Training

## Table of Contents
<a href="#one">Day 1 - Fundamentals of VLSI Design and Overview of Sand-to-Silicon</a>
<br>
<a href="#two">Day 2 - Analog VLSI Design Flow and CMOS Fabrication Process</a>
<br>
<a href="#three">Day 3 - CMOS Fabrication Process in DeepSubmicron (DSM) and Ultra DeepSubmicron (UDSM) Technology</a>
<br>
<a href="#four">Day 4 - Metal-Oxide-Semiconductor Structure</a>
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
<summary>Assignment</summary>
<br>

<br>
</details>



<a name="user-content-two"></a>
### Day 2 - Analog VLSI Design Flow and CMOS Fabrication Process

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
<br>
  
1. **Substrate Creation**

![image](https://user-images.githubusercontent.com/121998024/215072649-8dc2d5e5-9d0d-4eae-b580-06836e0667c5.png)

2. **Oxidation Process**
- Grow a protective silicon dioxide, SiO2 on top of the silicon wafer.
  
![image](https://user-images.githubusercontent.com/121998024/215073368-bbfed27e-2c78-48ed-8163-baf20d217a8c.png)
  
3. **Photoresist**
- Deposit a layer of photoresist where photoresist is a light sensitive organic polymer. It will softens when exposed to the light.
  
![image](https://user-images.githubusercontent.com/121998024/215074993-c8f55a40-cd13-4161-ae39-3a8ac83a0ccd.png)

4. **Lithography**
- Photoresist is exposed through the n-well mask.

![image](https://user-images.githubusercontent.com/121998024/215075697-f1bd3128-f88a-4c7a-b84e-7e0b116fb45e.png)

![image](https://user-images.githubusercontent.com/121998024/215075909-5e6bc0bb-852d-4e9c-baec-04b677e8c473.png)
  
5. **Etching**
- Oxide layer is etched with Hydrofluoric acid where this acid only attacks oxide.

![image](https://user-images.githubusercontent.com/121998024/215080709-b258dd16-3f0e-4044-b936-d1f9d769c6d8.png)

6. **Strip Photoresist**
- The remaining photoresist is stripped off using the micture of acids called the piranah etch.
  
![image](https://user-images.githubusercontent.com/121998024/215081081-93d96320-00c8-47d2-9876-42cb3754605e.png)

![image](https://user-images.githubusercontent.com/121998024/215081173-f269fc03-2b45-459f-89e2-6884b99c507f.png)

7. **N-well Creation**
- N-well is formed with diffusion or ion implantation.
  
![image](https://user-images.githubusercontent.com/121998024/215081772-3ea4bb9b-0310-4176-8280-ee3fdeee4dac.png)

8. **Strip Oxide**
- Remaining oxide is stripped off using Hydrofluoric acid, HF
  
![image](https://user-images.githubusercontent.com/121998024/215082586-effe906b-e7c2-48d1-a138-81ae170f6985.png)

![image](https://user-images.githubusercontent.com/121998024/215082653-bdbc5563-296d-4874-9444-00dd3b5b239d.png)

9. **Thin Oxide Deposition**
- A very thin layer of gate oxide is deposited.

 ![image](https://user-images.githubusercontent.com/121998024/215083644-e6234c76-c4e3-44f3-ac52-0877703eed41.png)

10. **Polysilicon Deposition**
- Chemical Vapor Deposition (CVD) of silicon layer to form polysilicon.
  
![image](https://user-images.githubusercontent.com/121998024/215084250-75169e71-9c35-4b67-ab27-215139a6551e.png)

11. **Polysilicon Patterning**
- Lithography process is applied to pattern the polysilicon.
  
![image](https://user-images.githubusercontent.com/121998024/215084844-9ddc7db2-33d8-4342-8bd4-5c89c0864d6b.png)
  
![image](https://user-images.githubusercontent.com/121998024/215084975-1c4a546a-ea7f-4814-a6b1-3fda2cc930b3.png)

12. **Thick Oxide Deposition**

![image](https://user-images.githubusercontent.com/121998024/215085832-a857afbf-0c66-420c-8c6f-7fcc9bf30176.png)

13. **Etching of Thick Oxide**

![image](https://user-images.githubusercontent.com/121998024/215086205-2285f6e4-408c-4ebe-80ee-9d86beee2d5e.png)

![image](https://user-images.githubusercontent.com/121998024/215086283-b602b25d-d6ed-453d-94c8-e2c80c18f990.png)

14. **N+ Diffusion Region Creation**
- N+ diffusion for NMOS source and drain are formed.
  
![image](https://user-images.githubusercontent.com/121998024/215086509-8facbe8d-a3ff-471f-a704-9764049d17f0.png)

15. **Etching of Thick Oxide**
- Oxide is stripped off to complete the patterning step.
  
![image](https://user-images.githubusercontent.com/121998024/215086786-bacf1fad-8b3a-42cd-820b-75b452a3fa64.png)

![image](https://user-images.githubusercontent.com/121998024/215086974-1203a87f-0b20-469d-a589-13ab1f5e381f.png)

16. **P+ Diffusion Region Creation**
- P+ diffusion region for PMOS source and drain are formed along with substrate contact.

![image](https://user-images.githubusercontent.com/121998024/215087576-1372f107-5c09-4957-9750-02ab0bb1653e.png)

![image](https://user-images.githubusercontent.com/121998024/215087665-237e8c59-dd22-4a38-9ed1-7bbdac62f414.png)

17. **Thick Oxide Deposition**
- The chip is covered with thick field oxide.
  
![image](https://user-images.githubusercontent.com/121998024/215088484-f20ed51b-b1d2-4439-9bf9-18e557f6aa77.png)

- The oxide is then etched where contact cuts are needed.

![image](https://user-images.githubusercontent.com/121998024/215088749-f66fe27a-e8c8-4d97-bf56-e9ba4b098373.png)

![image](https://user-images.githubusercontent.com/121998024/215088889-80b4f881-b150-4a9d-8a89-c7eec8f19304.png)

18. **Contact Creation**

![image](https://user-images.githubusercontent.com/121998024/215089304-dd4512a7-0095-4679-b193-ea770e90ef95.png)
  
19. **Metalization**
- It is patterned to remove access metal.

![image](https://user-images.githubusercontent.com/121998024/215089683-3b16ace6-373d-40c8-9e7e-8fc47cffbbc2.png)  
<br>
</details>  
  
<br>
</details>

<details>
<summary>Assignment</summary>
<br>

Question 1

![image](https://user-images.githubusercontent.com/121998024/215314580-1c25f545-8968-4fc5-8b2d-3d2587a2306e.png)

Question 2
  
![image](https://user-images.githubusercontent.com/121998024/215314602-9b5a3a44-ae52-4227-bba9-51db545cdcb9.png)

Question 3

![image](https://user-images.githubusercontent.com/121998024/215314618-4e389cca-8588-448a-9b10-69f61619c2eb.png)

Question 4
  
![image](https://user-images.githubusercontent.com/121998024/215314644-b74740f1-6a06-4726-8482-738571c8249c.png)

Question 5
  
![image](https://user-images.githubusercontent.com/121998024/215314659-727ba0d2-ab6d-4e05-81fa-f3a2154d96d4.png)

Question 6
  
![image](https://user-images.githubusercontent.com/121998024/215314678-a12a485b-686b-43d6-bcf0-18e3e5094fcb.png)
  
Question 7
  
![image](https://user-images.githubusercontent.com/121998024/215314695-08e1d576-6cd9-4ce1-b5a1-e0403f0652ed.png)

Question 8
  
![image](https://user-images.githubusercontent.com/121998024/215314711-913b630e-c854-4795-b02a-d598044d873e.png)
  
<br>
</details>



<a name="user-content-three"></a>
### Day 3 - CMOS Fabrication Process in DeepSubmicron (DSM) and Ultra DeepSubmicron (UDSM) Technology

<details>
<summary>Theory</summary>
<br>

1. **Disadvantage of the Submicron CMOS Process**

- The use of reverse bias PN junctions to isolate transistors becomes impractical as the transistor sizes decreased/depleted.

![image](https://user-images.githubusercontent.com/121998024/215318848-4939ca25-d1be-4529-b0d5-3021bf8e8ef7.png)
<br>

2. **Local Oxidation of Silicon (LOCOS) Isolation Process**
(Local Oxidation of Silicon, LOCOS is the traditional isolation technique used in submicron processes.)

Process Steps:
- A very thin layer silicon dioxide is grown on the wafer, called as pad oxide. Then a layer of silicon nitride is deposited which is used as an oxide barrier.

![image](https://user-images.githubusercontent.com/121998024/215322024-d310992f-c0a1-4472-945c-7d3208247ce1.png)

- Then photolithography is done to pattern and etch the nitride and pad oxide where the thick oxide will be grown.

![image](https://user-images.githubusercontent.com/121998024/215322100-28c3c7ba-7672-4540-9dfd-3eca34371bdf.png)

- Then by thermal oxidation process thick oxide is grown in the exposed area.

![image](https://user-images.githubusercontent.com/121998024/215322136-44fba5b8-ae36-4f5b-b7a3-98319e4dcfda.png)

- The last step is the removal of the silicon nitride layer.

![image](https://user-images.githubusercontent.com/121998024/215322272-0636722f-dff9-4037-ae08-3bebd82272c7.png)

  - The disadvantage of the LOCOS technique is the bird’s beak effect and the surface area which is lost to this encroachment.
  - The advantage of LOCOS fabrication process is simple process flow and high oxide quality because the whole LOCOS structure is thermally grown.
<br>

3. **Shallow Trench Isolation Technology**
- Shallow trench isolation (STI) allows closer spacing of transistors by eliminating the depletion region at the surface and Bird’s beak effect due to LOCOS process.

![image](https://user-images.githubusercontent.com/121998024/215322742-5a972f26-b4e8-4829-b7cb-b4d744112315.png)

Shallow Trench Isolation Technology Process Steps:
- Shallow Trench Isolation (STI) isolation is the preferred isolation process for deep-submicron process because it completely avoids Bird’s beak shape characteristics.
  
![image](https://user-images.githubusercontent.com/121998024/215323653-3b9f4072-b0b7-46c7-b3f5-6d4eb67048ee.png)

  - Cover the silicon wafer with pad oxide and silicon nitride.
  - First etch nitride and pad oxide. Next, an anisotropic etch is made in the silicon to a depth of 0.4 to 0.5 microns.
  - Grow a thin thermal oxide layer on the trench walls.
  - A CVD dielectric film is used to fill the trench.
  - A chemical mechanical polishing (CMP) step is used to polish back the dielectric layer until the nitride is reached. The nitride acts like a CMP stop layer.
  - Densify the dielectric material at 900°C and strip the nitride and pad oxide.
- STI advantage is more suitable for the increased density in a small area because it allows forming smaller isolation regions.
- The disadvantage is larger number of process steps.
<br>

4. **Deep Submicron (DSM) CMOS Technology**

![image](https://user-images.githubusercontent.com/121998024/215327504-6bba5ce1-5250-40cf-87f2-0693de4adfe5.png)

- Deep Submicron (DSM) technology provides:
  - A deep n-well that can be utilized to reduce substrate noise coupling.
  - A MOS Varactor that can be used to make voltage controlled oscillators (VCOs).
  - Different types of resistors in deep submicron (DSM), for example: diffused and/or implanted resistors, well resistors, poly resistors, and metal resistors.
  
  ![image](https://user-images.githubusercontent.com/121998024/215327871-69cf1296-3e29-478f-9863-2a0e1c995988.png)

  - At least 6 levels of metal that can form many useful structures such as inductors, capacitors, and transmission lines.
  - Different types of capacitors in deep submicron (DSM), for example: Metal-Insulator-Metal (MIM) Capacitor and Polysilicon-Polysilicon Capacitor.
  
  ![image](https://user-images.githubusercontent.com/121998024/215328431-16db20d5-002f-4033-b632-195b7c02c8da.png)
<br>

5. Fabrication Steps for a Deep Submicron (DSM) CMOS Process  
  
<details>
<summary>1. Starting Material</summary>
  
- The substrate should be highly doped to act like a good conductor.

![image](https://user-images.githubusercontent.com/121998024/215329449-8277acff-10a2-4c8b-a7d4-a6ca5e8ff44d.png)
<br>
</details>  

<details>
<summary>2. n and p-well creation</summary>
  
- These are the areas where the transistors will be fabricated - NMOS in the p-well and PMOS in the n-well. It is done by implantation followed by a deep diffusion.

![image](https://user-images.githubusercontent.com/121998024/215331025-b1f12bd7-17a1-40cb-bfbd-a31aced3a906.png)
<br>
</details>

<details>
<summary>3. Sallow Trench Isolation</summary>
  
- The shallow trench isolation (STI) electrically isolates one region/transistor from another.

![image](https://user-images.githubusercontent.com/121998024/215331138-c04beaa2-df42-49b0-bfe9-8b8403155ca9.png)
<br>
</details>
  
<details>
<summary>4. Threshold Shift and Anti-Punch through Implants</summary>
  
- The natural thresholds of the NMOS is about 0V and of the PMOS is about –1.2V. An p-implant is used to make the NMOS harder to invert and the PMOS easier resulting in threshold voltages balanced around zero volts.
- Also an implant can be applied to create a higher-doped region beneath the channels to prevent punch-through from the drain depletion region extending to source depletion region.

![image](https://user-images.githubusercontent.com/121998024/215331269-b6f2a4d2-15f2-4bff-885b-9fa71fddb4de.png)
<br>
</details>  
  
<details>
<summary>5. Thin Oxide and Polysilicon Gate</summary>
  
- A thin oxide is deposited followed by polysilicon. These layers are removed where they are not wanted.  

![image](https://user-images.githubusercontent.com/121998024/215331374-e6fb9164-9622-41e6-9ee7-79412dab82aa.png)
<br>
</details> 
  
<details>
<summary>6. Lightly Doped Source and Drain</summary>
  
- A lightly-doped implant is used to create a lightly-doped source and drain next to the channel of the MOSFETs.  

![image](https://user-images.githubusercontent.com/121998024/215331470-4cbf8d49-11e0-473b-9538-ef7ec6269bb6.png)
<br>
</details>  
  
<details>
<summary>7. Sidewall Spacer</summary>

- A layer of dielectric is deposited on the surface and removed in such a way as to leave “sidewall spacers” next to the thin-oxide-polysilicon-polycide sandwich. These sidewall spacers will prevent the part of the source and drain next to the channel from becoming heavily doped.  

![image](https://user-images.githubusercontent.com/121998024/215331736-9855c42d-90ce-42c6-bc4f-6d5088194807.png)
<br>
</details>
  
<details>
<summary>8. Implantation of Havily Doped Source and Drain</summary>

- Note that not only does this step provide the completed sources and drains but allows for ohmic contact into the wells and substrate.

![image](https://user-images.githubusercontent.com/121998024/215331805-d237fd96-c857-45be-a9d8-557a2f947df2.png)
<br>
</details>  
  
<details>
<summary>9. Siliciding (Salicide and Polyside)</summary>

- This step reduces the resistance of the bulk diffusions and polysilicon and forms an ohmic contact with material on which it is deposited.

![image](https://user-images.githubusercontent.com/121998024/215331918-f87814c0-bdd1-4a59-a201-4ba1663e592c.png)
<br>
</details>    
  
<details>
<summary>10. Intermediate Oxide Layer</summary>

- An oxide layer is used to cover the transistors and to planarize the surface.

![image](https://user-images.githubusercontent.com/121998024/215332122-aeb3530c-c746-44b2-9057-f9fafa15decd.png)
<br>
</details>
  
<details>
<summary>11. First Level Metal</summary>

- Tungsten plugs are built through the lower intermediate oxide layer to provide contact between the devices, wells and substrate to the first-level metal.

![image](https://user-images.githubusercontent.com/121998024/215332202-432e6d8c-4155-4a8c-9546-059fba675bc0.png)
<br>
</details>
  
<details>
<summary>12. Second Level Metal</summary>

- The previous step is repeated for the second-level metal.

![image](https://user-images.githubusercontent.com/121998024/215332269-7ccedad3-40c5-4898-864b-2ae4f6dddc42.png)
  
Final Product:
![image](https://user-images.githubusercontent.com/121998024/215332313-0bdb5dc2-44e5-44ae-b25c-f2860c11d174.png)
<br>
</details>
<br>

6. **Summary of Deep Submicron (DSM) CMOS Fabrication Process**
- DSM technology typically has a minimum channel length between 0.35μm and 0.1μm
- DSM technology addresses the problem of excessive depletion region widths in junction isolation techniques by using shallow trench isolation
- DSM technology may have from 4 to 8 levels of metal
- Lightly doped drains and sources are a key aspect of DSM technology  
<br>

7. **Ultra Deep Submicron (UDSM) CMOS Technology**
  USDM Technology Main Features
  - Lmin ≤ 0.1 microns
  - Minimum feature size less than 100 nanometers
  - Today’s state of the art:
    - 22 nm drawn length
    - 5 nm lateral diffusion (12 nm gate length)
    - 1 nm transistor gate oxide
    - 8 layers of copper interconnect
  - Specialized processing is used to increase drive capability and maintain low off currents
<br>

8. **Advantage of UDSM CMOS Technology**

 **Digital Viewpoint**:
   - Improved Ion/Ioff
   - Reduced gate capacitance
   - Higher drive current capability
   - Reduced interconnect density
   - Reduction of active power
  
 **Analog Viewpoint**:
   - More levels of metal
   - Higher cutoff frequency
   - Higher capacitance density
   - Reduced junction capacitance per transconductance
   - More speed  
<br>

9. **Disadvantage of UDSM CMOS Technology**

  **Analog Viewpoint**:
  - Reduction in power supply resulting in reduced headroom
  - Gate leakage currents
  - Reduced small signal intrinsic gain
  - Increased nonlinearity
  - Increased noise and poorer matching
  
<br>
</details>


<details>
<summary>Assignment</summary>
<br>

**Assignment - DSM and UDSM Fabrication Process**  

1. List the five basic MOS fabrication processing steps and give the purpose or function of each step.
  - **Oxidation**
    - Is a process of growing a layer of silicon dioxide (SiO2) on the surface of silicon wafer.
    - It provides isolation between two layers and protects underlying material from contamination.
  - **Diffusion**
    - Movement of impurity atoms at the surface of the silicon into the bulk of the silicon - from higher concentration to lower concentration. Diffusion typically completed at high temperatures: 800 to 1400 °C.
  - **Deposition**
    - Deposition is the process by which various materials are deposited on the silicon wafer. For example: silicon nitride (Si3N4), Silicon dioxide (SiO2), Polysilicon, Aluminium and etc.
  - **Etching**
    - Etching is the process of selectively removing a layer of material.
  - **Photolithography**
    - Photolithography is a patterning process in which a photosensitive polymer is selectively exposed to light through a mask, leaving a latent image in the polymer that can then be selectively dissolved to provide patterned access to an underlying substrate.
<br>
  
2. What is the difference between positive and negative photoresist and how is photoresist used?  
  - Positive photoresist: Areas exposed to UV light are soluble in the photoresist developer solvent.
  - Negative photoresist: Areas not exposed to UV light are soluble in the photoresist developer solvent.
  - The photoresist is Solid organic material used in photolothography which transfers the designed pattern to the wafer surface. Photoresists have high etch reaction and adhesion properties.
<br>
  
3. Sketch the approximate cross sectional view of a NMOS transistor in a p-substrate. Identify each region and identify the connections at the top surface of the integrated circuit for the source, drain, gate and bulk/substrate.

![image](https://user-images.githubusercontent.com/121998024/215342954-5806225b-404c-4df7-8d48-289c2aec67ba.png)
<br>

4. Consider a mask that is opaque everywhere except for a transparent circle in the center. Metal is deposited on a substrate followed by an application of negative photoresist which is patterned with the mask described. After exposure, developing, and subsequent etching, what will remain ?

![image](https://user-images.githubusercontent.com/121998024/215345231-f52d386c-2ffd-4cb1-a09c-e71d2e8317c4.png)
<br>

5. What is the difference between submicron, deep submicron and ultra-deep submicron process ?  

| Comparison Feature              | Deep Submicron (DSM)                  | Ultra Deep Submicron (UDSM)       |
| --------------------------------|:-------------------------------------:| ---------------------------------:|
| Minimum Channel Length          | Between 0.35um and 0.1um              | Less than 0.1um                   |
| No. of Metal Layers             | May have 4 ~ 8 levels of metal.       | 8 layers of copper interconnect   |
| 
<br>  
  
6. What are the advantages of ultra-deep submicron (UDSM) process over deep submicron (DSM) process.  

   Digital Viewpoint:
   - Improved Ion/Ioff
   - Reduced gate capacitance
   - Higher drive current capability
   - Reduced interconnect density
   - Reduction of active power
   Analog Viewpoint:
   - More levels of metal
   - Higher cutoff frequency
   - Higher capacitance density
   - Reduced junction capacitance per transconductance
   - More speed
<br>

7. What is the difference between LOCOS and STI process ?
  - Local Oxidation of Silicon (LOCOS) is the traditional isolation technique.
    - It is a simple process flow.
    - It has high oxide quality because the whole LOCOS structure is thermally grown.
    - LOCOS technique has significant drawback, which is the formation of bird's beak effect and the surface area which is lost to this encroachment.

     ![image](https://user-images.githubusercontent.com/121998024/215347381-a0935bab-1158-4d0d-8b8d-ee05df1ab31e.png)

  - Shallow Trench Isolation (STI) is the preferred isolation technique for Submicron process because it completely avoids the bird's beak shape characteristic.
    - The main difference compared to LOCOS process is that shallow trench is etched into the silicon substrate, as shown in figure below.
  
    ![image](https://user-images.githubusercontent.com/121998024/215347539-0678257f-5627-4ad8-9924-efb8cb85bcdc.png)

    - The disadvantage is larger number of process steps.
<br>
  
8. Why for body connection a heavily doped n+ or p+ is used ?

<br>

9. What is use of silicide and polyside ? 
  - Both refer to metal contacts between metal interconnect and silicon transistor terminals in the substrate.
  - Polycide = Silicide over Polysilicon (non-self-aligned)
  - Salicide = Self-Aligned Silicide = Polysilicon over Silicide
<br>

10. Which process steps used for control threshold voltage and punch-through effect?
  - The 3rd step of Deep Submicron (DSM) CMOS fabrication process, which is 'Threshold Shift and Anti-Punch through Implants'.
  - The natural thresholds of the NMOS is about 0V and of the PMOS is about –1.2V. An p-implant is used to make the NMOS harder to invert and the PMOS easier resulting in threshold voltages balanced around zero volts.
  - Also an implant can be applied to create a higher-doped region beneath the channels to prevent punch-through from the
drain depletion region extending to source depletion region. 
<br>
</details>



<a name="user-content-four"></a>
### Day 4 - Metal-Oxide-Semiconductor Structure

<details>
<summary>Theory</summary>
<br>

<br>
</details>


<details>
<summary>Assignment</summary>
<br>

<br>
</details>











