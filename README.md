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
2.Machine Code for sd ra, 8(sp)
Instruction: sd ra, 8(sp) Opcode: 0100011 (7 bits) Immediate: 8 (12 bits, split into imm[11:5] and imm[4:0]) Source Register (rs2): ra (x1, 5 bits) Base Register (rs1): sp (x2, 5 bits) Function (funct3): 011 (3 bits) Breakdown:

Immediate (8): 0000000001000 rs2 (ra = x1): 00001 rs1 (sp = x2): 00010 funct3: 011

Machine Code Format: imm[11:5] | rs2 | rs1 | funct3 | imm[4:0] | opcode 0000000 | 00001 | 00010 | 011 | 00000 | 0100011

3.Machine Code for li a5, 100
Instruction: li a5, 100 (Expands to: addi a5, x0, 100) Opcode: 0010011 (7 bits) Immediate: 100 (12 bits) Source Register (rs1): x0 (constant 0, 5 bits) Destination Register (rd): a5 (x15, 5 bits) Function (funct3): 000 (3 bits) Breakdown:

Immediate (100): 00000001100100 rs1 (x0 = 0): 00000 funct3: 000 rd (a5 = x15): 01111

Machine Code Format: imm[11:0] | rs1 | funct3 | rd | opcode 0000001100 | 00000 | 000 | 01111 | 0010011

