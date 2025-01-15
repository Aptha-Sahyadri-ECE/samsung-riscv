# RISC-V Talent Development Program

The Program is based on practical knowledge and optimization techniques in RISC-V and its applications in the semiconductor industry.
The instructor for this internship is Kunal Ghosh Sir.

## Basic Details
**Name:** Aptha Shetty

**College:** Sahyadri College of Engineering and Management,Mangaluru


-------------------------------------------------------------------------------------------------------------------------------------------

<details>
<summary><B>Task 1:</b> Task is to install all the essential tools required for this internship such as Ubuntu on VMBox.Execute simple program using RISC-V and C in our machine.</summary>
  <br>

  **1. Install Ubutuntu 18.04on the Oracle Virtual Machine Box**
 ![Ubuntu 18 04](https://github.com/user-attachments/assets/bf88b238-658e-46f6-8e14-347942b1e9ae)

  **2. Execution of the program to sum numbers in C.**
  ![1  sum-execution](https://github.com/user-attachments/assets/79df157e-a46f-40dc-ab3b-338daec28ac1)
  
  **i. Change the directory to Home**
 
  To change to the home directory using the cd command

  **ii. Install leafpad command**

  Leafpad is a simple, lightweight, and fast text editor suitable for basic tasks. It is particularly favored in systems with limited resources.
  The command sudo apt install leafpad is used to install the Leafpad text editor on a Linux system.
  
  **iii. Open a File in leafpad**
 
  leafpad sum.c
  
  This command opens the sum.c file in the Leafpad text editor

 **iv. Write C code to sum numbers**
 ![2 sum-c code](https://github.com/user-attachments/assets/920523d8-e7bd-44db-b3ff-0282728522ea)

 Code to sum the numbers
 
 **v. Compile the program**

 gcc sum.c

 This command compiles the sum.c file using the GNU Compiler Collection (gcc).


**vi. Run the Program**

./a.out

This runs the generated executable.

**3. Execution of program using RISC-V**

RISC-V program execution involves compiling code with RISC-V-compatible compilers. Its reduced instruction set and optimization options ensure efficiency, scalability, and versatility across computing applications.

**i. Display contents of summing code**

![3 display content of the sum code](https://github.com/user-attachments/assets/0f91bbd9-7412-48c3-ac04-bcf6c492f963)


cat sum.c

 It displays the content of a C program named sum.c


**ii. Optimzation using O1 and Ofast**

![4 RISC_V program compilation optimization(O1 Ofast)](https://github.com/user-attachments/assets/dc86a143-f57a-418b-9cdf-857cf251462a)

-O1 enables basic optimizations, while -Ofast applies aggressive optimizations for maximum performance.


**iii. Optimized assembly of O1**

![5 RISCV O1 optimized output](https://github.com/user-attachments/assets/e9f6acbd-96e5-4dcd-b15b-d5fc4216305b)

-O1 focuses on basic optimizations to reduce compilation time and improve code efficiency.

**iv. Optimized Assembly of Ofast**

![6 RISCV Ofast optimized output](https://github.com/user-attachments/assets/71a4c921-c62d-44fe-8426-1e1a80e87656)

-Ofast applies aggressive optimizations, including those that may break strict standards compliance for maximum performance.
</details>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<details>
<summary><B>Task 2:</b> Task is to refer to lab videos and execute the task of compiling the C code using gcc and riscv compiler and performing SPIKE Simulation and Debugging the C code with Interactive Debugging Mode using Spike.</summary>
  <br>


 **1. Open a File in leafpad and write a code for calculating factorial**
 

 We use commands like leafpad filename.c and similar tools to create and write a simple program for calculating the factorial of a number.
 
  
 ![1 Factorial execution](https://github.com/user-attachments/assets/807e0918-bd9a-4c24-8d43-5532f6df537f)
 

 
![2  factorial C code](https://github.com/user-attachments/assets/8b16adac-d997-4d2e-8b0d-c04046692357)


**2. Execution of program using RISC-V**



**i. Display contents of factorial code and optiumization of the code using -O1**


 
![3 Display of C code and -O1 optimization](https://github.com/user-attachments/assets/1741e029-0338-43a4-8cbf-14d0852b1aa8)



**ii. Optimized assembly of O1**



![4 Assembly of -O1 optimization](https://github.com/user-attachments/assets/a0b9ff50-d686-43da-af67-d84202c61585)



-O1 focuses on basic optimizations to reduce compilation time and improve code efficiency.



**iii.-O1 optimized output**


We write a simple command to display the the output using riscv64 -O1 optimization.


spike pk filename.o


![5 -O1 Output](https://github.com/user-attachments/assets/123889bc-6f37-405a-af7d-85fe253f6537)



**iv.-O1 optimized assembly debugging**


We use the command spike -d pk filename.o for debugging.


![6 -O1 addi instruction debugging](https://github.com/user-attachments/assets/4dd0ba2c-9823-4289-bd32-0386d2519121)



reg 0 sp: This likely inspects the value of the stack pointer (sp), which holds the top of the stack.
**Assembly Instruction (addi sp, sp, -16)**:
This adjusts the stack pointer (sp) by subtracting 16 bytes, allocating space on the stack for local variables or function calls.
addi is the RISC-V instruction for "add immediate."
The stack pointer's new value is shown (0x000003fffffb40), indicating memory reserved for execution.



![7 -O1 sd instruction debugging](https://github.com/user-attachments/assets/ddb9181b-a067-49f8-b6e2-c33cdca076b6)


The debug output shows that the **instruction sd ra, 8(sp)** saves the return address (ra) onto the stack at an offset of 8 bytes from the stack pointer (sp). 
This is part of the function call setup to preserve the return address. The program counter (pc) moves to the next instruction, updating from 0x10188 to 0x1018c


![8 -O1 li instruction debugging](https://github.com/user-attachments/assets/e53b8fd6-13cd-4976-abfb-b482ab19cde6)


The debug output shows the execution of two **li (Load Immediate) instructions** in a RISC-V program.
The first instruction, li a2, 24, loads the immediate value 24 into register a2, as confirmed by the debug output showing reg 0 a2 with the value 0x0000000000000018 (decimal 24).
The second instruction, li a1, 4, loads the immediate value 4 into register a1, with the debug output showing reg 0 a1 holding 0x0000000000000004 (decimal 4).


**v. Display contents of factorial code and optimization of the code using -Ofast and its output**



![9 Display of c code and optimization and output for -Ofast](https://github.com/user-attachments/assets/9c914ee3-4658-4801-beb6-32eb63d35179)


**vi.-Ofast optimized assembly**


-Ofast applies aggressive optimizations, including those that may break strict standards compliance for maximum performance.


![91 assembly of -Ofast](https://github.com/user-attachments/assets/71854afc-0145-45be-b79b-0fcd6cd30860)



**vii.-Ofast optimized assembly debugging**


We use the command spike -d pk filename.o for debugging.



![92 lui,li,addi instruction debugging in _Ofast optimized assembly](https://github.com/user-attachments/assets/82ef63d5-c57e-43a9-b33a-6ec02ca62414)



**lui a0, 0x21**: Loads the upper 20 bits of register a0 with the value 0x21. The lower 12 bits are set to 0.


**addi sp, sp, -16**: Adjusts the stack pointer (sp) by subtracting 16. This is typically done to allocate space on the stack


**li a2, 24**: Loads the immediate value 24 into register a2. This is a pseudo-instruction, which translates to addi a2, x0, 24.


</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<details>
<summary><B>Task 3:</b> Task is to find  15 unique RISC-V instructions from the disassembly, their assembly representation, binary patterns, and corresponding 32-bit hexadecimal instructions.</summary>
  <br>


# RISC-V Instructions

This document contains 15 unique RISC-V instructions from the disassembly, their assembly representation, binary patterns, and corresponding 32-bit hexadecimal instructions.

---

## Instruction 1: `lui`
- **Assembly**: `lui a0, 0x21357`
- **Type**: U-Type
- **Binary**: `00100001001101010111 01000 0110111`
- **32-bit Hex**: `0x21357837`

---

## Instruction 2: `addi`
- **Assembly**: `addi sp, sp, -16`
- **Type**: I-Type
- **Binary**: `111111111111 01010 000 01010 0010011`
- **32-bit Hex**: `0xFFF00513`

---

## Instruction 3: `li`
- **Assembly**: `li a4, 24`
- **Type**: I-Type
- **Binary**: `000000001100 01001 000 01100 0010011`
- **32-bit Hex**: `0x01800593`

---

## Instruction 4: `add`
- **Assembly**: `add a0, a0, a1`
- **Type**: R-Type
- **Binary**: `0000000 00001 01000 000 01000 0110011`
- **32-bit Hex**: `0x00104133`

---

## Instruction 5: `jal`
- **Assembly**: `jal ra, <printf>`
- **Type**: J-Type
- **Binary**: `00000000100010100100 00001 1101111`
- **32-bit Hex**: `0x000A807F`

---

## Instruction 6: `ld`
- **Assembly**: `ld ra, 8(sp)`
- **Type**: I-Type
- **Binary**: `000000000100 01010 011 00001 0000011`
- **32-bit Hex**: `0x00828083`

---

## Instruction 7: `sd`
- **Assembly**: `sd ra, 8(sp)`
- **Type**: S-Type
- **Binary**: `0000000 00001 01010 011 00000 0100011`
- **32-bit Hex**: `0x0082A023`

---

## Instruction 8: `ret`
- **Assembly**: `ret`
- **Type**: I-Type (alias for `jalr`)
- **Binary**: `000000000000 00001 000 00000 1100111`
- **32-bit Hex**: `0x00008067`

---

## Instruction 9: `auipc`
- **Assembly**: `auipc gp, 0x10000`
- **Type**: U-Type
- **Binary**: `0001000000000000 00100 0010111`
- **32-bit Hex**: `0x10000137`

---

## Instruction 10: `sub`
- **Assembly**: `sub a0, a0, a1`
- **Type**: R-Type
- **Binary**: `0100000 00001 01000 000 01000 0110011`
- **32-bit Hex**: `0x40104133`

---

## Instruction 11: `beq`
- **Assembly**: `beq a0, a1, <offset>`
- **Type**: B-Type
- **Binary**: `0000000 00001 01000 000 00000 1100011`
- **32-bit Hex**: `0x00104263`

---

## Instruction 12: `j`
- **Assembly**: `j <offset>`
- **Type**: J-Type (alias for `jal x0, <offset>`)
- **Binary**: `000000000000 <imm[20:1]> 00000 1101111`
- **32-bit Hex**: `<computed value>`

---

## Instruction 13: `and`
- **Assembly**: `and a0, a0, a1`
- **Type**: R-Type
- **Binary**: `0000000 00001 01000 111 01000 0110011`
- **32-bit Hex**: `0x00107133`

---

## Instruction 14: `or`
- **Assembly**: `or a0, a0, a1`
- **Type**: R-Type
- **Binary**: `0000000 00001 01000 110 01000 0110011`
- **32-bit Hex**: `0x00106133`

---

## Instruction 15: `xor`
- **Assembly**: `xor a0, a0, a1`
- **Type**: R-Type
- **Binary**: `0000000 00001 01000 100 01000 0110011`
- **32-bit Hex**: `0x00104133`

---
</details>


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



  
