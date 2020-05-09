# 3: Instructions vs Data, ASCII Representation and IEEE 754 Format 
## Arithmetic Logic Unit (ALU)
* Two 1-bit inputs
* MUX: 16-1
* Uses 4 select lines S3-S0
* Performs all operations

### Full ALU
* A bunch of ALUs (like four of them) connected to each other
* Allows for carry bits

## Architecture in Detail
* Control Unit
	* Contains operations
	* It handles the loading of new commands into the CPU and the decoding of these commands. 
	* Also, it directs the data flow and the operation of the ALU. 
* Input Device
	* The input
* Output Device
	* obviously the output
* Register
* ALU
	* (see above)
* Memory Unit


## Memory
### Registers
* Fast and Volatile
	* Does not persist after turning off computer

#### Kinds of Registers
* **Program Counter**
	* holds the memory address of the next instruction. 
* **Memory Access Register**
	* Holds the memory location of data 
	* contains the RAM address of the instruction the CPU wants next. 
* **Memory Data Register**
	* Holds the actual data 
	* MDR holds data that will be written to the RAM or that was read from RAM
* **Accumulator**
	* holds the intermediate results of the currently running instructions. 

### How Computers Organize Memory
#### Memory Hierarchy
* A structure that uses multiple levels of memory in order to improve memory access time
* Performance

#### Principle of Locality
* A program tends to access data that forms a physical cluster in memory

#### Temporal Locality
* If a memory element is referenced, it will tend to be referenced again soon

#### Spacial Locality
* If a memory element is referenced, memory elements whose memory addresses are close by will tend to be referenced soon

### Cache
* Level of memory hierarchy between the processor and main memory
* Used to take advantage of temporal and spatial locality
* Slower than registers but faster than non-volatile memory
* Multiple levels of cache is a design choice used to find the best tradeoff between speed and hardware cost