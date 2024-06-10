# VSDSquadron1

TASK1

The task was to install RISC-V toolchain and the installation is done.

Then the task was to complile the c program which calculates the sum from 1 to n.For this the command to open is "gedit sum1ton.c".
And after the code is written for sum of integers we need to compile it and the following commands were used to accomplish the same.After the compilation the sum value will be printed as shown below.The command to display the output is "./a.out".

![WhatsApp Image 2024-05-21 at 9 16 54 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/22081e20-03fb-4d4a-a331-5284ac627e41)

![WhatsApp Image 2024-05-21 at 9 15 40 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/c0db19f5-9787-4ea6-84f1-0e76102e7ef0)

![WhatsApp Image 2024-05-21 at 9 16 54 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/6ac14dcc-ce01-4e47-936c-e905dd818197)

Next to compile the same code with RISC-V compiler.
For that we need to open the code in terminal itself.Command to open is "cat sum1ton.c" as shown below.

![WhatsApp Image 2024-05-21 at 9 19 04 PM (1)](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/11f76780-7e05-4eb3-995d-3a65ea1c041d)

Then the following command is used to create .o file as shown below.

![WhatsApp Image 2024-05-21 at 9 30 15 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/54eb1fe8-fb2c-4391-b949-c46213d1b8e3)

Then to open the assembly level instructions for the above written c code  we use the following command

![WhatsApp Image 2024-05-21 at 9 34 44 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/6231d6f1-1ba2-4780-8c17-32520eda5b9e)

Then a huge set of instructions are generated as shown below.

![WhatsApp Image 2024-05-21 at 9 36 26 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/30a00e8f-9ffa-45e5-8eb0-09c48582fe1f)

In this code lets search for the "main".

![WhatsApp Image 2024-05-21 at 9 39 49 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/dd7480ce-c71c-4dc1-8cf9-c7b8c6924b26)

 if we subtract 101b0-10184 it is 11 so there are 11 instructions in this above assembly code in the "main".

To reduce the number of instructions we add"|less"  along with the above command which  generates less assembly code instructions in this we are mainly concerned about main so to search we use "/main" and this is how it looks.

Next we can compile in other way as shown below

![WhatsApp Image 2024-05-21 at 10 04 10 PM](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/85b7bb3c-acf4-42cd-9c7d-136dd0118ff0)

![WhatsApp Image 2024-05-21 at 10 03 23 PM (1)](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/b04e9e0b-e423-43a4-a9fd-afb63d17e1cf)

The number of instructions hasn't changed because it was a simple program.


TASK 2

RISC V
RISC stands for reduced instruction set computer.It is a 32 bit instruction set.It has various instructions some of the basic and important instructions are R,I,S,B,J.

RISCV has foloowing 5 stages

1)Fetch
2)Decode
3)Execute
4)Memory
5)Writeback

R-TYPE

R-type format is used to carry out various operations, including arithmetic and logical instructions.
Due to the fact that these instructions operate on two register operands, they facilitate the effective execution of various operations. 
Here R stands for Register.It has 3 registers rs1,rs2 are the source registers and rd is the destination register and R-type instruction has 6 fields such as func7 which is of 7 bits,rs2 5 bits,rs1 5bits,func3 3 bits,rd 5 bits,op which stands for operational code which tells what the instruction do is of 7 bits as shown below.

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/2d42cbe4-37bd-4ea8-8632-7eeb85e7d1ee)

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/1e3552d9-c9e4-42b0-81b2-9d9c640ae00c)

Let us see the above example for R-type instruction.The first  instruction performs addition operation which has two source registers and 1 destination register where the computed value gets stored.Second instruction performs subtraction operation and as we can see both the instructions has the same opcode value but the source registers,func7.destination registers are different these are the parameters that are considered for differentiating above two instructions.

The various operation executed in R-type format is as shown below.

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/aee7c752-dbdd-4109-bc5c-bd965f5b5658)

I-type

Here I stands for immediate.THe immediate is a 12 bit signed number which is used for arithmetic and logical instructions as well as for load type instructions.

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/d63cdd0f-dbcb-4f62-8f5e-50afc43b1d73)

Some of the examples of I-type format is shown below.

Add Immediate (ADDI):

Adds an immediate value to a register and stores the result in a destination register.
Syntax: ADDI rd, rs1, imm
Example: ADDI x1, x2, 10 (x1 = x2 + 10)

Load Word (LW):

Loads a word from memory into a register.
Syntax: LW rd, offset(rs1)
Example: LW x1, 4(x2) (x1 = M[x2 + 4])

so here in this above instruction the data which is present at the address (X2+4) gets loaded into the destination register X1.

