# README

## Details

**Name:** Vikas KA  
**College:** Sahyadri College of Engineering and Management, Mangalore  
**Email:** [vikaska9945@gmail.com](mailto:vikaska9945@gmail.com) / [vikas.ec23@sahyadri.edu.in](mailto:vikas.ec23@sahyadri.edu.in)

---

## Tasks

<details>
<summary>▶ Task 1: Development of C Program</summary>

### Files:
1. [C-programming output snapshot](./Task1/c%20programm%20output%20snapshot.png)
2. [RISC-V (O1, Ofast)](./Task1/riscv%20(O1,Ofast).png)
3. [RISC-V 1 (O1)](./Task1/riscv%201(O1).png)
4. [RISC-V 2 (Ofast)](./Task1/riscv%202%20(Ofast).png)
5. [Ubuntu screenshot](./Task1/ubuntu%20screenshot.png)

</details>

<details>
<summary>▶ Task 2: Simulation with Spike</summary>

### Files:
1. [C code compiled for Spike simulation](./Task2/C%20code%20complied%20or%20spike%20simulation.png)
2. [Debugging screenshot](./Task2/Debugging.png)
3. [Objdump using -O1 format](./Task2/Objdump%20using%20-O1%20farmat.png)
4. [Objdump using -Ofast format](./Task2/Objdump%20using%20-Ofast%20format.png)

</details>

<details>
<summary>▶ Task 3: Machine Code Instructions</summary>

### File:
- [Instructions.md](./Task3/instructions.md)

### Content:

#### Machine Code for `addi sp, sp, -16`
- **Instruction:** `addi sp, sp, -16`  
- **Opcode:** `0010011` (7 bits)  
- **Immediate:** `-16` (12 bits, two's complement)  
- **Source Register (rs1):** `sp (x2)` (5 bits)  
- **Destination Register (rd):** `sp (x2)` (5 bits)  
- **Function (funct3):** `000` (3 bits)  

**Breakdown:**
- Immediate (-16): `111111111100`  
- rs1 (sp = x2): `00010`  
- funct3: `000`  
- rd (sp = x2): `00010`  

**Machine Code Format:**  
`imm[11:0] | rs1 | funct3 | rd | opcode`  
`1111111100 | 00010 | 000 | 00010 | 0010011`

---

#### Machine Code for `sd ra, 8(sp)`
- **Instruction:** `sd ra, 8(sp)`  
- **Opcode:** `0100011` (7 bits)  
- **Immediate:** `8` (12 bits, split into `imm[11:5]` and `imm[4:0]`)  
- **Source Register (rs2):** `ra (x1)` (5 bits)  
- **Base Register (rs1):** `sp (x2)` (5 bits)  
- **Function (funct3):** `011` (3 bits)  

**Breakdown:**
- Immediate (8): `0000000001000`  
- rs2 (ra = x1): `00001`  
- rs1 (sp = x2): `00010`  
- funct3: `011`  

**Machine Code Format:**  
`imm[11:5] | rs2 | rs1 | funct3 | imm[4:0] | opcode`  
`0000000 | 00001 | 00010 | 011 | 00000 | 0100011`

---

#### Machine Code for `li a5, 100`
- **Instruction:** `li a5, 100` (Expands to: `addi a5, x0, 100`)  
- **Opcode:** `0010011` (7 bits)  
- **Immediate:** `100` (12 bits)  
- **Source Register (rs1):** `x0 (constant 0)` (5 bits)  
- **Destination Register (rd):** `a5 (x15)` (5 bits)  
- **Function (funct3):** `000` (3 bits)  

**Breakdown:**
- Immediate (100): `00000001100100`  
- rs1 (x0 = 0): `00000`  
- funct3: `000`  
- rd (a5 = x15): `01111`  

**Machine Code Format:**  
`imm[11:0] | rs1 | funct3 | rd | opcode`  
`0000001100 | 00000 | 000 | 01111 | 0010011`

---

#### Machine Code for `addiw a5, a5, -1`
- **Instruction:** `addiw a5, a5, -1`  
- **Opcode:** `0011011` (7 bits)  
- **Immediate:** `-1` (12 bits, two's complement)  
- **Source Register (rs1):** `a5 (x15)` (5 bits)  
- **Destination Register (rd):** `a5 (x15)` (5 bits)  
- **Function (funct3):** `000` (3 bits)  

**Breakdown:**
- Immediate (-1): `111111111111`  
- rs1 (a5 = x15): `01111`  
- funct3: `000`  
- rd (a5 = x15): `01111`  

**Machine Code Format:**  
`imm[11:0] | rs1 | funct3 | rd | opcode`  
`1111111111 | 01111 | 000 | 01111 | 0011011`

---



</details>