4.Machine Code for addiw a5, a5, -1
Instruction: addiw a5, a5, -1 Opcode: 0011011 (7 bits) Immediate: -1 (12 bits, two's complement) Source Register (rs1): a5 (x15, 5 bits) Destination Register (rd): a5 (x15, 5 bits) Function (funct3): 000 (3 bits) Breakdown:

Immediate (-1): 111111111111 rs1 (a5 = x15): 01111 funct3: 000 rd (a5 = x15): 01111

Machine Code Format: imm[11:0] | rs1 | funct3 | rd | opcode 1111111111 | 01111 | 000 | 01111 | 0011011

5.Machine Code for bnez a5, 10160
Instruction: bnez a5, 10160 (Expands to: beq a5, x0, offset) Opcode: 1100011 (7 bits) Immediate: Offset (calculated based on PC) Source Register (rs1): a5 (x15, 5 bits) Source Register (rs2): x0 (constant 0, 5 bits) Function (funct3): 001 (3 bits)

Breakdown: Immediate: Calculated (split as imm[12|10:5|4:1|11]) rs1 (a5 = x15): 01111 rs2 (x0 = 0): 00000 funct3: 001

Machine Code Format: imm[12|10:5] | rs2 | rs1 | funct3 | imm[4:1|11] | opcode xxxxxxxxxxx | 00000 | 01111 | 001 | xxxxxxxx | 1100011

6.Machine Code for lui a2, 0x1
Instruction: lui a2, 0x1 Opcode: 0110111 (7 bits) Immediate: 0x1 (20 bits, shifted left by 12 bits) Destination Register (rd): a2 (x12, 5 bits)

Breakdown: Immediate (0x1): 00000000000000000001 rd (a2 = x12): 01100

Machine Code Format: imm[31:12] | rd | opcode 0000000000000001 | 01100 | 0110111

7.Machine Code for addi a2, a2, 954
Instruction: addi a2, a2, 954 Opcode: 0010011 (7 bits) Immediate: 954 (12 bits) Source Register (rs1): a2 (x12, 5 bits) Destination Register (rd): a2 (x12, 5 bits) Function (funct3): 000 (3 bits)

Breakdown: Immediate (954): 001110101010 rs1 (a2 = x12): 01100 funct3: 000 rd (a2 = x12): 01100

Machine Code Format: imm[11:0] | rs1 | funct3 | rd | opcode 0011101010 | 01100 | 000 | 01100 | 0010011

8.Machine Code for li a1, 100
Instruction: li a1, 100 (Expands to: addi a1, x0, 100) Opcode: 0010011 (7 bits) Immediate: 100 (12 bits) Source Register (rs1): x0 (constant 0, 5 bits) Destination Register (rd): a1 (x11, 5 bits) Function (funct3): 000 (3 bits)

Breakdown: Immediate (100): 00000001100100 rs1 (x0 = 0): 00000 funct3: 000 rd (a1 = x11): 01011

Machine Code Format: imm[11:0] | rs1 | funct3 | rd | opcode 0000000110 | 00000 | 000 | 01011 | 0010011

9.Machine Code for lui a0, 0x1c
Instruction: lui a0, 0x1c Opcode: 0110111 (7 bits) Immediate: 0x1c (20 bits, shifted left by 12 bits) Destination Register (rd): a0 (x10, 5 bits)

Breakdown: Immediate (0x1c): 00000000000001110000 rd (a0 = x10): 01010

Machine Code Format: imm[31:12] | rd | opcode 0000000000000111 | 01010 | 0110111

10.Machine Code for addi a0, a0, 160
Instruction: addi a0, a0, 160 Opcode: 0010011 (7 bits) Immediate: 160 (12 bits) Source Register (rs1): a0 (x10, 5 bits) Destination Register (rd): a0 (x10, 5 bits) Function (funct3): 000 (3 bits)

Breakdown: Immediate (160): 000010100000 rs1 (a0 = x10): 01010 funct3: 000 rd (a0 = x10): 01010

Machine Code Format: imm[11:0] | rs1 | funct3 | rd | opcode 0000101000 | 01010 | 000 | 01010 | 0010011

11.Machine Code for jal ra, printf
Instruction: jal ra, printf Opcode: 1101111 (7 bits) Immediate: Offset (calculated based on PC) Destination Register (rd): ra (x1, 5 bits)

Breakdown: Immediate: Calculated (split into imm[20|10:1|11|19:12]) rd (ra = x1): 00001

Machine Code Format: imm[20|10:1|11|19:12] | rd | opcode xxxxxxxxxxxxxxxxxxxxx | 00001 | 1101111

12.Machine Code for ld ra, 8(sp)
Instruction: ld ra, 8(sp) Opcode: 0000011 (7 bits) Immediate: 8 (12 bits) Source Register (rs1): sp (x2, 5 bits) Destination Register (rd): ra (x1, 5 bits) Function (funct3): 011 (3 bits)

Breakdown: Immediate (8): 0000000001000 rs1 (sp = x2): 00010 funct3: 011 rd (ra = x1): 00001

Machine Code Format: imm[11:0] | rs1 | funct3 | rd | opcode 0000000100 | 00010 | 011 | 00001 | 0000011

13.Machine Code for add sp, sp, 16
Instruction: add sp, sp, 16 Opcode: 0110011 (7 bits) Immediate: Not used (R-type) Source Register (rs1): sp (x2, 5 bits) Source Register (rs2): sp (x2, 5 bits) Destination Register (rd): sp (x2, 5 bits) Function (funct3): 000 (3 bits) Function (funct7): 0000000 (7 bits)

Breakdown: rs1 (sp = x2): 00010 rs2 (sp = x2): 00010 rd (sp = x2): 00010 funct3: 000 funct7: 0000000

14.Machine Code Format: funct7 | rs2 | rs1 | funct3 | rd | opcode 0000000 | 00010 | 00010 | 000 | 00010 | 0110011

Machine Code for ret
Instruction: ret (Expands to: jalr x0, 0(ra)) Opcode: 1100111 (7 bits) Immediate: 0 (12 bits) Source Register (rs1): ra (x1, 5 bits) Destination Register (rd): x0 (5 bits) Function (funct3): 000 (3 bits)

Breakdown: Immediate (0): 000000000000 rs1 (ra = x1): 00001 funct3: 000 rd (x0 = 0): 00000

Machine Code Format: imm[11:0] | rs1 | funct3 | rd | opcode 0000000000 | 00001 | 000 | 00000 | 1100111

15.Machine Code for sd a0, -32(sp)
Instruction: sd a0, -32(sp) Opcode: 0100011 (7 bits) Immediate: -32 (split into imm[11:5] and imm[4:0]) Source Register 1 (rs1): sp (x2, 5 bits) Source Register 2 (rs2): a0 (x10, 5 bits) Function (funct3): 011 (3 bits)

Breakdown: Immediate (-32): 1111111111100000 imm[11:5]: 1111110 imm[4:0]: 00000 rs1 (sp = x2): 00010 rs2 (a0 = x10): 01010 funct3: 011



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
