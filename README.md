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

### Machine Code Instructions:

#### 1. **Instruction: addi sp, sp, -16**

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

#### 2. **Instruction: addi x5, x0, 8**

- **Opcode:** 0010011 (7 bits)  
- **Immediate:** 8 (12 bits)  
- **Source Register (rs1):** x0 (5 bits)  
- **Destination Register (rd):** x5 (5 bits)  
- **Function (funct3):** 000 (3 bits)  

**Breakdown:**
- Immediate (8): 000000001000  
- rs1 (x0 = 0): 00000  
- funct3: 000  
- rd (x5 = x5): 00101  

**Machine Code Format:**  
imm[11:0] | rs1 | funct3 | rd | opcode  
000000001000 | 00000 | 000 | 00101 | 0010011

---

#### 3. **Instruction: add x6, x7, x8**

- **Opcode:** 0110011 (7 bits)  
- **Source Register 1 (rs1):** x7 (5 bits)  
- **Source Register 2 (rs2):** x8 (5 bits)  
- **Destination Register (rd):** x6 (5 bits)  
- **Function (funct3):** 000 (3 bits)  
- **Function (funct7):** 0000000 (7 bits)

**Breakdown:**
- rs1 (x7): 00111  
- rs2 (x8): 01000  
- funct3: 000  
- rd (x6): 00110  
- funct7: 0000000  

**Machine Code Format:**  
funct7 | rs2 | rs1 | funct3 | rd | opcode  
0000000 | 01000 | 00111 | 000 | 00110 | 0110011

---

#### 4. **Instruction: lw x1, 0(x2)**

- **Opcode:** 0000011 (7 bits)  
- **Immediate:** 0 (12 bits)  
- **Base Register (rs1):** x2 (5 bits)  
- **Destination Register (rd):** x1 (5 bits)  
- **Function (funct3):** 010 (3 bits)  

**Breakdown:**
- Immediate (0): 000000000000  
- rs1 (x2 = 2): 00010  
- funct3: 010  
- rd (x1 = 1): 00001  

**Machine Code Format:**  
imm[11:0] | rs1 | funct3 | rd | opcode  
000000000000 | 00010 | 010 | 00001 | 0000011

---

#### 5. **Instruction: sw x1, 0(x2)**

- **Opcode:** 0100011 (7 bits)  
- **Immediate:** 0 (12 bits)  
- **Base Register (rs1):** x2 (5 bits)  
- **Source Register (rs2):** x1 (5 bits)  
- **Function (funct3):** 010 (3 bits)  

**Breakdown:**
- Immediate (0): 000000000000  
- rs1 (x2 = 2): 00010  
- funct3: 010  
- rs2 (x1 = 1): 00001  

**Machine Code Format:**  
imm[11:5] | rs2 | rs1 | funct3 | imm[4:0] | opcode  
0000000 | 00001 | 00010 | 010 | 00000 | 0100011

---

#### 6. **Instruction: jal x1, 1000**

- **Opcode:** 1101111 (7 bits)  
- **Immediate:** 1000 (20 bits)  
- **Destination Register (rd):** x1 (5 bits)  
- **Function (funct3):** 000 (3 bits)  

**Breakdown:**
- Immediate (1000): 00000000000000111100  
- rd (x1): 00001  
- funct3: 000  

**Machine Code Format:**  
imm[20] | imm[10:1] | imm[11] | imm[19:12] | rd | opcode  
0 | 0000000011 | 1 | 000000000000 | 00001 | 1101111

---

#### 7. **Instruction: and x9, x5, x8**

- **Opcode:** 0110011 (7 bits)  
- **Source Register 1 (rs1):** x5 (5 bits)  
- **Source Register 2 (rs2):** x8 (5 bits)  
- **Destination Register (rd):** x9 (5 bits)  
- **Function (funct3):** 111 (3 bits)  
- **Function (funct7):** 0000000 (7 bits)

**Breakdown:**
- rs1 (x5): 00101  
- rs2 (x8): 01000  
- funct3: 111  
- rd (x9): 01001  
- funct7: 0000000  

**Machine Code Format:**  
funct7 | rs2 | rs1 | funct3 | rd | opcode  
0000000 | 01000 | 00101 | 111 | 01001 | 0110011

---

#### 8. **Instruction: or x10, x5, x6**

- **Opcode:** 0110011 (7 bits)  
- **Source Register 1 (rs1):** x5 (5 bits)  
- **Source Register 2 (rs2):** x6 (5 bits)  
- **Destination Register (rd):** x10 (5 bits)  
- **Function (funct3):** 110 (3 bits)  
- **Function (funct7):** 0000000 (7 bits)

**Breakdown:**
- rs1 (x5): 00101  
- rs2 (x6): 00110  
- funct3: 110  
- rd (x10): 01010  
- funct7: 0000000  

**Machine Code Format:**  
funct7 | rs2 | rs1 | funct3 | rd | opcode  
0000000 | 00110 | 00101 | 110 | 01010 | 0110011

---

