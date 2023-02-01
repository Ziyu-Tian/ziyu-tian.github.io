# Digital Electronics 

## I: Logic Design Part-1

### 1: Introduction 

- Design based on **Boolean algebra** using combinatorial logics gates and sequential logic.

- Computer-aided design used and hence the inclusive of VHDL for hardware description.

#### 1.1: Building blocks

- Basic logic gates and their inverses:

![](image/2023-02-01-07-11-48.png)

#### 1.2: Logic Integration 

- Discrete elements:
    - Assemble gates from transistors, diodes, etc.

- SSI, MSI - integrated circuits. 

- LSI, VLSI (very large IC)
    - More gates on a chip 

- Design style progress:
    - Programmable, semicustom and custom.

#### 1.3: Digital logic Structure 

![](image/2023-02-01-07-16-37.png)

![](image/2023-02-01-07-17-30.png)

#### 1.4: CMOS transistors

- MOSFETs are voltage-controlled switches used to make logic gates.

![](image/2023-02-01-09-11-34.png)

- CMOS Inverter can be built using two transistors.

![](image/2023-02-01-09-13-46.png)

- CMOS two input NOR Gate:

![](image/2023-02-01-09-18-07.png)

- CMOS four-input NAND Gate:

![](image/2023-02-01-09-25-21.png)

- Gates with more than four inputs are rarely implemented directly, which can be composed of multiple gates with fewer inputs.

- **The negative logic gates can used as universal gates.**

#### 1.5: Programmable logic 

- The generalized logic circuits can lead to a possibility of arbitrary logic, hence the **Programmable Logic Array (PLA)**.

- Based on the fact that nay Boolean function can be represented as a sum of products.

- PLD based on a PLA consists of a programmable array of AND gates and a fixed array of OR gates.

![](image/2023-02-01-09-38-41.png)


#### 1.6: Sum of products 

- Any Boolean function can be represented as a sum of products.

- And a boolean function can be found through a truth table.

#### 1.7: Sum of products direct implementation 

![](image/2023-02-01-09-49-39.png)

![](image/2023-02-01-09-50-08.png)

- The PLA is divided into the AND plane and OR plane:
    - The 
