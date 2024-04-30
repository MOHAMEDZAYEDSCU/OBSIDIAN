[[Micro Lec 1]]

## What is microprocessor:-
- It is ALU & Control unit on single IC chip.
- IF we put memory with them on the same IC chip it will be microcomputer (microcontroller).
- It is digital device which can fetch, decode & execute instructions.
- accept data from input devices and send them to output devices.
- microprocessor specify by its **word size**
-  for example -
	- 8 bit microprocessor perform different operation on 8 bit data.
- also specify the width of the data bus.
### Address, Data & Control BUS:-
#### Address bus:
- unidirectional since address locations are sent by microprocessor to i/o devices or memory.
#### Data bus:
- Bi directional cause it send and receive data
#### Control bus:
- Bi directional from the processor to the i/o devices
- signals like read or write form i/o or memory are the output of microprocessor.الاوامر التي تنفذ تكون خارجة من المعالج

## Tristate Bus:
- 3 transmitter with 3 output gates connect to a single bus and only one should transmit at instant (time) through enable and disable gate.
## Clock Generation:
- in past, every microprocessor need a clock and it will be externally
- now the clock generator circuit embedded in the microprocessor chip
- to synchronize the i/o devices with processor . it put the clock as clock out
- in multi processor, the clock out can be connected to other microprocessors.
## Connecting microprocessor to i/o devices:
#### IO  Mapped, interface:
- i/o devices are identified by port number and memory location by addresses.
- when read from i/o device, the i/o signal is ON
- when read or write from memory, the memory signal is ON and particular location of memory is selected.
- no confusion between device addresses , port number and memory location.
- signal i/o and memory are not present.
- if memory address and the port number or i/o device are the same, there would be a conflict so they are not the same...
## Data transfer schemes:
- parallel and serial data transfer.
#### Parallel Data Transfer:
##### [1] Programmed I/O
- data transfer controlled by user program
- it may be synchronous or asynchronous depend on the type and speed of data transfer device.
- when i/o device match the speed of processor (synchronous)
- if the device not ready, the microprocessor still check it until it become ready.

##### [2] interrupt I/O
- microprocessor kept busy for slower io devices
- u can make the microprocessor do its job while the io device getting ready through interrupt send to the processor.
- microprocessor can do higher priority jobs.
- microprocessor should scan the interrupt pin each machine cycle to check if there are interrupt happened or not.

##### [3] Direct memory access (DMA)
 - data is transferred to the memory through accumulator.
 
	the operation sequence of DMA :-
- the microprocessor check for DMA request signal each machine cycle.
- the I/O device send request to the DMA pin.
- microprocessor tristate address, data and control bus.
- microprocessor send acknowledgement signal to DMA acknowledgement pin.
- I/O devices use bus system to transfer data to memory
- after data transfer, I/O device withdraw the DMA request.
- the microprocessor continue check for DMA requests, when the signal is withdraw microprocessor resume normal operations.
- it can store data direct to the memory without the microprocessor interrupt, this will be faster for larger files.
#### Serial data transfer:
- between 2 processors in serial mode.
- bit by bit on single line.
- have 2 pins for input and output.
- has special software instruction to affect data transfer .
## Architectural Development of microprocessors:
- most of the computer development is in microprocessor field.
- **The pipelined microprocessors** : have a number of smaller units connected in series and each one can perform its tasks and the system can give more throughput than single processor.
#### Pipelining:
##### Pros:
- used for enhancing the execution speed.
- Instruction execution contain 4 sub tasks:
	[1] Instruction fetch
	[2] Instruction decode
	[3] operand fetch
	[4] execute.
- for example:
		we have a 4 processing element and a task T, so the T will be divided into 4 small tasks and each process element will have a clock cycle to execute it.
- single task has no advantage in pipelining than single processor.

##### Cons:
- not all instruction are independent, if instruction has to work on the result of the previous instruction.
- *control logic insert stalls*: waste clock cycle on dependences instructions.
- branch instruction has the same problem and could be solved by branch prediction.
## Cache memory:
- between the main memory and processor to maintain the execution speed.
- few kilobytes of high speed static ram. the main memory are dynamic, cheaper and slower.

- when CPU want to read byte or word, it output address on the address bus.
- the cache controller check if the content available in the cache memory.

- if available, the cache controller allow cache memory to send the addressed word/byte to the data bus.
	- data bus -> the road which data transfer between CPU and memory.
- if not available, the cache controller enable dram controller.
- DRAM controller send the address to the main memory to get the byte/word (will be slower)
- now data is read and transferred to the CPU and cache memory.
## Multilevel caches:
- there are inclusive or exclusive.
- in inclusive(شامل), the data could be in either cache1 and cache2
- in exclusive (حصري, مخصص), the data could be in cache1 or cache2.
## Virtual memory:
- the computer programs became lengthy and more complex so a physical memory size would be a problem to it.
- appeared to allow dividing program into fixed or size pages and store it into hard disk.
- and the basic idea is that pages can be swapped between hard disk and main memory when needed by the operating system.
- the translation of virtual address to physical address is done by **Memory Management Unit (MMU)** and it is hardware. 
- The dirty bit:
	- if the bit = 1, the page has been modified.
- Referenced bit:
	- if the bit = 1, the page has been set reference and may be currently in use.
- Protection bits:
	- specify whether the data in the page can be read/written or execute.
	