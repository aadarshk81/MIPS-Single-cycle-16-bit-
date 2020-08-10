# MIPS 16-bit Single cycle processor
![Datapath](https://user-images.githubusercontent.com/46645257/89717885-490d6780-d9d8-11ea-9fd3-756eed49fc36.png)

MIPS (Microprocessor without Interlocked Pipelined Stages) is a reduced instruction set computer (RISC) instruction set architecture (ISA). In this project I developed 16-bit Single Cycle MIPS processor. A single cycle processor is a processor that carries out one instruction in a single clock cycle.

## ISA
In MIPS architecture there are 3 types of Instructions. The type of Instruction is identified using the first 3 bits of 16 bit word called as opcode. These are-:
* **R-type-** This type consists of arithmetic and logical instructions. Identified by '000' as opcode.
* **I-type-** These are immediate instructions. They requie sign extension. Identified by rest representations.
* **J-type-** These are jump instructions. Identified by '010' and '011' as opcode.

The Instruction format in MIPS architecture is as follows.
![Isa](https://user-images.githubusercontent.com/46645257/89718432-28dfa780-d9dc-11ea-8305-69c7240d7915.png)                             
The instructions in a type with example is shown in following table-
![ex](https://user-images.githubusercontent.com/46645257/89728724-0b96f180-da4d-11ea-86c3-14e4c0738469.png)

## Control Unit
The control unit in MIPS processor or any other processor is an essential part. It is responsible for generating signals such as RegWrite(tell whether data need to be written in Reg), it also handles crucial signals of ALU which tell which operation to perform and many more signals.
The Input to the control unit is [15:13] bits of the 16 bit instruction.

Following table summarises different signals and what value each of them hold for a instruction.

![control signals](https://user-images.githubusercontent.com/46645257/89728830-c7f0b780-da4d-11ea-881f-fb1ecb3371f4.png)

## ALU Control
This unit tells ALU what operation need to be done on the basis of signal ALUOp received from mail control unit. The following table describes the operation on basis of ALUOp.
![Annotation 2020-08-10 214638](https://user-images.githubusercontent.com/46645257/89805276-091ebf80-db53-11ea-9e39-fddc0d9292b8.png)

## Register File
These are the registers from which data is read and onto which data is wrtten. There are 8 registers which can store 16-bit word. It has in total 7 inputs. Clock, Reset, two 3-bit addresses to know from which register data needs to be read, one 3-bit address to know in which register the data needs to be written, one control signal RegWrite which is enabled when data need to be written in register and one 16-bit data which need to be written. There are two 16-bit outpus which has the data read from two registers.
