# vasudha_Nasscom_vsd_socdesignprog
## Inception of open source EDA, openLANE, sky130
## Day-1 How to talk to computers
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
