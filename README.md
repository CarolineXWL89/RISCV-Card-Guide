# Simplified RISC-V Card + Guide

This unofficial card/guide was created for CS61C because the current references that students are directed to are sometimes hard to understand, especially to someone new to RISC-V.


## RV32I Base Integer Instructions

| Mnemonic | Name | FMT | Description | Usage |
|----------|-----|------|-------------|-------|
|`add`      | ADD                     | R  | rd = rs1 + rs2               | `add rd rs1 rs2`
|`sub`      | SUB                     | R  | rd = rs1 - rs2               | `sub rd rs1 rs2`
|`xor`      | XOR                     | R  | rd = rs1 ^ rs2               | `xor rd rs1 rs2`
|`or`       | OR                      | R  | rd = rs1 \| rs2              | `or  rd rs1 rs2`       
|`and`      | AND                     | R  | rd = rs1 & rs2               | `and rd rs1 rs2` 
|`sll`      | Shift Left Logical      | R  | rd = rs1 << rs2              | `sll rd rs1 rs2`
|`srl`      | Shift Right Logical     | R  | rd = rs1 >> rs2              | `srl rd rs1 rs2`
|`sra`      | Shift Right Arith       | R  | rd = rs1 >> rs2              | `sra rd rs1 rs2`
|`slt`      | Set Less Than           | R  | rd = (rs1 < rs2)?1:0         | `slt rd rs1 rs2`
|`sltu`     | Set Less Than (U)       | R  | rd = (rs1 < rs2)?1:0         | `sltu rd rs1 rs2`
|`addi`     | ADD Immediate           | I  | rd = rs1 + imm               | `addi rd rs1 imm`
|`xori`     | XOR Immediate           | I  | rd = rs1 ^ imm               | `xori rd rs1 imm`
|`ori`      | OR Immediate            | I  | rd = rs1 \| imm              | `ori rd rs1 imm`
|`andi`     | AND Immediate           | I  | rd = rs1 & imm               | `andi rd rs1 imm`
|`slli`     | Shift Left Logical Imm  | I  | rd = rs1 << imm              | `slli rd rs1 imm`
|`srli`     | Shift Right Logical Imm | I  | rd = rs1 >> imm              | `srli rd rs1 imm`
|`srai`     | Shift Right Arith Imm   | I  | rd = rs1 >> imm              | `srai rd rs1 imm`
|`slti`     | Set Less Than Imm       | I  | rd = (rs1 < imm)?1:0         | `slti rd rs1 imm`
|`sltiu`    | Set Less Than Imm (U)   | I  | rd = (rs1 < imm)?1:0         | `sltiu rd rs1 imm`
|`lb`       | Load Byte               | I  | rd = M[rs1+imm][0:7]         | `lb rd imm(rs1)`
|`lh`       | Load Half               | I  | rd = M[rs1+imm][0:15]        | `lh rd imm(rs1)`
|`lw`       | Load Word               | I  | rd = M[rs1+imm][0:31]        | `lw rd imm(rs1)`
|`lbu`      | Load Byte (U)           | I  | rd = M[rs1+imm][0:7]         | `lbu rd imm(rs1)`
|`lhu`      | Load Half (U)           | I  | rd = M[rs1+imm][0:15]        | `lhu rd imm(rs1)`
|`sb`       | Store Byte              | S  | M[rs1+imm][0:7]  = rs2[0:7]  | `sb rs2 imm(rs1)`
|`sh`       | Store Half              | S  | M[rs1+imm][0:15] = rs2[0:15] | `sh rs2 imm(rs1)`
|`sw`       | Store Word              | S  | M[rs1+imm][0:31] = rs2[0:31] | `sw rs2 imm(rs1)`
|`beq`      | Branch ==               | B  | if(rs1 == rs2) PC += imm     | `beq rs1 rs2 label`
|`bne`      | Branch !=               | B  | if(rs1 != rs2) PC += imm     | `bne rs1 rs2 label`
|`blt`      | Branch <                | B  | if(rs1 < rs2) PC += imm      | `blt rs1 rs2 label`
|`bge`      | Branch                  | B  | if(rs1 >= rs2) PC += imm     | `bge rs1 rs2 label`
|`bltu`     | Branch < (U)            | B  | if(rs1 < rs2) PC += imm      | `bltu rs1 rs2 label`
|`bgeu`     | Branch >= (U)           | B  | if(rs1 >= rs2) PC += imm     | `bgeu rs1 rs2 label`
|`jal`      | Jump And Link           | J  | rd = PC+4; PC += imm         | `jal label` OR `jal rd label`
|`jalr`     | Jump And Link Reg       | I  | rd = PC+4; PC = rs1 + imm    | `jalr rd` OR `jalr rd imm(rs1)`
|`lui`      | Load Upper Imm          | U  | rd = imm << 12               | `lui rd imm`
|`auipc`    | Add Upper Imm to PC     | U  | rd = PC + (imm << 12)        | `auipc rd imm`
|`ecall`    | Environment Call        | I  | Transfer control to OS       | `ecall`
|`ebreak`   | Environment Break       | I  | Transfer control to debugger | `ebreak`

## Multiply Extension

| Mnemonic | Name | FMT | Description | Usage |
|----------|-----|------|-------------|-------|

## Pseudo instructions

| Mnemonic | Name | FMT | Description | Usage |
|----------|-----|------|-------------|-------|

## About Jumps

##### j
##### jr
##### ret
##### jal
##### jalr

## About Calling Convention

## FAQ

##### What is PC?

##### What is (U)?

##### What is the difference between arithmetic and logical shifting?

##### What does M[] mean?

##### How do I interpret [0:15] 

