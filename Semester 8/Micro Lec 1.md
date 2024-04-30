
## ***Computer and its Organizations :***

- ##### *consists of 5 parts (input, output, ALU, control unit, memory unit)*

### input unit :
  - read the data into the machine.
### output unit :
- display the output result after the ALU processing.

### Central processing unit :
##### ALU (Arithematic logic unit):
- used for performing the arithmetic & logical operations on data.
##### Control unit:
- central nervous system
- controls all other units and the flow of data for performing computations or sequences operations with the help of the clock.
- #### **Consists of**
    - program counter : contain the address of the current instruction.
    - stack pointer : in CPU or main memory, point to the next available memory location in the stack, (push & pop) are instruction used with it.
    - instruction register :  store the instruction read from memory and should be decoded to generate control sequence.
    - ![[Screenshot 2024-02-24 012749.png]]

### memory unit:
- stores 2 types of Informations (data and program)
- RAM is the main memory
- read/write performed using two registers. memory address register (MAR) -> contain the address ,memory buffer register (MBR) -> data to be written or data after the read operations.







## ***Instruction Execution :***
- ![[Screenshot 2024-02-24 015349.png]]
### instruction fetch :
- reading the instruction from the memory
- decode it
- give the address of the operand used.
### instruction execution :
- generate control signal
- execute the decoded instruction.


## Clock
- control all operations (control signal) in the computer
#### 2 edges :
- leading & trailing edge
- all action initiated by one of them and take a fixed number of clock period to complete
#### 2 states :
- lv 0 & lv 1 per period.


## ***instruction format :***
#### *The operation code :*
- specify the operation to be performed (logical, arithematic, data movement, branch operation)
- ![[3.png]]
#### *The operand address :*
- specify the location of the operand
#### *The addressing mode :*
##### specify :
- where the operand is located
- how to reach it
##### *the operand maybe located as :*
###### immediate data as part of instruction 
![[4.png]]
###### data stored in register 
![[5.png]]
###### data stored in memory
- you need to know the address to access the data in the memory and it may be:

	1 - specified directly in the instruction (direct addressing mode)
		- the operand address specify as part of the instruction.
		![[6.png]]
	2 - specified indirectly in the instruction (indirect addressing mode)
		- instruction specifies a place (register or memory) of the operand
		![[Pasted image 20240224025550.png]]
		- you can consider indexed addressing mode is a part of indirect addressing mode.
	3 -  Indexed addressing mode :
		- useful when a list or array are to be accessed using for loop to perform the same operations.
		- The base of the array is a register called  **BASE REGISTER**
		- index or distant from the base to the stored value register called  **INDEX REGISTER**
		- the sum of content of base & index registers are the address of the operand in memory.
		- for example:
			assume you have 10 numbers x1 to x10 are stored in the memory consecutive started from 0200H.
			- so the base register is 0200H, and to access X5 you need to pass 1, 2, 3, 4 so the index register will contain 04.
			- 
			** How it work ?
			- load the base register with the location of the array
			- load the index register with 0.
			- perform operation and increment the index until it match your search so (if the incremented register content is less than or equal the index -> increment, else continue.)
			- if 2D array:
				- Base Register: contain the base of the array
				- Index Register: contain the increment from base to the row where the data is stored
				- Displacement: in the instruction or separate register ,move between element in the row.

#### Page 18:
- the register names goes to internal registers first t obtain it's location in the memory (indirect addressing)
- direct addressing directly go the memory cause the instruction in the memory and doesn't need to search it in the registers. something like this...
## Instruction set: (5 groups)
#### 1- Data transfer group: 6 types
- deals with the movement of data
		- register to register
		- memory to register
			![[8.png]]
		- register to memory 
		- immediate data to register
			![[9.png]]
		- immediate data to memory
		- exchange data between registers
			![[10.png]]

#### 2- Arithmetic & logical group
##### Arithmetic group:
- normal data addition
- addition with carry
- normal subtraction
- subtraction with borrow
- multiplication
- division
- increment & decrement
##### logical group:
- AND, OR, XOR
- NOT
- Shift / Rotate
#### 3 - String manipulation
- Loading and storing elements
- moving to another memory location
- comparison of 2 strings.
#### 4 - Program Control group
- Conditional & Unconditional branch
- ~ & ~ call to subroutine
- return from subroutine
- restart
#### 5 - Execution control instruction
- instructions is related to :
		- no operation
		- Halt
		- enable & disable interrupts
		- initialization of control or function registers for interrupt, there are more than one instruction fall under one category ...
			![[12.png]]
## Programming System:-
#### Machine languages program:
- in the beginning of computer, users was only use machine languages(0,1) with different bit patterns. it was very difficult.
#### Assemble language program:-
- the second generation after machine language, it's more easier to write and understand than machine language.
- **Assembler** -> used as a system to convert assembly to machine code (it is a subsystem).
#### Assembly directives:-
- there are 2 instruction actually not instructions and don't need to be converted into machine language.
- ORG , END. 
- every assembler will have (pseudo / directive) to help the programmer to communicate with the assembler.
- operation (define), EQU (define a name)
- ![[13.png]]
#### Compilers:-
- after the growth of the computer, a complex problems has shown so we should develop a high level language like c, basic, etc to easy write program.
- a compiler needed to convert the high level language to machine code with the help of the assembler.
#### OS:-
- operating system also allocate computer resources and play different roles.