#### 9. **Instruction: xor x11, x5, x6**

- **Opcode:** 0110011 (7 bits)  
- **Source Register 1 (rs1):** x5 (5 bits)  
- **Source Register 2 (rs2):** x6 (5 bits)  
- **Destination Register (rd):** x11 (5 bits)  
- **Function (funct3):** 100 (3 bits)  
- **Function (funct7):** 0000000 (7 bits)

**Breakdown:**
- rs1 (x5): 00101  
- rs2 (x6): 00110  
- funct3: 100  
- rd (x11): 01011  
- funct7: 0000000  

**Machine Code Format:**  
funct7 | rs2 | rs1 | funct3 | rd | opcode  
0000000 | 00110 | 00101 | 100 | 01011 | 0110011

---

#### 10. **Instruction: slli x7, x8, 3**

- **Opcode:** 0010011 (7 bits)  
- **Immediate:** 3 (12 bits)  
- **Source Register (rs1):** x8 (5 bits)  
- **Destination Register (rd):** x7 (5 bits)  
- **Function (funct3):** 001 (3 bits)  
- **Function (funct7):** 0000000 (7 bits)

**Breakdown:**
- Immediate (3): 000000000011  
- rs1 (x8): 01000  
- funct3: 001  
- rd (x7): 00111  
- funct7: 0000000  

**Machine Code Format:**  
funct7 | imm[5:0] | rs1 | funct3 | rd | opcode  
0000000 | 000011 | 01000 | 001 | 00111 | 0010011

---

#### 11. **Instruction: srli x7, x8, 4**

- **Opcode:** 0010011 (7 bits)  
- **Immediate:** 4 (12 bits)  
- **Source Register (rs1):** x8 (5 bits)  
- **Destination Register (rd):** x7 (5 bits)  
- **Function (funct3):** 101 (3 bits)  
- **Function (funct7):** 0000000 (7 bits)

**Breakdown:**
- Immediate (4): 000000000100  
- rs1 (x8): 01000  
- funct3: 101  
- rd (x7): 00111  
- funct7: 0000000  

**Machine Code Format:**  
funct7 | imm[5:0] | rs1 | funct3 | rd | opcode  
0000000 | 000100 | 01000 | 101 | 00111 | 0010011

---

#### 12. **Instruction: beq x5, x6, 256**

- **Opcode:** 1100011 (7 bits)  
- **Immediate:** 256 (12 bits)  
- **Source Register 1 (rs1):** x5 (5 bits)  
- **Source Register 2 (rs2):** x6 (5 bits)  
- **Function (funct3):** 000 (3 bits)  

**Breakdown:**
- Immediate (256): 000000010000  
- rs1 (x5): 00101  
- rs2 (x6): 00110  
- funct3: 000  

**Machine Code Format:**  
imm[12] | imm[10:5] | rs2 | rs1 | funct3 | imm[4:1] | imm[11] | opcode  
0 | 000010 | 00110 | 00101 | 000 | 0000 | 0 | 1100011

---

#### 13. **Instruction: bne x5, x6, 512**

- **Opcode:** 1100011 (7 bits)  
- **Immediate:** 512 (12 bits)  
- **Source Register 1 (rs1):** x5 (5 bits)  
- **Source Register 2 (rs2):** x6 (5 bits)  
- **Function (funct3):** 001 (3 bits)  

**Breakdown:**
- Immediate (512): 000001000000  
- rs1 (x5): 00101  
- rs2 (x6): 00110  
- funct3: 001  

**Machine Code Format:**  
imm[12] | imm[10:5] | rs2 | rs1 | funct3 | imm[4:1] | imm[11] | opcode  
0 | 000100 | 00110 | 00101 | 001 | 0000 | 0 | 1100011

---

#### 14. **Instruction: j x9, 1024**

- **Opcode:** 1101111 (7 bits)  
- **Immediate:** 1024 (20 bits)  
- **Destination Register (rd):** x9 (5 bits)  

**Breakdown:**
- Immediate (1024): 00000000000000000100  
- rd (x9): 01001  

**Machine Code Format:**  
imm[20] | imm[10:1] | imm[11] | imm[19:12] | rd | opcode  
0 | 0000000001 | 0 | 000000000100 | 01001 | 1101111

---

#### 15. **Instruction: xor x10, x11, x12**

- **Opcode:** 0110011 (7 bits)  
- **Source Register 1 (rs1):** x11 (5 bits)  
- **Source Register 2 (rs2):** x12 (5 bits)  
- **Destination Register (rd):** x10 (5 bits)  
- **Function (funct3):** 100 (3 bits)  
- **Function (funct7):** 0000000 (7 bits)

**Breakdown:**
- rs1 (x11): 01011  
- rs2 (x12): 01100  
- funct3: 100  
- rd (x10): 01010  
- funct7: 0000000  

**Machine Code Format:**  
funct7 | rs2 | rs1 | funct3 | rd | opcode  
0000000 | 01100 | 01011 | 100 | 01010 | 0110011



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
