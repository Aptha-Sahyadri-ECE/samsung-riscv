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

The image displays the content of a C program named sum.c


**ii. Optimzation using O1 and Ofast**

![4 RISC_V program compilation optimization(O1 Ofast)](https://github.com/user-attachments/assets/dc86a143-f57a-418b-9cdf-857cf251462a)

-O1 enables basic optimizations, while -Ofast applies aggressive optimizations for maximum performance.


**iii. Optimized assembly of O1**

![5 RISCV O1 optimized output](https://github.com/user-attachments/assets/e9f6acbd-96e5-4dcd-b15b-d5fc4216305b)

-O1 focuses on basic optimizations to reduce compilation time and improve code efficiency.

**iv. Optimized Assembly of Ofast**

![6 RISCV Ofast optimized output](https://github.com/user-attachments/assets/71a4c921-c62d-44fe-8426-1e1a80e87656)

-Ofast applies aggressive optimizations, including those that may break strict standards compliance for maximum performance.



  
 
 




  