Sets the destination register to 1 if the source register is less than the immediate value, otherwise sets it to 0.
Syntax: SLTI rd, rs1, imm
Example: SLTI x1, x2, 5 (x1 = (x2 < 5) ? 1 : 0)

so here if X2 value is less than 5 then the value of X1 gets set to 1 else 0.

Bitwise AND Immediate (ANDI):

Performs a bitwise AND operation between a register and an immediate value, storing the result in a destination register.
Syntax: ANDI rd, rs1, imm
Example: ANDI x1, x2, 15 (x1 = x2 & 15)

Shift Left Logical Immediate (SLLI):

Shifts the bits in the source register to the left by the number of positions specified by the immediate value, storing the result in the destination register.
Syntax: SLLI rd, rs1, shamt (where shamt is the shift amount)
Example: SLLI x1, x2, 3 (x1 = x2 << 3)

Consider the ADDI instruction:

ADDI x1, x2, 10:
Immediate (imm): 10 (0b0000001010)
Source register (rs1): x2 (2 in decimal, 0b00010 in binary)
Destination register (rd): x1 (1 in decimal, 0b00001 in binary)
funct3: 000 (for ADDI)
opcode: 0010011 (for I-type arithmetic instructions)
The instruction encoding would be:

imm[11:0]: 000000001010 (12-bit binary representation of 10)
rs1: 00010
funct3: 000
rd: 00001
opcode: 0010011
Putting it all together:
000000001010 00010 000 00001 0010011

In hexadecimal, it would be:
0x00510093.


S-type
Here S refers to store,where the data from the particular address will get stored in to the memory location.

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/84192a0a-3867-4af5-a772-0517f69e4476)

Let us see some of the S-type format.

1) Store Byte (SB):

Stores a byte (8 bits) from a register to memory.

Syntax: SB rs2, offset(rs1)
Example: SB x3, 4(x5) (Store the least significant byte of x3 at the address x5 + 4).

2) Store Halfword (SH):

Stores a halfword (16 bits) from a register to memory.
Syntax: SH rs2, offset(rs1)
Example: SH x3, 4(x5) (Store the least significant 16 bits of x3 at the address x5 + 4)

3) Store Word (SW):

Stores a word (32 bits) from a register to memory.
Syntax: SW rs2, offset(rs1)
Example: SW x3, 4(x5) (Store the 32-bit value of x3 at the address x5 + 4)

Examples of S-type instructions

Consider the SW instruction:

SW x3, 20(x5):
Immediate (imm): 20 (0b00000000010100)
Source register 2 (rs2): x3 
Source register 1 (rs1): x5 
funct3: 010 (for SW)
opcode: 0100011 (for store instructions)
The immediate is split into imm[11:5] and imm[4:0]:

imm[11:5]: 0000000
imm[4:0]: 10100
The instruction encoding would be:

imm[11:5]: 0000000
rs2: 00011
rs1: 00101
funct3: 010
imm[4:0]: 10100
opcode: 0100011
Putting it all together:
0000000 00011 00101 010 10100 0100011

In hexadecimal, it would be:
0x01430223.

B-type

Here B refers to branch type.This is especially used when a conditional statement is executed and up on the condition satisfied it branches to other instruction.

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/43d5ad28-0c4b-4646-b839-b620f7ed3d2e)

The branch target address is calculated using an immediate offset added to the current PC.

Common B-Type Instructions
Branch if Equal (BEQ):

Branches to the target address if the values in rs1 and rs2 are equal.
Syntax: BEQ rs1, rs2, offset
Example: BEQ x1, x2, 16 (Branch to PC + 16 if x1 equals x2)
Branch if Not Equal (BNE):

Branches to the target address if the values in rs1 and rs2 are not equal.
Syntax: BNE rs1, rs2, offset
Example: BNE x1, x2, 16 (Branch to PC + 16 if x1 does not equal x2)
Branch if Less Than (BLT):

Branches to the target address if the value in rs1 is less than the value in rs2 (signed comparison).
Syntax: BLT rs1, rs2, offset
Example: BLT x1, x2, 16 (Branch to PC + 16 if x1 is less than x2)
Branch if Greater or Equal (BGE):

Branches to the target address if the value in rs1 is greater than or equal to the value in rs2 (signed comparison).
Syntax: BGE rs1, rs2, offset
Example: BGE x1, x2, 16 (Branch to PC + 16 if x1 is greater than or equal to x2)
Branch if Less Than Unsigned (BLTU):

Branches to the target address if the value in rs1 is less than the value in rs2 (unsigned comparison).
Syntax: BLTU rs1, rs2, offset
Example: BLTU x1, x2, 16 (Branch to PC + 16 if x1 is less than x2)
Branch if Greater or Equal Unsigned (BGEU):

