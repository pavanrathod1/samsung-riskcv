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

## Task4:By making use of RISCV Core: Verilog Netlist and Testbench, perform an experiment of Functional Simulation and observe the waveforms

4. FUNCTIONAL SIMULATION

4.1 About iverilog and gtkwave

Icarus Verilog is an implementation of the Verilog hardware description language.
GTKWave is a fully featured GTK+ v1. 2 based wave viewer for Unix and Win32 which reads Ver Structural Verilog Compiler generated AET files as well as standard Verilog VCD/EVCD files and allows their viewing.
4.2 Installing iverilog and gtkwave
For Ubuntu
Open your terminal and type the following to install iverilog and GTKWave

$   sudo apt get update
$   sudo apt get install iverilog gtkwave
To clone the repository and download the netlist files for simulation , enter the following commands in your terminal.
$ git clone https://github.com/vinayrayapati/iiitb_rv32i
$ cd iiitb_rv32i
To simulate and run the verilog code , enter the following commands in your terminal.
$ iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v
$ ./iiitb_rv32i
To see the output waveform in gtkwave, enter the following commands in your terminal.
$ gtkwave iiitb_rv32i.vcd


