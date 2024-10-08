# vasudha_Nasscom_vsd_socdesignprog
##  Day-1 Inception of open source EDA, openLANE, sky130
## How to talk to computers
### In Introduction to QFN-48 Package, chip, pads, core, die and IPs
> The aim of the workshop is to give fundamental overview of chip design. Below image shows the arduino baord, known as FPGA board. Here, we will concentrate on the chip in the board called processor
![1](https://github.com/user-attachments/assets/bb6c61ee-9939-4835-82b9-b11961b4711e)
> The Arduino bard can be represented in the form of block diagram. As shown below, processor is surrounded by the interfaces like Vcc/GND, SRAM chip, JTAG etc. This is the typical board diagram to design an arduino board. 
> 
![2](https://github.com/user-attachments/assets/b1f0600a-d363-4c93-9e41-81725edb02c9)

Inside image of the chip is shown below. It is called as packages.This is particularly QFN-48. Chip is lacated at the centre of the package. CHip is connected to the packages using wire bond.

![4](https://github.com/user-attachments/assets/62a5f64a-3130-4c34-b86a-12f069de6e06)


![5](https://github.com/user-attachments/assets/3a7b6248-9b54-4d46-87ba-60825f2a4a20)

If we expand the chip. It consists of pads, core and die.

![7](https://github.com/user-attachments/assets/a828585c-6935-4aa9-bf2c-ea7a81dd269b)


![8](https://github.com/user-attachments/assets/d226a57f-2b6f-4f09-82fa-ee76e9b5b716)

* **Chip**: Pads are the physical areas on a chip used for making electrical connections between the IC and the outside world. They serve as interfaces for the external connections, including power, ground, and signal lines.  Pads can be input pads, output pads, power pads, or ground pads. Typically, pads are placed around the periphery of the chip to facilitate bonding with the package leads or solder bumps in flip-chip designs.

* **Core**: The core of a chip refers to the central part of the IC where the main functional blocks or logic circuits are implemented. It is the "heart" of the chip where the primary computational tasks are performed. The core may include digital logic circuits, analog circuits, processors, memory blocks, and other functional modules. The core is surrounded by the pad ring, which contains the pads mentioned earlier.
  
* **Chip die**: The chip die is the actual piece of silicon wafer that contains the integrated circuit. After the IC is fabricated on the wafer, the wafer is diced into individual dies, each containing a complete copy of the circuit. A die includes the core, pad ring, and other circuitry necessary for the chip's operation. The die is subsequently packaged to protect the silicon and provide connections to the external world.

* **Foundary IP's**: Foundry IPs (Intellectual Property) refer to the pre-designed and pre-verified blocks provided by semiconductor foundries. These IPs are optimized for the specific manufacturing processes of the foundry and are essential for efficient and reliable VLSI design.  IP blocks can include processors, memory modules, interface controllers, communication protocols, analog blocks, and more. Foundary Ip's need some amount of intellegent technique to bulid particular building blocks.

*  **Macros**: "macros refer to pre-designed and pre-verified blocks of circuitry that are used as building components in an integrated circuit (IC). These blocks can range from simple components, like logic gates, to more complex functional units, such as memories or processors. It is pur digital logic.

### In Introduction to RISC V
>  An ISA defines the way a processor interacts with the software and hardware. RISC-V is an open-standard Instruction Set Architecture (ISA) based on established Reduced Instruction Set Computing (RISC) principles.RISC V is the language of the computer. It is the way we are goinig to talk to the computer so that top level decription about an ISA (Instruction set Architecture). RISC-V interacts with hardware through a well-defined set of interfaces and protocols that govern how instructions are executed, how data is accessed and manipulated, and how peripherals and external devices communicate with the processor.
>
> For example if we want run a C program on hardware/computer which has particular layout as shown in the image. C program is first converted to assembly language program which is nothing but the RISC Vassebmly laguage. This assembly language is then converted to the machine language which is binary language program understood by the hardware of the computer. Then finally this bits are executed by the layout to get the required output.
>
> One more interface that present between the RISC-V architechture and layout is HDL (hardware description language). RTL is used to implement RISC-V specification. Here, it is picorv32 CPU core. So, RTL implement the RISC-V specification then finally we get RTL to layout. It's nothing but standard RTL to GDS flow.


![2](https://github.com/user-attachments/assets/00bde373-c2b2-4192-b40e-8737f364baab)

### From software application to hardware
> In real life, we typically interact with application software (applications) to communicate with the hardware. Between the application software and hardware, there is a layer called system software. The application interface with the system software which then converts the application progrem into the binary language.
![L3_1](https://github.com/user-attachments/assets/e293e4b4-745b-4083-aa7c-6e9b378e8891)
>
> The system software is comprised of several layers:
>* Operating ystem (OS): The task of the OS is to handle input/output operations, memory allocation and low level system function. The operating system converts the apps into corresponding code in language s such as C, C++, Java.
>* Compiler: The compiler takes the code from the OS and converts it into an instruction set (eg .exe files).Instr1, Instr2 acts as an abstract interface between c language and hardware.
>* Assembler: The assembler converts the .exe files into binary language which the hardware understand and execute to perform the desired operation.
>
## Day-1  SoC design and OpenLANE
### Introduction to all components of open-source digital asic design
> An Application-Specific Integrated Circuit (ASIC) is a type of integrated circuit (IC) customized for a particular use or application rather than intended for general-purpose use.  Elements to design ASIC are:
> 1. RTL
> 2. EDA
> 3. PDK


![1](https://github.com/user-attachments/assets/f8e7de77-3154-4d77-9cd1-808a0d223fa1)

* RTL: RTL (Register Transfer Level) is a critical abstraction level used in the digital design process of ASICs and FPGAs. It describes the flow of data between registers and the logical operations performed on that data. RTL design is implemented using Hardware Description Languages (HDLs) such as Verilog or VHDL. Open source RTL design sites are given in figure.
* EDA: EDA (Electronic Design Automation) tools are software solutions that facilitate the design, simulation, verification, and manufacturing of electronic systems, particularly integrated circuits (ICs) and printed circuit boards (PCBs). EDA tools are essential for managing the complexity of modern electronics design and ensuring that designs meet performance, power, area, and manufacturability requirements.
* PDK: THe interface between the FAB and the designer becomes set of data files and documents that is referred to as PDK. Collection of files used to model a fabrication process for the EDA tools used to design an IC.
> PDK includes process design rules such as DRC, LVS, PEX, device models, digital standard libraries and I/O libraries and many more.
>> In 2020, google releases its first ever open source PDK for the masses. The PDK has all the data information for successful ASIC implementation using open source EDA tools for 130 nm. ASIC design is a complex process. A methodology is needed for successful ASIC implementation. The main objective of ASIC flow is to take the design from RTL to GDSII final layout.

### Simplified RTL2GDS flow

This starts with design a RTL model ends with ready to fabricate mask layout in GDSII format. The diagram shows the major implementation steps:
![2](https://github.com/user-attachments/assets/6832e7c7-78e9-4519-a514-51013616bef1)

* Synthesis: Converts RTL to a circuitout of component from standard cell library (SCL). The resultant circuit is described in HDL, usually referred to as gate level netlist. A gate level netlist is function equivalent to the RTL. Standard cells have regular layout. Each cell comes with different models/view utilized by different EDA tools e.g. electrical, HDL, SPICE, laout (abstract and detailed) view. 
![3](https://github.com/user-attachments/assets/d7f55b6d-d0ba-4d6f-a5d7-817b49ab85dd)

* Floor planning and power planning: In chip floor planning a chip die is partitioned between different chip components and place the I/O pads.
   
![5](https://github.com/user-attachments/assets/d7dbe90a-993c-4bf1-8896-137cb5215c36)

. In macro floor planning we define the macro dimentions, pin locations, also rows and routing tracks are defined.
![6](https://github.com/user-attachments/assets/db09981a-fbc5-493a-a259-e2dd89f30ab9)

In power planning power networks are consrtucted. Typically a chip is powered by multiple Vdd/Gnd pins; the power pins are connected to all component through rings, verticle and horizontal straps, such parallel structures are ment to reduce the resistance. Typically pwer distribution network uses the upper metal layer as they are thicker than lower metal layer hence have less resistance.
![7](https://github.com/user-attachments/assets/11ce277d-dc51-4b9b-81d9-0b4ec5882181)

* Placement: For macros we place the gate level netlist cells on the floor plan rows aligned with the sites. Connected cells to be placed very close to each other to reduce the interconnect delay.
![8](https://github.com/user-attachments/assets/09691d5e-7ca7-4b4e-abf3-ff9be61a5933)
Typically cell placements are done in two steps global followed by detailed placement.

* Routing: Clock routing is performed prior to signal routing by creating clock distribution network that deliver the clock to all clock cells e.g. flip-flops. The clock network looks like a tree.The clock tree is synthesised to deliver the clock to all cells in good shape with minimum skew and minimum latancy. Clock skwe means the arrival of the clock at different component at different time. Symmetric tree structures (H-tree, I-tree, X-tree) are used to eleminate the clock skew. 
![clkrout](https://github.com/user-attachments/assets/a9672c75-9368-45e5-8a9f-27b8825dca74)

After clock routing, signal routing is performed using fixed number of metal layers. Routing uses the availble metal layers defined as defined by PDKs.
The sky130 pdk defines six metal layers. The last layer is called the local interconnect layer (Ti), the follwing five layers also local interconnect layers are all Al layers.
Most routers are grid routers. They construct the routing grid out of the metal layer track. As routing grid is huge, divide and conqure approch is used for routing.
1. Global routing: It generates routing guide using course grid.
2. Detailed routing: I uses the routing guides to implement the actual wiring.

* Sign off: After the routing is completed, we construct final layout which undergoes various varifications like physical verifications and timing verifications. Physical verifications are DRC (design rule check), LVS (Layout vs schematic). DRC verifies design rule compliance, while LVS ensures functional correctness against the gate level netlist.
> Timing verification is static timing analysis, this checks the design for timing violations.  

### Introduction to OpenLANE ASIC flow
 When using open source EDA tools we need to know about 
+ Tools qualification
+ Tools calibration
+ Missing tools
+ 
OPen source has public repo on Github. OpenLANE started as an open-source flow for a true open source tape-out experiment. At efabless we have a familty called stiVe and we wanted to have open everything SOCs : open PDK, open EDA, open RTC.

 StiVe SOCs have several members as shown below.
![strive](https://github.com/user-attachments/assets/610a0716-466d-49fe-893b-04829169649a)

The main goal of the openLANE is to produce clean GDSII with no human intervention i.e. No LVS violation, No DRC violations and timing violations Open LANE is tuned for skywater130nm open PDK, It is also tested for XFAB180 and GF130G. 
It can be used to impement macros and chips. It has two mode of operations: autonomous (push button based) and interactive (run commands one by one).
OpenLANE is based on several open source projects such as Yosis, OpenRoad, magic, klayout, fault and some of othe open source tools.
The diagram shows openLANE ASIC flow. The flow strarts with design RTL which undergoes RTL synthesis using Yosis and ABS to produce an optimized gate-level netlist. This netlist is then subjected to STA (ststic timing analysis) to check for timing violations.  Following STA, Design for Test (DFT) is performed, though this step is optiona land uses the fault tool.

![openlane ASIC flow](https://github.com/user-attachments/assets/563de540-27cf-4656-a212-01e2eb7e4724)

Open source project FAULT for DFT includes:
* Scan insertion
* Automatic Test pattern generation (ATPG)
* Test pattern compaction
* Fault coverage
* Fault simulation
  

![Fault](https://github.com/user-attachments/assets/d69e4673-5ae5-4b43-9fba-41089c6ebe47)

After DFT, next step is physical implementation, also known as Automated Place and Rout (PnR), using openRoad.

For physical implmentation we use OpenRoad to perform
+ Floor/power planning
+ End decoupling capacitors and tap cells
+ Placement: Global and detailed
+ Post placement optimization
+ Clock tree synthesis
+ Routiong: GLobal and detailed

  During PnR, LEC is performed using Yosys. SO we compare the netlist resultant from the optimization during physical implementation to the gate level netlist generated from the sythesis to make sure the functional equivalence. LEC ensures that function did not change after modifying the netlist.

> Fake antenna diode insertion is the most impart step during physical implementation. This step is requires to avoid antenna rule violations.

**Dealing with antenna rules violations**
> When a metal wire segment is fabricated and it is long enough, it can acts as an antenna . RIE causes charge to accumulate on the wire, damaging the transistor gates during fabrications.
> Generally router eleminates such issues. If routers fails there are two solutions:
> 1. Bridging attaches a higher layer intermideary
> 2. Add antenna diode cell to leak away charges. antenna diodes are provided by the SCL.

![solutions](https://github.com/user-attachments/assets/b4478bf7-d619-4d51-83e3-5605eb39c166)

With OpenLane, we take preventive approach. We add a fake antenna diode next to every cell input after placement. Run the antenna checker (magic) on the routed layout. If the checker reports a violation on the cell input pin, replace the fake diode cell by the real one.
![9](https://github.com/user-attachments/assets/8d77ad61-10b4-4bba-a3ab-3492a10b1277)

 At the end, physical verification is performed which includes dDRC and LVS. Along with physial verification STA is also performed to check for timing violations in the design.
 DRC is performed using magic and also SPICE extraction from layout.
 MAgic and Netgen are used for LVS by comparing extracted SPICE by Magic vs. verilog netlist.

 ## Get familiar to open-source EDA tools
###  OpenLANE Directory structure in detail

OpenLANE comprises of many open source EDA tools. The aim of openLANE tool is to get RTl to GDSII flow.
** Linuz command step by step
   ```
   cd Desktop/work/tools               # Navigate to the tools directory
  cd openlane_working_dir             # Move to the openlane_working_dir directory
  cd pdks/sky130A/                    # Navigate to the sky130A directory within pdks
  ls -ltr                             # List files in sky130A directory (reverse chronological order)
  cd libs.ref                         # all process specific files
  ls -ltr                             # List files in libs.ref directory
  cd ../libs.tech                     # Move to libs.tech directory (files specific to the tools)
  ls -ltr                             # List files in libs.tech directory
  ```
  
      

![2](https://github.com/user-attachments/assets/78b36992-dc30-47c6-bbc5-b35deb8ddb53)

We are working with sky130A pdk.
```
cd libs.ref                         # all process specific files
ls -ltr                             # List files in libs.ref directory
cd ../libs.tech                     # Move to libs.tech directory (files specific to the tools)
ls -ltr                             # List files in libs.tech director
cd ../
cd libs.ref
ls -ltr
```

![3](https://github.com/user-attachments/assets/d023e52c-f8e0-4b2b-b316-cf8085d4487a)

```
cd sky130_fd_sc_hd
ls -ltr
cd lib
ls -ltr
cd ../
cd lef
cd ../
cd techlef
cd ../../../../
ls -ltr
cd openlane
clear
```
![lib](https://github.com/user-attachments/assets/64f4c2fd-5776-4682-ae9d-e0dac91afdd0)


![lef](https://github.com/user-attachments/assets/d2cce2cc-a99d-455c-8557-c73c592f1470)


![techlef](https://github.com/user-attachments/assets/7eed51a5-07d2-4cf2-a33a-7310942e374b)
**Commands to invoke OpenLANE**
Commands to get into openLANE directory and invoke openLANE:
```
cd Desktop/work/tools
cd openlane_working_dir
cd openlane
docker
ls -ltr
./flow.tcl -interactive
```
![invokeopenlane](https://github.com/user-attachments/assets/5beecb49-e386-4f49-ac93-213869d8a80b)

> Openlane is meant to automate RTL to GDS flow, so if we use ./flow.tcl without interaction, it will run the complete flow.
>
> Command to import all the packages
> package require openlane 0.9
![package](https://github.com/user-attachments/assets/0d5b3c44-47e3-4b41-933f-66cb33f30d13)

Steps involved in preparing for the design process
/openlane cd designs
```
/ls -ltr
picorv32a
ls -ltr
cd src      %SRC stands for source
ls -ltr
cd ../
less config.tcl % bypass any configuration that has been already done into a plane
ls -ltr
clear
```
![confi tcl](https://github.com/user-attachments/assets/6edc0542-75f5-4561-a27f-6f24cbda7bfc)

prep -design picorv32a %prepare file system to setting data for design

### ![prep](https://github.com/user-attachments/assets/61d751ed-0959-4e27-bbee-d81711c58e86)
Review files after design preparation and run synthesis
```
cd runs
ls -ltr
cd 12_08_10_49
ls -ltr
cd temp
less merged.lef
```
![ouputmerge lef](https://github.com/user-attachments/assets/8d2d0ccf-1f73-497e-a3ee-a34bd44ff1f1)
```
cd ../
 cd results
cd synthesis
cd ../../
cd reports
cd ../
less config.tcl
less cmd.log
```

```
run_synthesis
```
### Steps to characterize synthesis results
```
cd results
ls -ltr
cd synthesis
ls -ltr
less picorv32a.synthesis.v
cd ../ cd../
cd reports
ls -ltr
cd synthesis
ls -ltr
```
![flopratio](https://github.com/user-attachments/assets/54a3d1eb-5504-494f-85da-c9a4c837b08d)

## Day 2 - Good floorplan vs bad floorplan and introduction to library cells
## Chip Floor planning considerations

**1. Define width and height of core and die**
> * Establish core and die dimensions to fir the design witin the chip's physical constraints.
> * Ensue the aspect ratio aligns with design and manufacturing requirements for optimal layout. All the logical cell should be inside the core.
>
> If logical cell occupies the complete area of the core as shown below then there is 100 % utilization.
>![1](https://github.com/user-attachments/assets/4a5f1a6c-704e-4860-9e16-4ce78d78bacb)

> Utilization factor= Area occupied by netlist/Total area of the core.
>![3](https://github.com/user-attachments/assets/6418cd08-48e6-460a-b23a-266ddbc5d41a)
> In case of 100 % utilization, utilization factor=1.
>
> ![4](https://github.com/user-attachments/assets/f8f10ece-fc29-4271-bc4d-7d2a73c85c16)

> Practically, we don't go for 100% utilizatio, we go for 50-60% utilization and utilization factor=0.5-0.6.

```
> **Aspect ratio=Height/width**
> when AR=1; it signifies the chip is sqare shape.
>      AR &ne; 1; chip is rectangular shape.
```

![5](https://github.com/user-attachments/assets/6b147b71-b50d-4fa1-a2e6-85261f4f24e3)

**2.Define the location of pre placed cell**
> * Placement of IP's/block in a user defined location in chip before automated placement and routing are called pre-placed cells.
> * Automated placement and routing tools places the remaining logical cells in the design onto chip.
> * Pre-placed cells are macros or IP's which is a piece of complex logic that can be reused multiple times.
> * The arrangement of the IP's in chip is referred as floor planning.
> * Preplaced cells surroud with decoupling capacitors.
>

![3](https://github.com/user-attachments/assets/f8440805-e8c1-4c5d-9c87-f4c9796d5c1c)

 ![5](https://github.com/user-attachments/assets/8ce9775c-11b8-4948-8e1c-661c93db0b2f)
 
 **Decoupling capacitors**
> * Place capacitors around pre-placed cells to stabilize power and mitigate noise interference.
> * Ensure adequate coverage to prevent power supply issues and maintain signal integrity.
>   
![4](https://github.com/user-attachments/assets/79a2a63c-2eba-45de-b524-58d1d620f59c)

**Power planning**
> * It involves creating a robust power distribution network (PDN) that ensures all parts of the chip receive adequate power while minimizing power noise, voltage drops (IR drop).
> * Multiple Vdd and Gnd is placed in the chip to solve the problem of voltage droop and voltage bump due to single power supply line.

![1](https://github.com/user-attachments/assets/2b060afd-0387-43ca-9d50-140273e8ee2d)

**Pin placement**
> * Pin placement refers to the strategic positioning of input/output (I/O) pins around the periphery of the IC or within specific regions in the case of advanced packaging or multi-die systems.
> * Proper pin placement ensure signal integrity, routing efficiency, power distribution, thermal management, and manufacturing considerations.
>
>   ![3](https://github.com/user-attachments/assets/ba964bb9-e4fa-4acc-8ff7-e9aae8831aa9)


**Logical cell placement blockage**
> * Logical cell placement blockage refers to regions within the IC layout where standard cells or logical cells are restricted from being placed as it is reserved for the pin placement.

![2](https://github.com/user-attachments/assets/198de248-732d-40e6-a3a3-9938ce762a6d)

 **Commands to run floorplan**

 ```
run_floorplan  # in openlane prompt
```
Commands to see floorplan layout in magic tool
![layout](https://github.com/user-attachments/assets/bf49dc92-083c-4e96-8b4f-74ed72bb60da)

Floorplan def in magic tool
```
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/30-07_09-24/results/floorplan/
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```
![zoomin_1](https://github.com/user-attachments/assets/d3621b58-7f2e-4e41-a48d-cca8908dc6a1)

## Library binding and placement
First step in placement and routing is to bind the netlist with the physical cells. Library contains the cells of different shapes and sizes and delay information. 
As shown in the below diagram shape of the gates define its functionality but in reality they are represented in the form of blocks of different sizes. The diagram below shows th eplacement of cell in the floorplan.

![1](https://github.com/user-attachments/assets/e8fc4b27-d4e4-4fd1-b73c-13024517047c)

![2](https://github.com/user-attachments/assets/321e34b0-5937-4cdf-ad06-1061e8a02927)

![3](https://github.com/user-attachments/assets/ef4adc7c-7f11-4f81-b441-67c211a3c18a)


![3](https://github.com/user-attachments/assets/2ee5cc46-bb44-4676-8c90-d33a9ead1337)


**Placement**
The next step after library binding is to place all the cells onto the floorplan keeping in mind it should not affect the pre-placed cell.
![4](https://github.com/user-attachments/assets/24b161d1-a838-4d43-8e84-70937dd7f393)

Command to run placement in openlane
```
run_placement
```
![placement](https://github.com/user-attachments/assets/685bb9fa-c305-4192-aaef-abfc88b023fc)

To open generated placement def in magic tool
```
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/30-07_09-24/results/placement/

magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &

```
![placement_1](https://github.com/user-attachments/assets/179f9b3e-99b0-4439-ac14-381592187e18)

**Cell design and characterization**

If we have placed and routed chip as shown in diagram. It represents placement and routed version of logical synthesis step. The cells placed is referred to as standard cells.

![1'](https://github.com/user-attachments/assets/1230efdb-2994-41f6-8a79-65ae2cd9cbc4)


Standard cells are being place in the library. Library consists of cells with different functionality, different sizes and different threshold voltages.
![1](https://github.com/user-attachments/assets/9c50c082-57c9-4d84-b830-87ab97272f51)

Ceonsidering one of the invertor let's see the cell design flow.  ary.

Cell design flow is being divided into three part.
1. Inputs
2. Design Steps
3. Outputs

   Lets understand the step by step cell design flow from below images.
   
   We have to design the invertor based on the PDKs given by the library.
![2](https://github.com/user-attachments/assets/2263c68b-0025-4c64-89b1-185bead304b1)
![3](https://github.com/user-attachments/assets/83e2708e-ead8-46a3-9dc8-1afecf75def1)

Next step is to design the circuit based on the available inputs. Design invloves circuit design, layout design and characterization.
First step in circuit design is to implement the function and then is to get PMOS and NMOS network graph.
![cktdesign](https://github.com/user-attachments/assets/ca38b65a-f41a-4992-addc-b4ba030426db)

Typical output of the circuit is called CDL (Circuit Description Language) file. Next step is layout design. First step is to get the function implemented through MOS transistors (NMOS and PMOS). Next step is to get the PMOS and NMOS network graph out of the circuit design. 

![layout design'](https://github.com/user-attachments/assets/c20b7b5a-98fc-406b-98ba-5450941d4935)

Next step is to get the Euler's path. It is the path which is being traced only once

![layout design](https://github.com/user-attachments/assets/f2455736-dace-4e93-b643-eb4bd1820488)

.Then draw stick diagram out of Euler's path. Stick diagram is derived from the circuit diagram.

![layout design1](https://github.com/user-attachments/assets/ba584b57-15f7-490e-88e9-1915f0b00440)

Next step is to convert the stick diagram into layout adhering to the rules we got from the input, DRC rules given by the foundary and user defined specification given by the top level user.
![layout design2](https://github.com/user-attachments/assets/a6b57d9c-e010-4739-bb4d-1bb14b811158)

Final step is to extract the paracitics out the layout and characterize it in terms of the timing. Output of the layout is in GDSii format, LEF basically decides the width and the height of the cells and extracted spice netlist (resistance/capacitance) or parasitics of each and every elements extracted out of the layout. That is called the spice net list.


![5](https://github.com/user-attachments/assets/41813225-6e8a-40d0-bffc-6577b4467066)

 Next step is characterization. Characterization helps to get the timing, noise and power information.

 **Characterization flow for buffer circuit**

 1. Read the model file
 2. Read the extracted spice netlist.
 3. Define/recognise the behay of the buffer.
 4. Read the sub circuit of the inverter.
 5. Attach the necessary power sources
 6. Apply the stimulus (inputs).
 7. Provide necessary output capacitance.
 8. Provide necessary simulation commands ( eg transient or dc)

 ### General timing characterization parameters 

 **Timing characterization and propagation delay**
  GUNA is the software used for characterization. It Perform timing, power, and noise characterizations and validate the design against specifications.

  

## Sky130 Day 3 - Design library cell using Magic Layout and ngspice characterization
### Labs for CMOS inverter ngspice simulations
** IO placer revision**

In openlane prompt 

```
run_floorplan
```
then Floorplan def in magic tool to see the cell configuration. 

We see that pins are equidistant from each other. If we want to change to some other i/o pin strategies. So there are four strategies that are supported by io placer. io placer is one the open source EDA tools which is used to place the i/o pins and all the core. So for this in /openlane/congiguration/ folder README.MD file which has the description of all the switches.

/openlane/configuration/less README.md    # it has the description of all the switches
/openlane/configuration/floorplan.tcl     # setting the ip pin strategies

copy the variable ::env(FP_IO_MODE) to open lane prompt and execute the command

set ::env(FP_IO_MODE) 2 
run_floorplan
```
```
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/30-07_09-24/results/floorplan/
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &


**Spice deck creation and simulations**

| ![1](https://github.com/user-attachments/assets/4baeccd2-c27c-442e-abf9-079a6b52348b) |![2](https://github.com/user-attachments/assets/3b4522a7-9171-42a0-a36d-b5d4ff29035a)  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|

| ![3](https://github.com/user-attachments/assets/f1fe5195-44d4-45bc-9496-ccb77024b1e9) | ![4](https://github.com/user-attachments/assets/817e8909-33d4-464e-ae9c-134d4070aaa2) |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|

|  ![6](https://github.com/user-attachments/assets/6ce48530-a230-42c4-a3f9-71c1988b7ec0) | ![5](https://github.com/user-attachments/assets/9fba9b02-53e2-4614-9b99-41575e049ec5) |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|

| ![8](https://github.com/user-attachments/assets/ccf04eaf-04fe-47d1-8419-81b31b6a2c6c) |![7](https://github.com/user-attachments/assets/65de310f-d700-4a70-ba8c-a721711ddf96) |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
**Inverter characteristics**

**Static Characteristics**
Switching Threshold (Vth): The voltage at which the inverter transitions from the high state (logic 1) to the low state (logic 0).

Input Low Voltage (Vil): The maximum input voltage considered as logic 0.

Input High Voltage (Vih): The minimum input voltage considered as logic 1.

Output Low Voltage (Vol): The voltage at which the output transitions from high to low.

Output High Voltage (Voh): The voltage at which the output transitions from low to high.

Noise Margins: The voltage range between Vil and Vol (low noise margin) and between Vih and Voh (high noise margin).

**DYNAMIC CHARACTERISTICS**

Propagation Delays: The duration required for the output to respond after a change in the input.

Rise Time (tr): The time it takes for the output to move from the low voltage level (Vol) to the high voltage level (Voh).

Fall Time (tf): The time it takes for the output to move from the high voltage level (Voh) to the low voltage level (Vol).

**Lab steps to git clone vsdstdcelldesign**
In openlane, we will gitclone one of the repository 
```
cd Desktop/work/tools/openlane_working_dir/openlane      # change directory to openlane
 https://github.com/nickson-jose/vsdstdcelldesign.git   #clone the repository with custom invertor design
ls -ltr
cd vsdstdcelldesign                                     # Change into repository directory
ls -ltr                                                 # open vsd standard cell
pwd                                                     # gives the location to where we will copy
 ```
![1](https://github.com/user-attachments/assets/9bd6b2b8-2f1a-4ec8-9fe5-5f321f6a4eae)
![2](https://github.com/user-attachments/assets/b31bf4c1-45a8-4029-85b4-1b625ff1f4c0)

Now we open the mag file. But before this we need to have the magic tech file to open this.

# Copy magic tech file to the repo directory for easy access
cd pdks/sky130A/libs.tech/magic    #it is in the openlane_working_dir
ls -ltr
cp sky130A.tech /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
![3](https://github.com/user-attachments/assets/ad5b5f58-00e4-452c-8602-1858c81ad91d)

In vsdstdcelldesign directory 

```
ls -ltr
magic -T sky130A.tech sky130_inv.magic &    
```
![4](https://github.com/user-attachments/assets/09ff6084-4cf3-4c5b-b960-0f8cf88740ea)
![5](https://github.com/user-attachments/assets/81bd6561-6d61-462c-a481-62434b6f9537)

![6](https://github.com/user-attachments/assets/23ca72ca-9598-455f-b927-0410b3ab17a6)

**Press 'S' and then 'V' to centralize the layout.

### 16 Mask CMOS  Fabrication Process ###

| ![1](https://github.com/user-attachments/assets/93c87b42-499d-44b6-b4e5-9801d39522d2)| ![3](https://github.com/user-attachments/assets/fd94b128-d38d-4c0d-af31-c5fe8e57ce1c)|
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|

| ![5](https://github.com/user-attachments/assets/66fa2acc-382e-4db5-9358-bf999960340f)| ![7](https://github.com/user-attachments/assets/e1cd574b-f825-49a2-8c7f-43070394641d) | 
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|

|![pwell creation2](https://github.com/user-attachments/assets/9a5a28b5-1863-41da-8c54-bcd24951fdc3)| ![n well creation](https://github.com/user-attachments/assets/2f82cf53-e50c-45f2-b7b9-e086e61e2ae4) |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|

|![8](https://github.com/user-attachments/assets/66b30e83-6f4d-45c5-982f-5816681b5427)| ![6](https://github.com/user-attachments/assets/fd2928b7-d147-42b9-bd27-2f92edd08f6b)|
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|

|![sidewall spacer1](https://github.com/user-attachments/assets/cb711bc4-0685-42e4-a9a5-968931fab74c)| ![7](https://github.com/user-attachments/assets/23e3b19a-da70-49b4-a8fa-6e68c3f2723f)|
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|

|![10](https://github.com/user-attachments/assets/9e7dca8c-9d0e-4b7f-9b1b-f5ed3a8aefcb)| ![16](https://github.com/user-attachments/assets/79905093-c662-4a98-9ee1-93a68e04ec67)|
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
1. Selecting a substrate
2. Create active region
3. Formation of N well and P well
4. Formation of gate terminal
* low energry implant to attain required doping concentration at the surface. Doping concentration depaends on the threshold voltage.
* make the polyisilicon gates low resistance by aading additional n type impurities.
5. Lightly doped drain (LDD) formation

6. Source and drain formation
7. Local interconnect formation
8. Higher level metal formation

  ## Sky130 tech file
  **Lab steps to create final SPICE deck using sky130 tech**
  
![ext2spice1](https://github.com/user-attachments/assets/c60aafcc-9bf3-469a-81fa-5e02ac88981d)

```
pwd

# Extraction command to extract to .ext format
extract all

# Before converting ext to spice this command enable the parasitic extraction also
ext2spice cthresh 0 rthresh 0

# Converting to ext to spice
ext2spice
```
![runngspice](https://github.com/user-attachments/assets/b9fb6cb2-bc09-4213-b7b5-0a7788138697)
Creation of std cell layout and extract spice netlist Spice File
![4](https://github.com/user-attachments/assets/7c555233-027f-4ac0-9e43-da9b650a49be)

![2_changingcload](https://github.com/user-attachments/assets/0057489b-1440-4ece-be68-7c3b255cafba)


###  Lab introduction to Sky130 basic layers layout and LEF using inverter
![3](https://github.com/user-attachments/assets/eb1ddacd-94b5-4005-9fbf-348a6a67f93a)

![4](https://github.com/user-attachments/assets/7d4cfa65-8171-4243-a4d9-b522b0cbf633)
![5](https://github.com/user-attachments/assets/0583725d-5eb2-462d-b8cf-4a190bee2e72)
![rise transition graph](https://github.com/user-attachments/assets/f527cb37-26ae-4ff6-b932-f4a3bccf29aa)

![rise transition value](https://github.com/user-attachments/assets/c487248c-d69b-4089-998d-9ea5e9c5fb5a)


![fall time 20per](https://github.com/user-attachments/assets/7e70fbb4-d42d-4e6f-b958-01bf3d2a55c7)
![falltime80per](https://github.com/user-attachments/assets/08af5e70-c03e-4a0a-b464-7d21d87365b1)
![falltime](https://github.com/user-attachments/assets/734f1d91-d4db-46cd-b2a6-5c7b04717881)
![cellfalldelay](https://github.com/user-attachments/assets/200280ec-c218-48f4-8206-9a864d54d248)
![cellrisedelay](https://github.com/user-attachments/assets/9b0ff42b-00e6-4eae-877a-385da8b46b71)

**Lab introduction to magic and Steps to load skyTechrules**

Topics:
+ In depth overview of magic's drc emgine
+ Introduction to google/skywater DRC engine
+ Lab warmup excercise: Fix or create a simple rule error
+ Lab main exercise: Fix or create a complex problem

  website: www.opencircuitdesogn.com/magic

  + Look at magic tutorial 2 and 6. See magic commands.
  + See technology files
  + Magic technology gile menu
  + See cifoutput section and Drc section
  + In table of contents see DRC section
  + See documentation Fabrication technology -----> google ----->skywater.

**Lab introduction to sky130 pdks and steps to download labs**
pdk information can be found in https://github.com/google/skywater.pdk

and documentation can be found in https:// github.com/google/skywarwepdk/sky130A

See skywater-pdk.readthedocs.io/en/main
see periphery rules

Lab contents URL:
https://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz

+ tar xfz drc
+ drc_tests.tgz.1
+ tar xfz drc_tests.tgz
+ cd drc
+ cd
+ drc_tests
+ ls -al
+ pwd
+ cd home/cad/design/drc_test
+ ls -al
+ vi -magicrc  # see technology file
+ magic -d XR

**Lab introduction to magic and steps to load sky130tech rules**
In tkcon2.3 main
+ Goto file---->open---->met3.mag
+ See met3 description in periphery (Type colon or semicolon)
+ In tkcon 2.3 main execute command
+ select area
+ goto m31
+ drc why

magic uses u=many deried layers. To see this visually, draw a large area using a mouse pointer. Select the material from color box (via2)
Type command
```
cif see VIA2 # select via 2 from color palate
box
snap int
box
```

 **Lab exercise to fix poly.9 error in Sky130 tech file**
 Commands
 ```
feed clear
load poly # in magic load the file poly.mag
```
**check the website for rule description. Distance between the n poly and ploy should be 0.22 um but clearly it is not. so first define the error under
drc_test directory

```
drc_test directory
vi sky130A.tech
/drc   #search for drc
/poly.9 #search for poly.9
```
```
Make corrections
/aliases #check this section
add allpolynonres in place of poly

after correction check in magic

tech load sky130A.tech
drc why
```








 
    



![1](https://github.com/user-attachments/assets/d12d3e0b-a9fe-4e83-90e1-6ad72f734765)

![2](https://github.com/user-attachments/assets/dc5ac898-7384-435e-aeca-41773782ed43)


![met3 mag](https://github.com/user-attachments/assets/f836062f-20ff-4780-a480-022de14a3e8c)
![via3](https://github.com/user-attachments/assets/00e49fd8-3997-434b-ad26-88a875cfed2f)

**Poly.9**

![1](https://github.com/user-attachments/assets/dae4e0a7-1772-4605-bffe-55950248c99e)
![2](https://github.com/user-attachments/assets/bc019bfa-7c3c-4dfa-8fe4-9b37d5d071c9)
![after correction](https://github.com/user-attachments/assets/754f1319-cb9e-4d6d-a41d-bdb4baa57914)
![correction](https://github.com/user-attachments/assets/5b78cc89-04e4-40b1-855f-44feafb1efe0)

**Lab exercise to implement poly resister spacing to diff and tap**
![before corrections](https://github.com/user-attachments/assets/3d59b4f6-7ff7-42f3-a1a8-1f59267b5d79)

![after correction](https://github.com/user-attachments/assets/3bc1dcb0-e567-4795-a44f-68b1a1acbb1c)

**Exercise to describe DRC error as geometrical construct**
![load nwell](https://github.com/user-attachments/assets/6f0aaec8-a832-4885-b069-5a21d5fd516e)

![1](https://github.com/user-attachments/assets/30ea1659-e002-49b7-9b14-670668b641ce)
![2](https://github.com/user-attachments/assets/6ee6501b-6d19-4459-8b15-d2f14fd055d9)

![3](https://github.com/user-attachments/assets/fce151c8-47f1-4f7e-8d51-daf527d42974)
![4](https://github.com/user-attachments/assets/be0984b3-3fa1-4dab-9971-a46cb824ffea)
![styledrc](https://github.com/user-attachments/assets/a1eb7e3b-460d-49a7-9cd8-73c29274ba16)

** find missing or incorrect rules and fix them**

![1](https://github.com/user-attachments/assets/bfe0be4d-ec74-4795-af0f-b5c561e3091f)
![2](https://github.com/user-attachments/assets/37b8308d-a0aa-42b7-8a0e-f60a94a4b017)
![3](https://github.com/user-attachments/assets/39ba29b3-e951-47c4-9c45-d0cc5ddc5f26)
![4](https://github.com/user-attachments/assets/24029d8a-5021-4068-8ff9-e75b5bc57545)
![5](https://github.com/user-attachments/assets/baced382-e029-482d-b9a3-258d218ac472)
![6](https://github.com/user-attachments/assets/f55725e5-42c0-42f0-8175-394fca5c317b)


## Day 4 - Pre-layout timing analysis and importance of good clock tree

###  Timing modelling using delay tables

**Lab steps to convert grid info to track inf**

![1](https://github.com/user-attachments/assets/fced14b4-dcf0-44c5-bf25-fd1a8d133e1e)
![1_1](https://github.com/user-attachments/assets/6b2b65eb-c7e4-44ac-9087-10d08ff85bcd)
![2](https://github.com/user-attachments/assets/b99c36b3-6baf-4183-b7da-268124bdde34)
![3](https://github.com/user-attachments/assets/0ba91365-e27c-423b-8fbc-e617fb4e86d1)
![4](https://github.com/user-attachments/assets/6711b59c-9b4b-471e-81a3-9a3c680d1152)
![5](https://github.com/user-attachments/assets/ce178c61-b16f-474e-b9b2-807207d0a3a8)

**Lab steps to convert magic layout to std cell LEF**
![1](https://github.com/user-attachments/assets/e0fb41f1-2323-4468-bebc-6ed5514c6785)

![2](https://github.com/user-attachments/assets/e6765d91-d212-486e-8d50-583669bce0cf)

![3](https://github.com/user-attachments/assets/de24efd4-ba01-4a9b-8127-40bec2e64bfc)

![4](https://github.com/user-attachments/assets/ef0b49b0-91c2-42ce-b89f-d3d631e1ad18)

**Introduction to timing libs and steps to include new cell in synthesis**
![get path using pwd](https://github.com/user-attachments/assets/ee3016e7-5628-4342-9706-3a03d75422cd)
![2copyleffile](https://github.com/user-attachments/assets/30958b96-23fd-4180-b71c-39e882bf1b6b)
![3](ht![4](https://github.com/user-attachments/assets/f0cf4789-5ea3-41a5-ac3f-d904805e9220)
![4](https://github.com/user-attachments/assets/065bd305-c6bc-41e0-99f9-b8df3d35d008)

![5](https://github.com/user-attachments/assets/5dce7b58-a49a-48c8-869c-ab5a21bebc35)
![6](https://github.com/user-attachments/assets/205ed859-3fb9-46ee-8a50-64345cd01ae2)
![7](https://github.com/user-attachments/assets/1814bf4d-b326-43a8-a359-3085febf24c1)
![8open config tcl](https://github.com/user-attachments/assets/99543be6-62b7-47e3-8519-2ac9f2d8795d)
![9](https://github.com/user-attachments/assets/ae4f2db5-0a5c-409b-9966-fcad0f8817cc)
![10 after modification](https://github.com/user-attachments/assets/3820e03e-8fbb-43c8-907c-fe0a783619fa)
![11](https://github.com/user-attachments/assets/ef9a56ae-4af8-494c-b230-86cb2c289840)

**Introduction to delay tables**
![1](https://github.com/user-attachments/assets/5f360911-47b9-476a-acbd-4a5386d19eb6)

![2](https://github.com/user-attachments/assets/46ae3f94-9f2e-4492-b3eb-d767282b03c2)

**Delay table usage Part 1**

![1](https://github.com/user-attachments/assets/59eca7a5-70af-4439-911f-327e5b89a2f3)


**Delay table usage Part 2**
![3](https://github.com/user-attachments/assets/92f47540-6d78-4e5b-a69e-5ea280d402d7)

***Lab steps to configure synthesis settings to fix slack and include vsdinv**
![synthesis](https://github.com/user-attachments/assets/12d5db4d-b977-44ba-8a42-c57e5e56ead1)
![2](https://github.com/user-attachments/assets/e3616c32-9f4d-4e43-8fb8-161566c442ea)
![3](https://github.com/user-attachments/assets/47fad521-69ef-4370-bf8f-78ae69aeb622)
![4](https://github.com/user-attachments/assets/054d3a7f-2f59-4d26-bcbb-1e12705d89e5)
![5](https://github.com/user-attachments/assets/dd34442e-6b68-4dd6-add9-796abaa2e309)
![6floorplan](https://github.com/user-attachments/assets/e99bfc3c-59f6-4965-97e3-8f00cdf2270a)
![7](https://github.com/user-attachments/assets/9777771f-b2bb-45e9-a845-c27cc8dd3f14)
![7](https://github.com/user-attachments/assets/3fa376c6-54dd-4c4b-94fa-f81566356360)

![8_placement result](https://github.com/user-attachments/assets/1cfb6219-a51a-4d20-a02a-da5b3c804fa8)
![9](https://github.com/user-attachments/assets/8d73b83a-1794-4dff-a54c-9cd2df295dec)


![10](https://github.com/user-attachments/assets/1528eb6b-0eaa-4a6a-8d1e-ae929f1f98a0)


##  Timing analysis with ideal clocks using openSTA

**L1 - Setup timing analysis and introduction to flip-flop setup time**

![1](https://github.com/user-attachments/assets/8ee47b49-66d2-4afa-b74e-9adb716e5365)

**L2 - Introduction to clock jitter and uncertainty**

![1](https://github.com/user-attachments/assets/b660ae77-c2c1-494e-83df-62022f56ea4e)

![2](https://github.com/user-attachments/assets/f6a2125e-c921-4f20-a527-702273ff4be0)

![3](https://github.com/user-attachments/assets/31fae378-4eb2-412c-9e7c-7759232f8785)

![4](https://github.com/user-attachments/assets/f27f84af-e3b6-497f-b5b9-18f1a783ee0d)
![5](https://github.com/user-attachments/assets/90f6b7b4-dead-4c17-b04e-de80b0666985)
![6](https://github.com/user-attachments/assets/d78552c7-7e0b-461a-9127-e40184c41d6b)
![7](https://github.com/user-attachments/assets/db88c4ff-1f93-4a4b-9707-9cf1fe334e11)


**L3 - Steps to configure OpenSTA for post-synth timing analysis**


![1](https://github.com/user-attachments/assets/14d47e49-eb79-4ea3-bb57-0e6cf96361a5)
![1 1](https://github.com/user-attachments/assets/4678d6f4-f8c5-450d-9470-91af10e0dd07)
![2](https://github.com/user-attachments/assets/c352071c-5471-4166-8e05-f4a1fa4377fe)
![3_capacitance](https://github.com/user-attachments/assets/83655446-c049-40b2-8af7-af31722c8791)
![3](https://github.com/user-attachments/assets/1b2fc431-d9dc-49f4-9341-3f4f46a24a2b)
![3 1](https://github.com/user-attachments/assets/ccc4a946-afa9-47fb-a344-82ddb207ead3)
![3 2](https://github.com/user-attachments/assets/a6061f9e-e537-4636-aecf-5f7e2b85685a)
![5mybase](https://github.com/user-attachments/assets/be379b4f-7e50-4817-a5b6-a3854c08cfd9)
![5 1mybase](https://github.com/user-attachments/assets/7298f7cb-7726-4525-b75e-fb686b7a296c)
![6](https://github.com/user-attachments/assets/98c1e3f1-cb7f-453a-b841-752988eb7d4c)
![7_sta pre_sta conf](https://github.com/user-attachments/assets/79353c70-6e32-44c0-9711-96eec8ec0e55)

**L4 - Lab steps to optimize synthesis to reduce setup violations**

![1](https://github.com/user-attachments/assets/4f4f39d8-1b21-4d7e-a4d5-2157579af07c)
![2](https://github.com/user-attachments/assets/585999cf-8c90-4773-8a98-8307065dc62c)
![3](https://github.com/user-attachments/assets/52afc4c1-f0ca-4daf-ab08-e2703a19ffda)
![4](https://github.com/user-attachments/assets/d3fdaf8e-37fb-4ee8-8c6e-bb2c66a41acd)
![5](https://github.com/user-attachments/assets/37f358c4-019c-402a-a162-c418b4e2ebd7)
![6](https://github.com/user-attachments/assets/6d1f9b41-6bd4-4ee3-82b7-2cfd1d44fb04)
![7](https://github.com/user-attachments/assets/cb587838-7151-4437-af13-0fd3dd081265)
![8](https://github.com/user-attachments/assets/8fa17410-d422-4fcc-91bd-5ee9dcf3b7ec)
![9](https://github.com/user-attachments/assets/35e143be-4774-4742-a971-29ee11cdc6ac)
![10](https://github.com/user-attachments/assets/e9cfc748-43aa-418a-bb98-52919d2763c3)
![11](https://github.com/user-attachments/assets/1d3adaef-5121-4259-939d-4248700ce075)
![12](https://github.com/user-attachments/assets/ae8fba1a-5cbe-4bd5-9140-04ca1ba4bb8e)
![13](https://github.com/user-attachments/assets/ab19254c-7efc-4f39-8a3a-32d2d8fe6091)

**L5 - Lab steps to do basic timing ECO**
![1](https://github.com/user-attachments/assets/4ee651c2-a061-416c-b457-31fd346589df)
![2](https://github.com/user-attachments/assets/185eb91e-6848-4385-b0c3-c9422877877e)
![3](https://github.com/user-attachments/assets/69c95f0d-2d5c-4f3e-a9b1-2118f5374211)
![4](https://github.com/user-attachments/assets/3ea8c3d4-0865-4acb-b0a9-10c3d0f2f6c7)
![5](https://github.com/user-attachments/assets/9d91322f-5b5c-4f96-b688-435fabc05b98)
![6](https://github.com/user-attachments/assets/9a2231c3-42fe-4a57-ad2b-1b26292321dc)
![7](https://github.com/user-attachments/assets/d7d85fe7-cb29-4152-9820-1b38b306b7dd)
![8](https://github.com/user-attachments/assets/f4875e47-8261-4c30-926b-3805a0a57ad8)
![9 1](https://github.com/user-attachments/assets/56794ddf-2cbf-45f6-9391-c8fb1e7ba6d2)
![9 2](https://github.com/user-attachments/assets/0fe311bb-f86c-47ec-a00c-e15a599de22e)


## Clock tree synthesis TritonCTS and signal integrity

**Steps to run CTS using TritonCTS**



![1](https://github.com/user-attachments/assets/81b8fa98-edc0-414a-9d78-5089bdc457df)
![2](https://github.com/user-attachments/assets/b22c0334-3490-41de-b3b9-86c826f0a8e7)
![3](https://github.com/user-attachments/assets/3eb40503-4df1-4f60-81b3-0edaf06ca46d)
![4](https://github.com/user-attachments/assets/0e23427f-975d-4211-98a8-a1dd8a84c120)
![5](https://github.com/user-attachments/assets/0ad3138c-0454-484e-bc34-c74b3d20e202)
![5 1](https://github.com/user-attachments/assets/1d5b687a-baff-4c84-af87-1b6c54ec901d)
![6](https://github.com/user-attachments/assets/02509d46-cc93-46cf-9cf9-dd1803e9c4fb)
![7](https://github.com/user-attachments/assets/118b5fcc-47fc-48fb-bd61-e77fbee607eb)
![8](https://github.com/user-attachments/assets/f8676da0-a43d-4a2c-9a87-66b1542bb717)
![9](https://github.com/user-attachments/assets/2750ed45-fe7a-4ef0-a9a1-8ca11984e6f2)
![9 1](https://github.com/user-attachments/assets/12f2ec3e-2f7e-4753-86ae-e42b3b7ae022)

![10](https://github.com/user-attachments/assets/725f25a9-a6f0-41b5-bd18-5b0d182d728f)
![11](https://github.com/user-attachments/assets/74909864-bb17-46c4-8289-fab99a754a7a)
![12](https://github.com/user-attachments/assets/255775e0-2857-48bf-9d30-68eaab3b2b01)
![13_floorplanrun](https://github.com/user-attachments/assets/e0c7d538-f3df-4f44-8031-62b6ad29a0ae)
![14](https://github.com/user-attachments/assets/a6a8ce8d-ccfa-4005-8ef0-3c7aefcd67ab)
![15](https://github.com/user-attachments/assets/6adb6463-56d5-431d-8aa9-4ecdd7d05224)
![16](https://github.com/user-attachments/assets/4603e27e-665a-4184-a7b4-a49590883e47)
![17](https://github.com/user-attachments/assets/ba14d099-77aa-43f7-9c69-91b482432163)

**Steps to verify CTS runs**


![1](https://github.com/user-attachments/assets/c23a7870-b89b-4193-b6a8-9d889d7131bd)
![2](https://github.com/user-attachments/assets/4a8054e2-6690-4b1b-b2f3-c3c761bfe715)
![3](https://github.com/user-attachments/assets/6c6083f8-b395-49c7-a0fb-83e3407d2a78)
![4](https://github.com/user-attachments/assets/81662c7c-8fab-459b-bd89-0fe1c400fe7a)
![5](https://github.com/user-attachments/assets/e4ca4470-b183-4654-8435-4d0e92f7be1c)
![6](https://github.com/user-attachments/assets/22555218-16af-4b73-a12b-d4709f89f301)
![6 1](https://github.com/user-attachments/assets/c6364814-1be8-42dc-9bcc-57687d1cf670)
![7](https://github.com/user-attachments/assets/1a425719-506f-49d8-8463-695630248b97)
![8](https://github.com/user-attachments/assets/1a77b5c7-01a1-4012-9fca-6465900e308d)
![8 1](https://github.com/user-attachments/assets/fba2bb06-8a51-47eb-b04a-b9af9027b405)
![9](https://github.com/user-attachments/assets/c0dc52e5-89c1-4be7-8e3b-712caccd8e94)
![10](https://github.com/user-attachments/assets/85986d1a-5761-4ba4-8d82-7bc4ba8262cb)

## Timing analysis with real clocks using openSTA

**Lab steps to analyze timing with real clocks using OpenSTA**
![1](https://github.com/user-attachments/assets/568e7da9-e893-44da-8d27-dbe27e3ddbe0)

![2](https://github.com/user-attachments/assets/f83582bb-913f-407e-8779-d9b19b721bed)
![3](https://github.com/user-attachments/assets/a4059e86-74f6-4c42-8425-0aba355d0072)
![4](https://github.com/user-attachments/assets/350aa818-af9d-4ba2-a8a2-84060166f088)
![5](https://github.com/user-attachments/assets/f24e4358-c618-40d2-9cb1-145bb8d0d024)
![6](https://github.com/user-attachments/assets/857d8f53-5b79-46b3-b20b-625e665e1ffe)

![7](https://github.com/user-attachments/assets/68b58cf9-f7c3-4781-8a6d-9823f638c4cf)

**Lab steps to execute OpenSTA with right timing libraries and CTS assignment**

![1](https://github.com/user-attachments/assets/6e92be18-f61b-406e-ab0a-3b68c7e3e61b)
![2](https://github.com/user-attachments/assets/fac6323d-a83a-442d-bb3a-6d4db2286b50)
![3](https://github.com/user-attachments/assets/43263db9-3764-4295-a626-802bb42aebc2)
![4](https://github.com/user-attachments/assets/96772fa4-5680-42c5-8714-500fdd8eb387)
![5](https://github.com/user-attachments/assets/c2abae93-a16e-46b3-a6d7-592f3e93afc3)
![6](https://github.com/user-attachments/assets/c17be0e8-fdd9-4313-9342-ef1ba9b554e5)
