Branches to the target address if the value in rs1 is greater than or equal to the value in rs2 (unsigned comparison).
Syntax: BGEU rs1, rs2, offset
Example: BGEU x1, x2, 16 (Branch to PC + 16 if x1 is greater than or equal to x2).

Example for B-type instruction

BEQ x1, x2, 16

Immediate (imm): 16 (0b0000000010000)

The immediate is split into imm[12|10:5|4:1|11]:

imm[12]: 0
imm[10:5]: 000000
imm[4:1]: 1000
imm[11]: 0

The instruction encoding would be:

imm[12]: 0
imm[10:5]: 000000
rs2: 00010
rs1: 00001
funct3: 000
imm[4:1]: 1000
imm[11]: 0
opcode: 1100011

Putting it all together:
0000000 00010 00001 000 1000 0 1100011

In hexadecimal, it would be:
0x00810263.

U-type

Here U refers to Upper immediate.

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/34f61f4c-2fab-4a01-9a58-9bb4346ef4a2)

U-type instructions in RISC-V are crucial for handling large immediate values, particularly useful for loading constants or computing addresses. The two main U-type instructions, LUI and AUIPC, enable the manipulation of the upper 20 bits of a register and facilitate operations involving large constants and PC-relative addressing.

Load Upper Immediate (LUI):

The LUI instruction loads a 20-bit immediate value into the upper 20 bits of the destination register, setting the lower 12 bits to zero.
Syntax: LUI rd, imm
Example: LUI x1, 0x12345 (loads 0x12345000 into x1)

Add Upper Immediate to PC (AUIPC):

The AUIPC instruction adds a 20-bit immediate value shifted left by 12 bits to the program counter (PC) and stores the result in the destination register.
Syntax: AUIPC rd, imm
Example: AUIPC x1, 0x12345 (stores PC + 0x12345000 into x1)

Example of U-type instruction

LUI x1, 0x12345:
Immediate (imm): 0x12345 (20 bits)
Destination register (rd): x1 (1 in decimal, 0b00001 in binary)
Opcode: 0110111 (for LUI)
The instruction encoding would be:

imm: 0001 0010 0011 0100 0101 (0x12345)
rd: 00001
opcode: 0110111
Putting it all together:
0001 0010 0011 0100 0101 00001 0110111

In hexadecimal, it would be:
0x12345037.

J-type

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/c296d143-8dd5-4f65-8c11-1056fd13101c)

J-type instructions in RISC-V, primarily JAL, are essential for implementing control flow in programs, allowing jumps to specified addresses and storing return addresses for subroutine calls. 

Jump and Link (JAL):
The JAL instruction jumps to a target address and stores the return address in a register.
Syntax: JAL rd, offset
Example: JAL x1, 1024 (jumps to the address PC + 1024 and stores the return address in x1)

Example of J-type instruction 

JAL x1, 1024:
Immediate (offset): 1024 (0x400, in binary: 0000 0100 0000 0000)
Destination register (rd): x1 (1 in decimal, 0b00001 in binary)
Opcode: 1101111 (for JAL)
To encode the immediate value, it needs to be broken down and placed into the instruction format:

imm[20] = 0
imm[10:1] = 0000000001 
imm[11] = 0
imm[19:12] = 00000000
Putting it all together, the instruction fields would be:

imm: 0 0000000001 0 00000000
rd: 00001
opcode: 1101111
In binary, it would be:
00000000001000000000000011101111

"Identify various RISC-V instruction type (R, I, S, B, U, J) and exact 32-bit instruction code in the instruction type format for below RISC-V instructions 
ADD r6, r2, r1(R-type)

SUB r7, r1, r2(R-type

AND r8, r1, r3(R-type)

OR r9, r2, r5(R-type)

XOR r10, r1, r4(R-type)

SLT r11, r2, r4(R-type)

ADDI r12, r4, 5(I-type)

SW r3, r1, 2(S-type)

SRL r16, r14, r2(R-type)

BNE r0, r1, 20(B-type)

BEQ r0, r0, 15(B-type)

LW r13, r1, 2(I-type)

SLL r15, r1, r2(R-type)

TASK3

In this task we were assigned to execute the instructions in the platform that were given in task2.
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/73cf043c-821d-47fc-8de7-e0bb104ae706)

As we know RISCV can execute all the basic instructions like add,sub,and,xor,beq we are verifying all these instructions.

Icarus Verilog, often abbreviated as iverilog, is a popular open-source Verilog simulation and synthesis tool. Verilog is a hardware description language (HDL) used to model electronic systems. Icarus Verilog allows developers and engineers to write, compile, and simulate Verilog code, making it an essential tool for digital design verification and testing.

 Icarus Verilog can simulate complex Verilog designs, allowing users to verify the behavior of their digital circuits before physical implementation.

