## An Overview of FPGA's
 
### Introduction 
Field Programmable Gate Arrays (FPGAs) are digital ICs that enable a 
person to program a customized Digital Logic as per his/her 
requirements. In an FPGA, Digital Logic of the IC is not fixed during its 
manufacturing (or fabrication) but rather it is programmed by the 
designer.
FPG is a type of PLD. PLD (Programmable Logic Device) is an IC 
containing a large number of Logic gates and Flip-flops that can be 
configured by the user to implement a wide variety of functions.
There are 3 types of PLD:
1. Simple Programmable Logic Devices (SPLD)
2. Complex Programmable Logic Devices (CPLD)
3. Field Programmable Gate Arrays (FPGA)
FPGA is the most complicated of the three.
### FPGA In depth explanation 
FPGAs are pre-fabricated Silicon devices that consists of a matrix of 
reconfigurable logic circuitry and programmable interconnects 
arranged in a two-dimensional array. The programmable Logic Cells 
can be configured to perform any digital function and the 
programmable interconnects (or switches) provide the connections 
among different logic cells.
Using an FPGA, you can implement any custom design by specifying 
the logic or function of each logic block and setting the connection of 
each programmable switch. Since this process of designing a custom 
circuit is done in the field rather than in fabrication, the device is 
known as “Field Programmable”.
![Screenshot 2024-09-05 141333](https://github.com/user-attachments/assets/f9d18c63-031d-41ad-ba28-2e803ce1dd38)

The core of the FPGA is made up of configurable logic cells and 
programmable interconnections. These are surrounded by a number 
of programmable IO blocks, which are used to talk to the external 
world.
Unlike processors, FPGAs are capable of parallel operations, so 
different processing operations do not compete for the same 
resources. Each independent task is assigned to a dedicated section 
of the chip and can function autonomously without influence from
other logic blocks. Consequently, the performance of one part of the 
application is unaffected as more operations are added.
FPGAs are designed to be programmed using Hardware Description 
Language such as Verilog HDL or VHDL.
 
### Components of an FPGA 
#### • Configurable Logic Blocks
Configurable logic blocks (CLBs) are the basic logic unit of an FPGA. A 
CLB gives the FPGA its ability to accept different hardware 
configurations. CLBs can be programmed to perform almost any logic 
function. The individual CLB contains a number of discrete logic 
components including look-up tables (LUTs) and flip-flops.
![Screenshot 2024-09-05 141447](https://github.com/user-attachments/assets/5197fd52-c5df-476f-871b-fcdf5bcc3099)

#### • Flip-Flops
A flip-flop is a type of circuit that can store and recall a single bit of 
information. By latching a value and changing it when triggered by a 
clock signal, flip-flops can store data over time. They are called flipflops because they have two stable states and switch between them 
based on a triggering event.
![image](https://github.com/user-attachments/assets/6d152948-f856-404f-8186-a577e0535cc9)

#### • Lookup Tables
A lookup table (LUT) determines what the output is for any given 
input. it is the truth table and defines how combinatorial logic 
behaves. A truth table is a predefined list of outputs for each 
combination of inputs. The LUT holds a custom truth table that is 
loaded when the chip is powered up. It defines and directs the 
behavior of the combinatorial logic of your chip based on your VHDL 
or Verilog code, referring to the predetermined values to produce the 
desired results. The multiplexer decides the inputs for the look up 
table.
![image](https://github.com/user-attachments/assets/4cb0d69d-f965-43c9-be26-acc8367f334a)

This means that the inputs you put into the Lookup Table are 
basically the address lines for a one bit wide RAM cell. As such, if you 
were to use a two inputs logic gate, it would make sense that it is 
able to produce or accommodate for four different combinatorial 
scenarios, thus making it suitable for a 4 x 1 bit RAM. You can keep 
increasing the number of inputs you wish to have and make 
subsequent modifications in the RAM you will be needing.
#### • Block RAM
Block RAM (BRAM) is a type of random access memory embedded 
throughout an FPGA for data storage. Block RAM is organized in 
blocks of fixed size, such as 18K bits or 36K bits per block, depending 
on the FPGA family and model. The size of each block may vary 
among different FPGA architectures. Block RAM can be configured in 
either dual-port or single-port modes. Dual-port mode allows for 
simultaneous read and write operations from two different ports, 
providing increased flexibility for certain applications. Block RAM in 
FPGAs typically operates synchronously with the clock signal of the 
FPGA. This means that read and write operations are synchronized to 
the clock, facilitating predictable and deterministic behavior.
#### • DSP Slices
A DSP slice, or sometimes referred to as a block or cell, is one of 
the specialized components in an FPGA. It carries out digital 
signal processing functions, like filtering or multiplying, more 
efficiently than using many CLBs. This multiplier circuitry saves 
on LUT and flip-flop usage in math and signal processing 
applications.
#### • Multiplexer
A multiplexer (or Mux) is another word for a selector. It acts much 
like a railroad switch. Multiplexers are used all the time in FPGAs in 
various sizes and configurations. This image shows what a 2 to 1 mux 
looks like symbolically. The inputs to the mux are A, B, sel, the output 
is out. A and B are the Data inputs that get selected to the output. sel 
is your control signal. Muxes can come in all possible combinations, 
depending on your particular use case. Typically, some number of 
inputs are selected to a single output. However the reverse could be 
true and it would still be a mux. A single input could be selected to 
any number of outputs.
![image](https://github.com/user-attachments/assets/91ef73d8-b6b5-4a54-8917-811ed933f015)

#### • Input/Output Blocks
Input Output (IO) blocks are the components through which data 
transfers in and out of the FPGA. Used to complete the driving and 
matching requirements for input/output signals under different 
electrical characteristics. The IO blocks are configurable depending 
on the type of data.
### Languages used in FPGA programming 
Hardware description language is used to assemble these FPGA 
building blocks into a circuit that will perform a specific task. The 
process is different from programming a GPU or CPU, since you aren’t 
writing a program that will run sequentially. Rather, you’re using an 
HDL to create circuits and physically change the hardware depending 
on what you want it to do.
The two most popular hardware description languages are VHDL and 
Verilog. VHDL’s syntax is similar to Pascal. Verilog, however, is similar 
to C.
![image](https://github.com/user-attachments/assets/c1f43b3c-e707-4118-87c7-71545738970c)

### Applications 
#### • Designing ASICs using FPGAs
We can create a prototype of ASIC using FPGA and thanks to this 
method, errors are correctable.
#### • Improvements in automotive experiences
Solutions for in-vehicle infotainment, comfort, and convenience using 
automotive silicon and IP.
#### • Supporting real-time systems
#### • Aerospace and defense use cases
#### • Digital signal processing, biomedical instrumentation, device controllers, software-defined radio,
####  random logic, medical imaging, computer hardware emulation, voice recognition,
####  cryptography, filtering and communication encoding, and more.
