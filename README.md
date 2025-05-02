# NASSCOM-RISC-V Workshop
## Day 1 – RISC-V ISA and GNU Compiler 

### Topics Covered

### 1. Introduction to RISC-V ISA  
RISC-V is an open-source instruction set architecture that is simple, modular, and extensible.  
It is designed for flexibility in education, research, and commercial use.

### 2. Finding the Sum from 1 to n  
We discussed a simple logic in C to calculate the sum from 1 to `n`.  
This helped demonstrate how basic loops and arithmetic are handled in RISC-V.

### 3. GCC Compiler for RISC-V  
GCC is used to compile programs into RISC-V machine code.  
We explored how to generate executable and assembly output using the RISC-V toolchain.

### 4. Disassembler (objdump)  
`objdump` was used to view the RISC-V assembly code generated from our C program.  
It shows how the high-level logic is broken into instructions.

### 5. Spike Simulation  
Spike is a functional RISC-V simulator.  
It was used to execute compiled programs and observe output in a simulated environment.

### 6. Debugging with GDB  
We used GDB to step through the program and inspect the values of variables and registers.  
This helped in understanding program flow and internal state.

### 7. Integer number representation 
We covered the difference between signed and unsigned integers.  
Signed numbers support both positive and negative values, while unsigned support only positive.




