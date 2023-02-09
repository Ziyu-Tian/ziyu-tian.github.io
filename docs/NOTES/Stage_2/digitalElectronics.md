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

#### 2.4: Buffering implementation 

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

- Using the RHS of truth table forming the OR plane:
![](image/2023-02-08-10-04-14.png)

- Using all the value '1' in LHS forming AND plane positive column:

![](image/2023-02-08-10-04-27.png)

- Using all value '0' in LHS forming AND plane negative column:

![](image/2023-02-08-10-04-37.png)

#### 2.8: Sum-of-Product SOP 


We can deduce the sum-of-product formula from the truth table value:


- Firstly, find out the SOP using result '1' lines:

$$
z = \bar{a}\bar{b}c + \bar{a}bc + a\bar{b}\bar{c} + a\bar{b}c + abc
$$

- Next step, rewrite the formula to product-of sum form (POS):

$$
z = (a+b+c).(a+\bar{b}+c).(\bar{a}+\bar{b}+c)
$$


#### 2.9: Basic rules of Boolean algebra 


#### 2.10: AND/OR vs NAND/NOR implementation of SOP expression 


- Implementing an SOP expression simply requires ORing the outputs of AND gates.


![](image/2023-02-08-10-01-40.png)


- NAND gates can be used to implement an SOP expression:


#### 2.11: The Karnaugh Map (K-map)


- The Karnaugh map can be used to minimize the Boolean function z(a,b,c).

- First write down the true table in K map:

![](image/2023-02-08-10-05-49.png)

- Then draw the circle to combine the nearly blocks:

![](image/2023-02-08-10-07-03.png)

- The result will be $z = a\bar{b}+\bar{c}$

- The same for 4 variable K-map:

![](image/2023-02-08-10-07-55.png)

- The result will be $z = a\bar{b}+a\bar{c}+\bar{b}\bar{c}$


#### 2.12: Multiple output minimization 

![](image/2023-02-08-10-14-49.png)

- The key point is to find common-product term.

- Increase the number of AND gates, decrease the number of *m*.

- For example of:

![](image/2023-02-08-10-21-24.png)

- The first step is to find all ANDs:

![](image/2023-02-08-10-21-54.png)

- Finally we find that *m* reduced to 2:

![](image/2023-02-08-10-22-37.png)

#### 2.13: Hardware implementation of connection bitmaps 

- Hard-wired: NOT programmable.

- Single-time programmable: WORM (Write once read only).

- Multiple-time programmable: connections done through transistors switches controlled by external signals.


#### 2.14: Diagram review of PLA

- Fuses used for non-programmable and single programmable.

![](image/2023-02-08-10-27-07.png)

- CMOS (transistors) used in multiple programmable device.

![](image/2023-02-08-10-27-55.png)

#### 2.15: Full programmability 

- Full programmability only requires one of the plane to have programmability:
    
- AND gates fixed and programmable OR gates are enough for full programmability.


#### 2.16: More complex K-maps 

- Minimize the 5-variables expression fro example:

![](image/2023-02-08-10-34-03.png)

- We can go with a **3D presentation** of the K-map.

- $z = f(a,b,c,d,e)$ can be expressed as $ z= f_{e=0}(a,b,c,d) + f_{e=1}(a,b,c,d)$.

![](image/2023-02-08-10-40-19.png)


- For six variables:

![](image/2023-02-08-10-41-41.png)

![](image/2023-02-08-10-41-51.png)

- To solve the problem in example, we can rewrite to:

$$
G =G_{V=0} + G_{V=1}
$$

then 

$$
G_{V=0} = X\bar{Y}\bar{Z} + WX\bar{Y}\bar{Z} \\
G_{V=1} = \bar{Y}\bar{Z} +\bar{X}Y\bar{Z} +WX\bar{Y}\bar{Z}
$$

![](image/2023-02-08-10-53-08.png)


- The result finally be $G = X\bar{Y}\bar{Z} + V\bar{X}\bar{Z}$










