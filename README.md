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

### In Introduction to QFN-48 Package, chip, pads, core, die and IPs