![sum1ton](https://github.com/user-attachments/assets/c79d4da1-69f8-447b-8217-93d564655e03)


![Screenshot 2025-04-25 214232](https://github.com/user-attachments/assets/e67eaf80-e26f-4d96-9512-121ed8be82ee)

---

## Day 2 – Introduction to ABI and Basic Verification Flow

## Topics Covered

### Introduction to ABI  
The Application Binary Interface (ABI) defines how functions interact at the binary level.  
It sets conventions for function calling, data layout, and register usage in compiled code.

### ABI Function Call  
We explored how parameters are passed to functions and how results are returned based on ABI rules.  
Registers like `a0–a7` are used for arguments and return values, while `s` and `t` registers serve specific roles.

### Algorithm for 1 to n using Assembly  
An algorithm to compute the sum from 1 to `n` was implemented in RISC-V Assembly.  
This demonstrated the use of loops, arithmetic operations, and register management manually.

### Basic Verification Flow (in Brief)  
The verification process ensures the correctness of assembly programs.  
Key steps include compiling, simulating with Spike, comparing expected output, and debugging with GDB if needed.

## Lab Work  
![Screenshot 2025-04-25 224414](https://github.com/user-attachments/assets/29dab975-e098-4568-9e6b-e41d77eb120d)


![Screenshot 2025-04-25 224348](https://github.com/user-attachments/assets/ae11534b-193d-4f61-b839-6f4691c241e4)


![Screenshot 2025-04-25 224326](https://github.com/user-attachments/assets/1eafeba5-0397-4b4d-9c5c-1a976325f767)


![Screenshot 2025-04-25 220331](https://github.com/user-attachments/assets/2e4bc5f1-8baf-428e-8b46-4134859622d4)


![Screenshot 2025-04-25 220313](https://github.com/user-attachments/assets/aa5d7f0c-4848-4d1c-a879-6da2cb33ef69)



---


## Day 3: Digital Logic with TL-Verilog and MakerChip

### Overview:
On Day 3, we explored fundamental concepts of digital logic design using TL-Verilog and MakerChip. The session focused on combinational logic, sequential logic, pipelining, and finite state machines (FSM), all of which were simulated using MakerChip to understand their behavior and functionality.

### Key Topics Covered:

#### 1. **Combinational Logic**
   - Combinational logic circuits produce outputs based purely on current inputs, with no memory or feedback.
   - Example components: AND, OR, NOT gates, multiplexers, and adders.
   - Focus: Designed and simulated basic combinational circuits to understand their behavior in different scenarios.

#### 2. **Sequential Logic**
   - Sequential circuits depend on both current inputs and past states, utilizing memory elements such as flip-flops.
   - Example components: D flip-flops, counters, and shift registers.
   - Focus: Emphasis was placed on implementing sequential circuits and understanding how memory elements impact circuit behavior.

#### 3. **Pipelining**
   - Pipelining divides a process into multiple stages, allowing concurrent processing of multiple data sets, thus increasing throughput.
   - Example: Multi-stage data processing in processors.
   - Focus: A simple 2-stage pipeline was used to understand how data flows through stages, enhancing circuit efficiency.

#### 4. **State  **
   - FSMs transition between a finite number of states based on inputs and the current state, making them suitable for control systems.
   - Example: Simple 2-state FSM used to toggle outputs based on inputs.
   - Focus: Explored both Moore and Mealy machine models to understand state transitions in response to different inputs.

### Tools and Environment:
- **TL-Verilog**: A hardware description language used to model digital circuits. It allowed for clear and concise circuit design.
- **MakerChip**: An online platform used for simulating TL-Verilog designs, enabling real-time visualization and testing of the circuits.


### Lab Work

![Screenshot 2025-04-24 114044](https://github.com/user-attachments/assets/5bacb580-c1b3-4b3e-9882-c617634e9931)


![Screenshot 2025-04-24 121549](https://github.com/user-attachments/assets/96417242-71be-4e50-a08d-bf781fc8d9a6)

---

# Lab-4: Basic RISC-V CPU Microarchitecture

## Overview
In Lab-4, we designed a basic RISC-V CPU microarchitecture, focusing on the Fetch, Decode, Register File Read, ALU, and Branch stages. This simplified pipeline serves as a foundation for building more complex RISC-V processors.

## Topics Covered

### 1. Fetch 
The Fetch stage retrieves the instruction from memory using the Program Counter (PC). The instruction is stored in the Instruction Register (IR). The PC is incremented to point to the next instruction.

### 2. Decode 
The Decode stage decodes the fetched instruction and extracts the opcode and operand registers. The Control Unit generates control signals for subsequent stages. Source registers are read from the Register File.

### 3. Register File Read
The Register File stores values of general-purpose registers. In this stage, two source registers are read from the Register File. The values are passed to the ALU for processing.

### 4. ALU
The ALU performs arithmetic or logical operations based on the decoded instruction. The operation is determined by control signals from the Decode stage. The result is sent to the next stage for possible branching or writing back.

### 5. Branch
The Branch stage checks if a branch condition (e.g., BEQ, BNE) is satisfied. If true, the PC is updated to the branch target address. If false, the PC continues to the next instruction.

### Lab work

[code](https://www.makerchip.com/sandbox/0kRfnhkLx/0Wnh53n)

![Picture9](https://github.com/user-attachments/assets/e48b2320-6155-44a4-99b4-635312548b76)


![Picture8](https://github.com/user-attachments/assets/d2ca6835-e00c-4794-8c6f-2b5845fbd7ee)


![Picture7](https://github.com/user-attachments/assets/52658b03-2b29-455a-8692-d196bb74729c)


![Picture6](https://github.com/user-attachments/assets/6ea90899-1c42-4720-a334-e593599b66b4)


![Picture5](https://github.com/user-attachments/assets/d28304de-02bf-438a-9723-6b8d42566aa0)


![Picture4](https://github.com/user-attachments/assets/6adac80f-c376-4cda-b43e-24b206a12d30)


![Picture3](https://github.com/user-attachments/assets/cf2ad945-c224-4395-a751-b7dc262a65d0)


![Picture2](https://github.com/user-attachments/assets/96873e2e-bffa-479d-9f04-4dd8856b9436)



![pc](https://github.com/user-attachments/assets/1e6b8d2f-960a-4fe1-ab89-f1b964f75b41)


---

## Day-5: Complete Pipelined RISC-V CPU Microarchitecture

###Topics Covered

###1. Pipelining in RISC-V CPU
Pipelining divides the CPU into stages (IF, ID, EX, MEM, WB), allowing concurrent execution of multiple instructions. Each stage processes different instructions simultaneously, improving throughput. This approach reduces instruction execution time and enhances overall CPU performance.

### 2. 3-Cycle Valid Signal
The 3-cycle valid signal ensures that data is properly validated before moving between pipeline stages. It prevents premature execution of data and maintains correctness. The signal helps prevent errors in data forwarding and execution order.

### 3. Handling Pipeline Hazards
Data hazards are resolved through forwarding and stalling to ensure proper data flow. Control hazards are managed with branch prediction and pipeline bubbles to avoid delays. Structural hazards are prevented by synchronizing shared resources and pipeline stages.

### 4. Load and Store Instructions
Load instructions retrieve data from memory, passing it through the pipeline stages. Store instructions write data to memory, requiring synchronization to avoid conflicts. Both types need hazard management to ensure correct execution and data flow.

### 5. Complete RISC-V CPU Design
The full RISC-V CPU integrates pipelined stages with proper hazard resolution and memory operations. It processes instructions efficiently through forwarding, stalling, and branch prediction. This design allows parallel execution and significantly improves performance.

### Lab work

![Picture10](https://github.com/user-attachments/assets/e8b24245-401e-42f1-bb60-2d2cf22fb6c8)





![Picture11](https://github.com/user-attachments/assets/756fd175-fcba-426c-bfdb-78b79731625c)




![Picture12](https://github.com/user-attachments/assets/82c62f52-6fcd-4c55-bd8c-7c78b565b582)





![Picture13](https://github.com/user-attachments/assets/eb6b17bd-ae64-4d68-908c-f0fe3d1d725f)





![Picture14](https://github.com/user-attachments/assets/94488695-bffd-4760-b56a-0700e6384c34)





![Picture15](https://github.com/user-attachments/assets/a55c00cb-2882-4f10-9a34-dc6032b4f1f3)


### final RISC-V Core

[final](https://www.makerchip.com/sandbox/0kRfnhkLx/0RghvY2)

![Picture16](https://github.com/user-attachments/assets/e8378c21-3272-4f98-b83b-f5c346863479)

---



