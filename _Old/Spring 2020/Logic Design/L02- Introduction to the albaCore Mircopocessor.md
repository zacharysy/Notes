# L02: Introduction to the albaCore Micropocessor

## What Is a Computer
* Contains **Memory** (with Data and  Program/.text) and **Processor**

### Relationships
* Memory sends instructions to processor (one wßay)
* Data is passed between memory and processor (two way)

## albaCore
* Processor that will be used for this course

## Memory
* Is basically a big table with lots of locations

### Address
* The pointer to a row in the table

### Values (Per Row)
* Data in
* Data out
* Control signal (write enabled)
* Bit widths
	* how wide the signal is

## Pointer
* Rows are represented by symbols (such as `A`)
* The address to the row is then `&A`

### Example
* if `A` is an integer and `B` is an array

```
int *pA=&A 
*pA = 7 // Change value in address A

*B = 7 // Changes the first 
```

## Inside the Processor
* Memory
	* Data
	* Text
* CPU
	* Fetch Unit
		* Program Counter (PC)
			* count location in process
		* Controller
	* Execution Unit
		* Register File
			* 16 of them, `r0-r16`
		* Arithmetic Logic Unit (ALU)
			* Has two inputs, which it takes from the register file 
			* outputs it back to register

## Instruction Types
### Arithmetic/Logic
* Does operations of the form `rw <- ra op rb`
* `+,-,&,|,~,>>,<<`

### Memory Access
* Load `ld rw, rb, imm4`
	* memory to register
	* `rw <- M[ra+offset]`
* Store `st ra, rb, imm4`
	* register to memory
	* `M[ra+offset] <- rb`

### Branch
* Used to create conditionals and loops
* Skip instructions
* `PC <- PC + displacement`

#### Unconditional
* `br imm8`
#### If Zero
* `bz rb, imm8`
#### If Negative
* `bn rb, imm8`

### Jump
* Go to specific address
* Used to call functions

#### Jump and Link `jal imm12`
* Jumps to address and sets `r15` to the next memory location after the location of `jal`

#### Jump register `jr ra`
* Jump to address stored in register

## AlbaCore Instructions
* All instructions are 16-bit
	* bits 16:13 - OpCode

### Load Immediate `ldi`
* `| 0x7 | rw | IMM8 |`

### Arithmetic Logic Insructions
* `add`
	* `|0x0|rw|ra|rb|`
* `sub`
	* `|0x1|rw|ra|rb|`