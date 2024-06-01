TASK 2

RISC V RISC stands for reduced instruction set computer.It is a 32 bit instruction set.It has various instructions some of the basic and important instructions are R,I,S,B,J.

RISCV has following 5 stages

1)Fetch 2)Decode 3)Execute 4)Memory 5)Writeback

Different Type of Instruction Sets:

1. R-type
2. I-type
3. S-type
4. B-type
5. U-type
6. Jtype

# R-type 
*Used for arithmetic and logical instructions.
*Format: opcode [6:0] | rd [11:7] | funct3 [14:12] | rs1 [19:15] | rs2 [24:20] | funct7 [31:25]
*Example: add x1, x2, x3 (adds the values in registers x2 and x3, and stores the result in x1)

opcode: 0110011
funct7: 0000000
rs2: 00011 (x3)
rs1: 00010 (x2)
funct3: 000
rd: 00001 (x1)'

# I-type (Immediate)
*Used for arithmetic instructions with immediate values, load instructions, and some system instructions.
*Format: opcode [6:0] | rd [11:7] | funct3 [14:12] | rs1 [19:15] | imm [31:20]
*Example: addi x1, x2, 10 (adds the value in register x2 with the immediate value 10, and stores the result in x1)

opcode: 0010011
imm: 000000001010 (10)
rs1: 00010 (x2)
funct3: 000
rd: 00001 (x1)

# S-type (Store)
*Used for store instructions.
*Format: opcode [6:0] | imm[4:0] [11:7] | funct3 [14:12] | rs1 [19:15] | rs2 [24:20] | imm[11:5] [31:25]
*Example: sw x1, 8(x2) (stores the value in register x1 into the memory address computed as x2 + 8)

opcode: 0100011
imm[4:0]: 01000 (8)
rs2: 00001 (x1)
rs1: 00010 (x2)
funct3: 010
imm[11:5]: 0000000

# B-type (Branch)
*Used for conditional branch instructions.
*Format: opcode [6:0] | imm[11] [7] | imm[4:1] [11:8] | funct3 [14:12] | rs1 [19:15] | rs2 [24:20] | imm[10:5] [30:25] | imm[12] [31]
*Example: beq x1, x2, label (branches to label if the values in registers x1 and x2 are equal)

opcode: 1100011
imm[11]: 0
imm[4:1]: 0000
rs2: 00010 (x2)
rs1: 00001 (x1)
funct3: 000
imm[10:5]: 000000
imm[12]: 0

# U-type (Upper Immediate)
*Used for instructions that operate with a 20-bit immediate that is shifted left by 12 bits (e.g., lui and auipc).
*Format: opcode [6:0] | rd [11:7] | imm [31:12]
*Example: lui x1, 0x12345 (loads the upper 20 bits of x1 with the value 0x12345)

opcode: 0110111
imm: 00010010001101000101 (0x12345)
rd: 00001 (x1)

# J-type (Jump)
*Used for jump and link instructions (jal).
*Format: opcode [6:0] | rd [11:7] | imm[19:12] [19:12] | imm[11] [20] | imm[10:1] [30:21] | imm[20] [31]
*Example: jal x1, label (jumps to label and stores the return address in x1)

opcode: 1101111
imm[19:12]: 00000000
imm[11]: 0
imm[10:1]: 0000000000
imm[20]: 0
rd: 00001 (x1)

# Examples of RISC-V Instructions

Arithmetic and Logical Instructions:

add x1, x2, x3: Adds the values in x2 and x3, and stores the result in x1.
sub x1, x2, x3: Subtracts the value in x3 from x2, and stores the result in x1.
and x1, x2, x3: Performs a bitwise AND on x2 and x3, and stores the result in x1.
or x1, x2, x3: Performs a bitwise OR on x2 and x3, and stores the result in x1.

Immediate Instructions:

addi x1, x2, 10: Adds the immediate value 10 to x2, and stores the result in x1.
andi x1, x2, 0xFF: Performs a bitwise AND between x2 and 0xFF, and stores the result in x1.

Load and Store Instructions:

lw x1, 0(x2): Loads the word from the memory address at x2 into x1.
sw x1, 0(x2): Stores the word in x1 into the memory address at x2.

Branch Instructions:

beq x1, x2, label: Branches to label if x1 equals x2.
bne x1, x2, label: Branches to label if x1 does not equal x2.

Upper Immediate Instructions:

lui x1, 0x12345: Loads the upper 20 bits of x1 with the value 0x12345.
auipc x1, 0x12345: Adds the upper 20 bits shifted left by 12 bits of the current PC to x1.

Jump Instructions:

jal x1, label: Jumps to label and stores the return address in x1.
jalr x1, 0(x2): Jumps to the address in x2 and stores the return address in x1.