GTKWave

GTKWave is an open-source waveform viewer designed for use with digital simulation output. It is often used in conjunction with simulation tools like Icarus Verilog to visualize the signal changes over time within a digital circuit.

Waveform Viewing: Allows users to view and analyze the output waveforms from digital simulations, providing insights into the timing and functionality of their designs.
Support for Multiple Formats: It supports several file formats including VCD (Value Change Dump), LXT, FST, and GHW, among others.
So these two need to be installed as shown below.
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/d5592f32-86cc-43c3-b7bf-58dfdde750fc)

So now to execute all of this we need verilog file and its test bench,we were given a github repo.
So the main module and its testbench  were copied in to my repo as shown below.

https://github.com/harika-veluru/rv32i1.git

So the main module is iiitb_rv32i.v and the test bench is iiitb_rv32i_tb.v 

  
MEM[0] <= 32'h02208300;         // add r6,r1,r2.(i1)
MEM[1] <= 32'h02209380;         //sub r7,r1,r2.(i2)
MEM[2] <= 32'h0230a400;         //and r8,r1,r3.(i3)
MEM[3] <= 32'h02513480;         //or r9,r2,r5.(i4)
MEM[4] <= 32'h0240c500;         //xor r10,r1,r4.(i5)
MEM[5] <= 32'h02415580;         //slt r11,r2,r4.(i6)
MEM[6] <= 32'h00520600;         //addi r12,r4,5.(i7)
MEM[7] <= 32'h00209181;         //sw r3,r1,2.(i8)
MEM[8] <= 32'h00208681;         //lw r13,r1,2.(i9)
MEM[9] <= 32'h00f00002;         //beq r0,r0,15.(i10)
MEM[25] <= 32'h00210700;         //add r14,r2,r2.(i11)

These corresponding instructions which are 32 bit are executed.
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/e579ca01-b104-40ec-a506-6207a06ced3c)

Now rv32i1 has both the main module and the testbench as shown above
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/14b1da07-8c07-4eed-9520-f0dfeade413a)

The command to open the waveform is

iverilog -o rv32i1 iiitb_rv32i.v iiitb_rv32i_tb.v
./rv32i1

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/cf3d99f3-b6a4-4326-8ca6-1b3420e307aa)

Now the environment for simulation opens and lets see all the instructions present in the above verilog code.

The instructions here are hardcoded.
1)ADD 
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/243ddfca-6b72-479c-b7d0-bd3dcebd4368)

2)SUB
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/bfbb08f7-ffdb-45a6-87b6-e15bd89819ed)

3)AND
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/30cd2635-e4f1-4b2d-a526-318a73ec8425)

4)OR
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/bb672290-5413-4efd-b2ac-02a4a79eac70)

5)XOR
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/6ea42ddd-2bf7-470a-b925-f8ad4b4a788f)

6)SLT
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/c3bddc3f-f56d-4b08-aff7-6e83da95182e)

7)ADDI
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/9f858d7e-d207-4332-b589-bb26f7fd2c4a)

8)SW
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/26ab5565-3344-4952-8ca3-8d0b7a8d1288)

9)LW
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/26b83927-0757-4e3d-ae4e-a06126359ba9)

10)BEQ
![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/9410dba7-6844-48b2-8a04-6f2dea34cf93)



Next the yosys install was done using sudo apt install yosys

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/d2967a86-a75b-4432-aad1-cd0269f8c798)

Next script.ys was created and the following contents were written and the command to open script is "nano script.ys"

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/2ddb4967-e405-480d-86b4-71ba5806d347)

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/c031c55f-a127-41f7-b5d0-0211176c3b46)

The synthesis.v file is created as shown above.



TASK4

To describe a basic digital circulit to implement on vsdquadronmini

so the circuit i have choosen is 1:4 demultiplexer

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/133844a6-c4c5-4a93-9ac1-5692a4142262)

![image](https://github.com/harika-veluru/VSDSquadron1/assets/136460261/3be16cac-b6c7-40f6-af87-b5e712b89d48)

I have drawn the circuit using draw.io 

The components required are 

1)VSD quadronmini.
2)Breadboard.
3)pushbuttons.
4)leds.
5)connecting wires.

I am using 2 push buttons that are used as select buttons,

a)If pushbutton1 is off and pushbutton2 is also off then led1 and led2 will be off.

b)If pushbutton1 is off and pushbutton2 is on then led1 will be off and led2 will glow.

c)If pushbutton1 is on and pushbutton2 is off then led1 will glow and led2 will be off.

d)If pushbutton1 and pushbutton2 is on then led1 and led2 will glow.


TASK5
To implement 1:4 demux on VSDSquadronMini.
The following code was used to implement the above said circuit.

code


