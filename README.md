# README

## Details

**Name:** Vikas KA  
**College:** Sahyadri College of Engineering and Management, Mangalore  
**Email:** [vikaska9945@gmail.com](mailto:vikaska9945@gmail.com) / [vikas.ec23@sahyadri.edu.in](mailto:vikas.ec23@sahyadri.edu.in)

---

## Tasks

<details>
<summary>▶ Task 1: C Program Compilation and RISC-V Simulation</summary>

### Files:
1. ![C Program Output Snapshot](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task1/c%20programm%20output%20snapshot.png)
2. ![RISC-V Simulation Output (O1)](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task1/riscv%20(O1%2COfast).png)
3. ![RISC-V Simulation Output (O1) - Part 1](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task1/riscv%201(O1).png)
4. ![RISC-V Simulation Output (Ofast) - Part 2](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task1/riscv_2_Ofast.png)
5. ![Ubuntu Screenshot](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task1/ubuntu_screenshot.png)

### Task Overview:

In this task, a C program was compiled and simulated on the RISC-V architecture. Outputs from different optimization levels (-O1 and -Ofast) were analyzed to observe the effects on program performance and behavior.

#### 1. **C Program Output Snapshot (c_program_output_snapshot.png)**
   - A screenshot showing the output of the C program after compilation and execution.
   - It helps visualize the results produced by the program.

#### 2. **RISC-V Simulation Output (O1) (riscv_O1.png)**
   - A screenshot showing the output from the RISC-V simulation with -O1 optimization.
   - This output helps in comparing the performance and execution flow with optimization.

#### 3. **RISC-V Simulation Output (O1) - Part 1 (riscv_1_O1.png)**
   - A screenshot of the first part of the RISC-V simulation output with -O1 optimization.
   - It shows the intermediate results of the simulation.

#### 4. **RISC-V Simulation Output (Ofast) - Part 2 (riscv_2_Ofast.png)**
   - A screenshot showing the output from the RISC-V simulation with -Ofast optimization.
   - This output helps in comparing the results with the -O1 optimization.

#### 5. **Ubuntu Screenshot (ubuntu_screenshot.png)**
   - A screenshot showing the program execution environment on Ubuntu.
   - This image highlights the terminal where the C program was compiled and executed.

### Simulation Process:

1. **Compile the C Program**: The C program was compiled using the standard compilation method.
2. **RISC-V Simulation**: The compiled program was simulated using the RISC-V architecture with -O1 and -Ofast optimization levels.
3. **Analyze Outputs**: The outputs from both optimization levels were compared to observe performance differences.
4. **Capture Screenshots**: Screenshots of the simulation results were taken for documentation.

</details>

<details>
<summary>▶ Task 2: Simulation with Spike</summary>

### Overview:
In Task 2, the compiled C code was simulated on the Spike RISC-V simulator. Spike is an architecture simulator for RISC-V processors, which helps to simulate the execution of programs written for the RISC-V architecture. The task focused on debugging, observing the generated assembly output, and comparing the effects of different optimization levels during compilation. Two optimization levels were used during the process: `-O1` and `-Ofast`. Each optimization level affects the assembly instructions and overall program performance.

### Files:
1. ![C code compiled for Spike simulation](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task2/C%20code%20complied%20or%20spike%20simulation.png)
2. ![Debugging screenshot](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task2/Debugging.png)
3. ![Objdump using -O1 format](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task2/Objdump%20using%20-O1%20farmat.png)
4. ![Objdump using -Ofast format](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task2/Objdump%20using%20-Ofast%20format.png)

### Task Process:

1. **Compile C Code**: The C program was compiled using `riscv64-unknown-elf-gcc` with the respective optimization flags (`-O1` and `-Ofast`).
2. **Simulation with Spike**: The program was then run on the Spike RISC-V simulator to observe the execution and any differences between the optimization levels.
3. **Assembly Analysis**: Using `objdump`, the generated assembly code was inspected for both optimization levels to analyze how each optimization affected the code's structure and performance.
4. **Debugging**: Debugging was performed on the generated assembly code to identify any potential issues and observe the effects of different optimization flags on the program's behavior.

### Key Results:
- The comparison of `-O1` and `-Ofast` optimization levels showed noticeable differences in performance and code size.
- The debug process highlighted areas where the compiler optimizations led to more efficient code generation, especially in loop unrolling and instruction reordering.

</details>

<details>
<summary>▶ Task 3: Machine Code Instructions</summary>

### Files:
1. [Instructions.md](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/blob/main/Task3/instructions.md)
2. [Task3.txt](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/blob/main/Task3/Task3.txt)

### Content:

#### Machine Code for addi sp, sp, -16
- **Instruction:** addi sp, sp, -16  
- **Opcode:** 0010011 (7 bits)  
- **Immediate:** -16 (12 bits, two's complement)  
- **Source Register (rs1):** sp (x2) (5 bits)  
- **Destination Register (rd):** sp (x2) (5 bits)  
- **Function (funct3):** 000 (3 bits)  

**Breakdown:**
- Immediate (-16): 111111111100  
- rs1 (sp = x2): 00010  
- funct3: 000  
- rd (sp = x2): 00010  

**Machine Code Format:**  
imm[11:0] | rs1 | funct3 | rd | opcode  
1111111100 | 00010 | 000 | 00010 | 0010011

---

... (Include other instructions similarly) ...

</details>

<details>
<summary>▶ Task 4: Verilog Simulation</summary>

### Files:
![Basic Step of Iverilog](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task4/Basicstep_of_iverilog.png)
![GTKWAVE Waveform 1](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task4/GTKWAVE_waveform1.png)
![GTKWAVE Waveform 2](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task4/GTKWAVE_waveform2.png)
![GTKWAVE Window](https://github.com/VikasKA-Sahyadri-ECE/samsung-riscv/raw/main/Task4/GTKWAVE_window.png)

### Task Overview:

In this task, Verilog code was simulated using Iverilog and the resulting waveforms were analyzed using GTKWAVE. Below is a breakdown of the files involved:

#### 1. **Basic Step of Iverilog (Basicstep_of_iverilog.png)**
   - A screenshot showing the basic steps of running Iverilog for Verilog simulation.
   - It illustrates the setup and commands used to compile and simulate the Verilog code.

#### 2. **GTKWAVE Waveform 1 (GTKWAVE_waveform1.png)**
   - A screenshot showing the first waveform generated by GTKWAVE.
   - This waveform represents the output of the Verilog simulation for the given input.

#### 3. **GTKWAVE Waveform 2 (GTKWAVE_waveform2.png)**
   - A screenshot showing the second waveform, which may represent a different simulation or a modified version of the first one.

#### 4. **GTKWAVE Window (GTKWAVE_window.png)**
   - A screenshot showing the GTKWAVE window, displaying the simulation results in a graphical format.
   - This helps visualize the timing and behavior of the signals over time.

### Simulation Process:

1. **Iverilog Compilation**: The Verilog code was compiled using Iverilog with the following command:
   
```bash
iverilog -o simulation_output.vvp my_verilog_code.v
