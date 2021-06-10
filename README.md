# qty4 CPU 
A open-source tiny 4 bit CPU project! The goal of this project is to build a tiny 4-bit programmable computer that can fit onto one PCB. We also would like to have many LEDs to show the cpu's state as it prossess commands, just like the BenEater 8-bit computer. 

This was planned in a few hours late in the evening. We are too cool for correct spelling or grammer. 

![image](https://user-images.githubusercontent.com/33582457/121453614-0e14f100-c967-11eb-8a31-3ae4417b45b1.png)

----

## Instruction Set
Since the computer is only using 4-bits to address the memory, we are limited to 16 possible operations. These operations are listed below.

```
--- ALU

# add
# sub
# inc
# dec

--- JUMP

# jmp
# jc
# jz
# jnc
# jnz

--- REGISTERS

# lda
# ldb
# sta
# stb

--- MISC

# nop
# hlt

```

## General Parts
```
Modules chips and parts:

Clock:
	555 timer x 3

RAM:
	arduino nano
	shift register (?)
	4 bit register chip
	2 4 bit x 4 bit ram chips
	
Instruction register:
	4 bit register chip

control logic:
	4 bit counter (step counter)
	eeproms (1 or 2?)
	demultiplexers?
	
program counter:
	4 bit counter with input and output

alu:
	4 bit register x 4 (a + b registers & sum holder & flags register)
	4 bit adder chip
	xor (?) chip for 2's complemtnt subtraction
	nor + and for checking if zero
	
output:
	7 segment display
	4 bit register
	hex 7 segment display driver chip

notes:
	will need leds, caps, resistors, and other stuff
	
	currently not accounting for extra bus driver chips that 
	would be needed to have register contents on leds at all times

```

## Inspiration for the Project 
This cpu is based on the BenEater 8-bit computer (https://eater.net/8bit/schematics)
![image](https://user-images.githubusercontent.com/33582457/121454319-32250200-c968-11eb-96ae-d7bbfd19e3a0.png)

