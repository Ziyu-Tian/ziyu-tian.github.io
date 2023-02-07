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


### 2: Programmable logic

#### 2.1: Programmable logic 

- The generalized logic circuits can lead to a possibility of arbitrary logic, hence the **Programmable Logic Array (PLA)**.

- Based on the fact that nay Boolean function can be represented as a sum of products.

- PLD based on a PLA consists of a programmable array of AND gates and a fixed array of OR gates.

![](image/2023-02-01-09-38-41.png)


#### 2.2: Sum of products 

- Any Boolean function can be represented as a sum of products.

- And a boolean function can be found through a truth table.

#### 2.3: Sum of products direct implementation 

![](image/2023-02-01-09-49-39.png)

![](image/2023-02-01-09-50-08.png)

- The PLA is divided into the AND plane and OR plane:
    - The outputs of the AND plane are the product terms.
    - Then these products terms become the inputs of the OR plane.

![](image/2023-02-01-10-12-35.png)

#### 2.4: BUffering implementation 

- Each input variable needs to have both positive and negative wires:

![](image/2023-02-01-10-13-55.png)


#### 2.5: Programmable Gates 

For example of an AND gate with $x_0$, $\bar{x_1}$, $x_2$ three inputs:

![](image/2023-02-01-10-15-41.png)

if connects to the OR array:

![](image/2023-02-01-10-18-58.png)

We can also use the textual description:

![](image/2023-02-01-10-19-37.png)

This plane is then defined by this "bit map".

With n inputs and m outputs, the size of PLA can be calculated as *m(2n+q)* cells.

#### 2.6: Minimization of PLA equations 

- For special-purpose PLA, their size can be minimized.

- The target of minimizing are:
    - The total number of gates and as few gates as possible.
    - Then number of inputs **into** each gate as small as possible.

- For PLA, the following wires going into each gates (n) and number of OR gates (q)


- The number of AND gates and the inputs into each OR gates can be **reduced**.

For example, $y_0 = r_0$ and $y_1 = r_0 + r_2$, $r_0$ appears twice in outputs. To minimize, it only needs to be created once.

- PLA minimization is finding equivalent formulas to reduce *m*.


#### 2.7: From truth table to PLA bitmaps

