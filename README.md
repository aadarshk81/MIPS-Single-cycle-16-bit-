# MIPS 16-bit Single cycle processor
![Datapath](https://user-images.githubusercontent.com/46645257/89717885-490d6780-d9d8-11ea-9fd3-756eed49fc36.png)

MIPS (Microprocessor without Interlocked Pipelined Stages) is a reduced instruction set computer (RISC) instruction set architecture (ISA). In this project I developed 16-bit Single Cycle MIPS processor. A single cycle processor is a processor that carries out one instruction in a single clock cycle.

In MIPS architecture there are 3 types of Instructions. The type of Instruction is identified using the first 3 bits of 16 bit word called as opcode. These are-:
* **R-type-** This type consists of arithmetic and logical instructions. Identified by '000' as opcode.
* **I-type-** These are immediate instructions. They requie sign extension. Identified by rest representations.
* **J-type-** These are jump instructions. Identified by '010' and '011' as opcode.

The Instruction format in MIPS architecture is as follows.
![Isa](https://user-images.githubusercontent.com/46645257/89718432-28dfa780-d9dc-11ea-8305-69c7240d7915.png)
