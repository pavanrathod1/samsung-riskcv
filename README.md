# Samsung RISC-V Program  

**RISC-V Talent Development Program**, powered by **Samsung Semiconductor India Research (SSIR)** in collaboration with **VLSI System Design (VSD)**.  

## Basic Details  
- **Name**: Pavan  
- **College**: Vidyavardhaka College of Engineering  
- **Email**: pavanrathod5852@gmail.com  

## Task 1: RISC-V Toolchain Installation 
- Installation of RISC-V toolchain using the VDI link provided.
- The program demonstrates basic operations in C and their equivalent implementation in RISC-V assembly language.  

---
## Task 2:Task is to refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler simulator

Debugging with SPIKE: Comparing -O1 and -Ofast Optimizations

-O1: A moderate optimization for balanced performance.

-Ofast: A high-speed optimization that prioritizes performance over strict standards



## Task 3: Review the RISC-V software documentation to understand the R, I, S, B, U, and J instruction types.

RISC-V Instruction Types for the Given Code
Instruction Types
1. R-Type (Register-Register Instructions)
Typically involves arithmetic and logical operations between registers.
No such instruction appears directly in the given code at the C level, but operations like comparisons (e.g., num <= 0.0) may involve R-type instructions at the assembly level.
2. I-Type (Immediate Instructions)
Used for instructions with immediate values or memory addressing.
Example in the code: scanf("%lf", &num);
This would translate to an I-type instruction to load the address of num or handle immediate values.
3. S-Type (Store Instructions)
Used for storing data from a register to memory.
Example: Assigning the value entered by the user into the variable num involves S-type instructions.
4. B-Type (Branch Instructions)
Used for conditional branching.
Examples:
if (num <= 0.0)
if (num == 0.0)
These conditions are compiled into B-type instructions such as BEQ (branch if equal), BLT (branch if less than), or BGE (branch if greater or equal).
5. J-Type (Jump Instructions)
Used for unconditional jumps.
Example: The else block in the code could lead to a jump instruction to skip over the if block or jump to the end of the program.
6. U-Type (Upper Immediate Instructions)
Used for loading upper bits of immediate values.
While not directly visible in the C code, U-type instructions like LUI (load upper immediate) might be used during address calculations or handling larger constants.
7. UJ-Type (Unconditional Jump and Link Instructions)
Similar to J-type but used for function calls.
Example: The main() function or calls to printf and scanf might involve UJ-type instructions like JAL (jump and link).
This classification provides a detailed mapping of the instruction types based on the given C code.

## Task 4:By making use of RISCV Core: Verilog Netlist and Testbench, perform an experiment of Functional Simulation and observe the waveforms

Project Overview

This project performs a functional simulation of a RISC-V Core using a Verilog netlist and a testbench.
The goal is to verify the functional correctness of the core by analyzing the simulation results.
Prerequisites

Install the required simulation tools:
Icarus Verilog (iverilog) – To run the Verilog simulation.
GTKWave – To visualize the waveform outputs.
Ensure that you have access to:
The Verilog netlist of the RISC-V core.
The testbench for executing the simulation.
Setting Up the Simulation Environment
Clone or download the Verilog netlist and testbench files.

Install the required tools (e.g., Icarus Verilog, GTKWave).

Navigate to the project directory and compile the Verilog files using

iverilog -o riscv_sim risc_v_netlist.v testbench.v

Run the simulation:

vvp riscv_sim

Generate waveform files for analysis:

gtkwave dump.vcd

Running the Functional Simulation
Load the netlist and testbench into the simulator.
Execute the testbench to generate output signals.
Verify key signal behaviors such as:
Instruction execution
Register updates
Memory access
Capturing and Analyzing Waveforms
Use GTKWave to open the generated VCD file.
Observe important signals like PC (Program Counter), register values, and memory accesses.
Compare the expected vs. actual results to ensure functional correctness.
Uploading Results to GitHub
Save waveform snapshots as .png or .vcd files.
Update the README with:
Simulation logs
Waveform analysis

# task 5:Documentation and Repository Update 
Overview: Object Detector Using Ultrasonic Sensor with CH32V003
Project Summary:
This project is designed to detect objects using an HC-SR04 ultrasonic sensor interfaced with a CH32V003 RISC-V microcontroller. When an object is detected within a certain range, an LED indicator lights up to provide a visual alert. The system operates using a 3.3V power supply and is built on a breadboard using jumper wires for easy prototyping.

Project Description
This project implements an object detection system using the HC-SR04 ultrasonic sensor and the CH32V003 RISC-V microcontroller. It measures the distance of objects and triggers an LED when an object is detected within a specified range. The system operates on a 3.3V power supply and is built using a breadboard for easy prototyping.

Working Principle
The ultrasonic sensor (HC-SR04) emits sound waves from its TRIG pin.
The waves bounce back when they hit an object and are received by the ECHO pin.
The CH32V003 microcontroller calculates the distance based on the time delay between transmission and reception.
If the object is closer than 10 cm, the LED turns ON. Otherwise, it remains OFF.

# pinout configuration
![config](https://github.com/user-attachments/assets/a110e757-457b-4d09-8c1b-ad514b1be46c)

# components required
![Screenshot 2025-02-17 232536](https://github.com/user-attachments/assets/92298dde-df07-479f-802e-caf3bde6841b)

# application
Obstacle Detection for Robots
Proximity Sensing in Security Systems
Smart Parking Systems
Automatic Door Systems


# task6: Final Code Submission & Application Demo
![project im](https://github.com/user-attachments/assets/6b680db3-261d-470b-b20d-7e359ecb74e9)




