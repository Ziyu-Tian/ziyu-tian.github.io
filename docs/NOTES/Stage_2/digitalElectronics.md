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

- The result will be $z = a\bar{b}+c$

- The same for 4 variable K-map:

![](image/2023-02-08-10-07-55.png)

- The result will be $z = a\bar{b}+a\bar{c}+\bar{b}\bar{c}$


#### 2.12: Multiple output minimization 

![](image/2023-02-08-10-14-49.png)

- The key point is to find common-product term.

- Increase the number of AND gates, decrease the number of *m*.

- For example of:

![](image/2023-02-13-11-06-25.png)

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

## II: From PLAs to FPGAs 

### 1: PLA Usage 

- General PLA in CPU:

![](image/2023-02-13-14-06-24.png)

The control PLA takes in information and play a role as the controller.

Usually not optimizable, but fully programmable at design-time to accommodate CPU.

|![](image/2023-02-13-14-19-16.png)|![](image/2023-02-13-14-19-25.png)|
|---|---|

- General and Custom PLA:

![](image/2023-02-13-14-20-53.png)

### 2: Complex Programmable Logic Device (CPLD)

- Complex devices extend the idea of programmable logic further.

- A matrix of PLAs and programmable interconnection array (PIA)

![](image/2023-02-13-14-22-51.png)

### 3: Field programmable gate array (FPGA)

- FPGA employs another approach programmable logic (not based on PLA)

- The three basic elements are **configurable logic block (CLB)** or **logic array block (LAB)**, the **interconnections**, and the **IO Blocks**. 

![](image/2023-02-13-14-25-57.png)

- Each CLB is made up of **multiple smaller logic modules** and a lo**cal programmable interconnect** used to connect logic modules within CLB.

- General FPGA cell:

![](image/2023-02-13-14-33-04.png)

- SRAM -Based FPGAs 

     - FPGAs are either non-volatile because they are based on SRAM.

![](image/2023-02-13-14-38-13.png)

- FPGA Cores:
    - A hard core is a portion of logic in an FPGA that is put in by the manufacturer to provide a specific function and that cannot be reprogrammed.

![](image/2023-02-13-14-39-45.png)


- Specific FPGA Devices:
    - Example FPGA block diagram: Several manufacturer produce FPGAs as well as CPLDs.

![](image/2023-02-13-14-41-01.png)


## III: Memories in logic design 

### 1: Introduction 

- Gate-level memory cells (latches, flip-flops), used in CPU registers.

- Transistor level volatile memory cell:

    - SRAM, used in cache memory.
    - DRAM, used in main memory.

- Floating-gate memory cells (flash), non-volatile.

- FRAM, MRAM, Memristors: non-volatile.


### 2: SR Latch 

- Simplest memory elements based on a cross-paired of two input NAND or NOR gates.

![](image/2023-02-13-14-52-03.png)

![](image/2023-02-13-14-53-24.png)

#### 2.1: Gated SR Latch 

![](image/2023-02-16-10-22-08.png)

- The enable input E can define whether it is enabled for SR latch to receive signals.
(only E = '1')

### 3: Gated D Latch 

![](image/2023-02-16-10-23-57.png)

- D latch only have one input D in addition to E.

#### 3.1: D flip-flop 

- Controlled by a periodic control signal, eg. CLK
    - Memory for single bit.
    - Fast, high power.
    - 20 transistors as below design.

![](image/2023-02-16-10-30-17.png)

![](image/2023-02-16-10-30-25.png)

- Operation:

![](image/2023-02-16-10-36-18.png)

### 4: SRAM 

- Simple single-bit memory
![](image/2023-02-16-10-41-03.png)

#### 4.1: 6T SRAM 

![](image/2023-02-16-10-42-48.png)

### 5: DRAM 

![](image/2023-02-16-10-47-45.png)

### 6: Floating gate memory cells 

- Flash is based on floating gate.
    - FGMOS transistor 

## IV: Arithmetic Logic-Adders 

### 1: Digital arithmetic  

- Data path in charge of arithmetic operations.

- Controller defines the sequence of operations.

- Data path operation include:
    - addition
    - subtraction 
    - multiplication 
    - division 
    - AND, OR, etc.

### 2: The case of addition 

- Subtraction
    - implemented by addition through the use of 2's complement.
    - A - B = A + (2's complement of B)

- 2's complement 
    - A bit string considers two interpretations:
        - Natural interpretation
        - 2's complement 

![](image/2023-02-20-14-15-55.png)


- Multiplication:
    - Multiplication is repeated addition.
![](image/2023-02-20-14-18-48.png)

- Division:
    - The division can be divided into **comparison** and **subtraction**.

![](image/2023-02-20-14-20-52.png)

- Integer power and roots:
    - $A^n$: repeated multiplication / division.
    - $\sqrt[n]{A}$: successive approximation (monotony functions only)

![](image/2023-02-20-14-28-05.png)

- Functions not amenable for successive approximation:
    - Power series and lookup table approach.

### 3: N-bit adder 

Simplify the boolean expression of full-adder:

![](image/2023-02-20-14-38-47.png)


#### 3.1: Adder as a Sum of Products 

- No common product terms for random logic solution.

- AND and OR can be made using NAND.

![](image/2023-02-20-14-41-36.png)

#### 3.2: A more modular approach 

- A half adder adds two operands A and B without taken in carry in $C_{in}$.

![](image/2023-02-20-14-47-17.png)

- The practical point of the half adder is you can assemble a full adder using two half adders in modular fashion and end with smaller gates.

![](image/2023-02-20-14-48-37.png)

- Fewer gates, smaller gates but delay more from B to $C_{out}$.


#### 3.3: Ripple carry adder 

- $C_{in}$ of next bit is $C_{out}$ of current bit.

- If no $C_{in}$, just wire $C_{in}$ to 0.

- An n-bit adder can add two n-bits number.

![](image/2023-02-23-10-23-29.png)

- Delay problem:

![](image/2023-02-23-10-25-22.png)


#### 3.4: Speeding up addition 

- For delay, carry is more critical.

- Fewer inputs gates are faster.

- Separate out non-carry portion.

- Composition of two half adders.

- Delay may different:

|![](image/2023-02-27-14-20-06.png)|![](image/2023-02-27-14-20-39.png)|
|----|----|

- The max fan-in/fan-out = 2:

![](image/2023-02-27-14-22-12.png)

which delay is 2 gates per bit.

#### 3.5: More focused analysis 

- If we rename the signals as k for 1 to n.

![](image/2023-02-27-14-23-57.png)

- The carry to carry ripple delay is the critical path: $2n\tau$:

![](image/2023-02-27-14-25-36.png)

- Reviewing the truth table of adder, we may find the rule of **propagate**:

|![](image/2023-02-27-14-28-38.png)|![](image/2023-02-27-14-28-44.png)|
|----|----|

- Carry Generate G = 1, then $C_{out}=1$ whatever $C_{in}$ is.

- Carry Propagate P = 1, then $C_{out}=C_{in}$

- As G and P are dependent on A and B nothing to do with $C_{in}$, no need to wait for $C_{in}$ signal.

#### 3.6: Propagate and Generate 

- P and G come from A and B and only have single gate delay $\tau$.

![](image/2023-02-27-14-37-06.png)

- If we define every C signal as a sum of products of $G_k$, $P_k$ and $C_{in}$ only.

- We generate the carry path by **recursively** using the formula:
![](image/2023-02-27-14-46-39.png)

$$
\begin{equation*}
\begin{split}
    C_k &= G_k +P_kC_{k-1} \\ 
    &= G_k + P_k(G_{k-1}+P_{k-1}C_{k-2}) \\
\end{split} 
\end{equation*}
$$

- Recursive until $C_{-1}$ remains on the right side.

- All carries are evaluated in parallel:

![](image/2023-02-27-14-48-28.png)

#### 3.7: Taking out the carry chain 

![](image/2023-02-27-14-51-16.png)

- Combining existing parts to form a CLA adder:

![](image/2023-02-27-14-52-51.png)

- $S_k = P_k \oplus C_{k-1}$

#### 3.8: CLA adder delay 

- CLA adder formulas:

$$
\begin{equation*}
\begin{split}
    C_k &= G_k +P_kC_{k-1} \\ 
    S_k &= P_k \oplus C_{k-1} \\
\end{split} 
\end{equation*}
$$

- The total CLA delay is therefore:

![](20230301110617.png)

- Remember ripple carry adder delay $2n\tau$.

- In this CLA design, the delay reduced from linear to constant.


#### 3.9: Fan-in and Fan-out 

- We need to consider fan-in and fan-out for a realistic estimation of performance:
    - The CLA have fan-in and fan-out increasing with the increasing of bits.


#### 3.10: Gate switching 

- Gate switching can be modelled as the charging through resistors.

- The gate delay is noted as $\tau = RC$:

![](20230301112035.png)

- For example of a NOR Gate with 2 fan-in and 4 fan-out:

![](20230301112246.png)

#### 3.11: Gate delay

- The rise and fall times of the voltage at Y in previous NOR gate example depends on the $C_{load}$.

- $C_{load}$ is proportional to fan-out N(Y), so that the gate delay is proportional to N(Y).

- Each input adds a pair of transistors to the gate which causing extra capacitance.

- In general, pull-up and pull-down delays are not equal.

![](20230301132449.png)


#### 3.12: Fan-out delay cost 

- Drive m outputs - single gate delay has become $m\tau$.

- CLA is even worse than ripple carry in the cost of delay as for a single $P_n$ will be several fan-out.

- To solve this problem, we use fan-in (out) trees to decrease the number of fan-out by adding levels.


#### 3.13: Fan-out / Fan-in buffers 

![](20230301134309.png)

- For this condition, the fan-out (controlled gate) of one gate is only 3.

- If we note B is the **branching ratio** and L is the **level**, the realistic controlled by the input is $B^L$, which is 27 in this condition.

- As we know, the delay time is proportional to the total value of capacitance.

- To calculate the equivalent capacitance of fan-out (parallel), we can find that $C_{load}=B \times C_{load_in}$.

- As the fan-out is same for each level, if we note 'k' is the proportional constant, the total delay is :

$$
t_{tot} = L \times k \times B
$$

- Compare the total delay of this method (9k) and common method (27k), it reduced obviously.

- As the delay is $kBL$, we can change the value of B or L as long as BL is constant:

![](20230312174007.png)

- The optimal value for B is $e \approx 2.718$.

- In custom, the fan-out and fan-in should be limited to 4 for optimal performance.

#### 3.14: Fan-out Tree optimization 

- The best possible worst-case delay for a buffer delay is:

$$
t_{pd} = 4 + B[ns]
$$

- If we want a fan-out of 60, for B = 2:

![](20230312174849.png)

![](20230312175146.png)

![](20230312175430.png)

- For B = 3:

![](20230312175512.png)

- For B = 4:

![](20230312175655.png)

- For B = 5:

![](20230312175950.png)

![](20230312180038.png)

![](20230312180133.png)


#### 3.15: Fan-in optimization example 

- Consider a circuit which used to justify if all bits of a 64-bit word are zero.

- The easiest way is using the NAND gate or NOR gate with 64 fan-in and 1 fan-out.

-  To reduce the delay, we can use the circuit below which combine the NOR gate and NAND gate:

![](20230312201002.png)

- The delay formula is given as:

$$
t = 2+ (1\times B_{in}) + (2 \times B_{out})[ns]
$$

- And we can change the number of fan-in as well as the level (layer) of the gate:

![](20230312201143.png)



### 4: Large Adders 

#### 4.1: Adder size limits 

- For a 4-bit adder delays:

![](20230306141438.png)

- CLA has better performance, but the max fan-out delay grows with adder size.

- CLA adder size therefore cannot be more bits and 4-bits is almost the optimizable choice.

#### 4.2: Large adder design 

- Two ways to extend the size of these adders, whilst keeping the fan-in an fan-out problem in check:
    - Ripple carry
    - Block carry

##### 4.2.1: Ripple carrying CLA blocks 

- Ripple carry with constant max fan-in and fan-out unrelated to the size of adder, can be applied between CLA adder blocks.


![](20230306142223.png)


##### 4.2.2: Block carry of CLA 

- We use the same CLA method to a 4-bit CLA. Instead of using the $C_3$ as the output, the block carry needs to output G and P, which can also be noted as $G'$ and $P'$.

- Block carry generate G':
    - G' = 1 when carry is generated without regard to $C_{in}$.
- Block carry propagate P':
    - P' = 1 when block carry output depends on block carry input.

- The 4-bit adder carry output is redefined as:

![](20230313062915.png)

- The output of normal of CLA is $C_{n-1}$

![](20230313063312.png)

- The output of the block CLA is $G$ and $P$.

![](20230313063437.png)

- Example of 16 bits CLA:
    - Delay to form G, P is **1 $\tau$**
    - Delay to form final sum is **1 $\tau$**
    - Delay to do the first carry calculation C0, C1, C2 is  **2 $\tau$**
    - Delay to do other carry calculation (in parallel) is **2 $\tau$**
    - Delay to do CLA is **2 $\tau$**

- Each level multiply the size by 4, only adds a constant of $4\tau$:

![](20230313071210.png)

- We can find that O(n) to O(log(n)) in this method.


### 5: Multiplication Basics 

#### 5.1: Binary multiplication 

- Long multiplication example as 13 $\times$ 11:

![](20230313072115.png)

- This requires 3 or n-bit adder.



#### 5.2: Parallel Multiplier 

- We don't need to complete each partial product before starting the next.

![](20230316102000.png)

- Before you can add in $r_0d_2$, the previous row's addition needs to have processed to column 2.

- The addition order is a kind of wavefront form $r_0d_0$, $r_0d_1$,$r_0d_2$ to $r_0d_3$, as the red line in below:

![](20230328152159.png)

##### 5.2.1: Delay analysis 

- Using the previous method:
    - Single $\tau$ for one-bit multiplication (using AND gate, fully parallel)
    - Addition step has a delay which is approx to $\tau\log n$ if we use the CLA adder.

- To reduce the delay, we find that the adding starts from the right-side, so some bit-wise multiplication in the left is not required:

![](20230316101221.png)

- So we can use the only calculate what we need (Note that the figure may not correct)

![](20230327082242.png)

- Using the delay analysis of Ripple Carry Adder, we can find the delay of:

|![](20230327082907.png)|![](20230328153234.png)|
|---|---|

- If we set $n$ is the partial product number, so the total delay can be expressed as:

$$
1\tau (n-1) + 3\tau (n-1) + 2\tau (n-1) = 6n\tau - 6\tau
$$

- Compared to the previous method delay of $\tau + k_1.(n-1).\log{n}.\tau$, the parallel method is only $k_2.(n-1).\tau$


##### 5.2.2: Scope for further speedup 

- The last-row ripple-carry adder cannot be replaced by CLA cause the feed-in are not parallel.

- The carry chain still exist on downward path.

##### 5.2.3: Carry-save scheme 

- We may change the algorithm so that the final product remains but each row have different partial product, which means the final result of each row appearing at the same time.

- If we want to add two A + B block, the carry number need to be passed leftward:

![](20230328161013.png)

- But if we add three A + B block, the addition order can be changed as right (carry-save) or left (previous):

|![](20230328161149.png)|![](20230328161203.png)|
|---|---|

- This doesn't work if there is only one adder row.

- The final row needs special attention to catch all carries saved from the previous row, we use CLA here.

##### 5.2.4: 16 x 16 Multiplier Example

![](20230328185714.png)

- As there is no more leftward carry in the first row, so the full-adders can be replaced by half-adders (HA).

- The delay depth per row is now a single instead of two.

- One more row because of carry save.

##### 5.2.5: Per-row delay reduction 

- The previous ripple carry delay per-row is $4\tau$, which only happen  at the right-most diagonal:

![](20230328190249.png)

- The total delay is only $2\tau$ in the carry save condition:


![](20230328190715.png)

- Passing to the next row avoids the sequential propagation (the waiting for the previous signals) within single row.

- The total delay consist of:
    - One A, B to S delay ($2\tau$) for n-1 row.
    - Last row is block CLA adder (log delay)

- Assuming a 4-bits CLA adders in the final row, the delay is:

$$
D = 2(n-1)\tau + 4\tau \log_{4}{n} + \tau
$$

- If we use ripple-carry adder in the last line, the delay will be:

$$
D = 4(n-1)\tau + 2(n-2)\tau + \tau
$$

##### 5.2.6: Further Speedup Methods 

- Wallace / Dadda trees
    - Reduce the middle layer of partial product.
    - The total time is O(log(n))

- Approximate computing
    - Full precision is not needed most of time.
    - Eg. if we use a OR gate as a single-bit adder, the accuracy is 75%.

-  Analogue Multiplier

#### 5.3: Serial Multiplier

##### 5.3.1: Serial arithmetic 

- Parallel Multiplier featuren large hardware size.

- The block CLA multiplier makes the addition happens in 1 step, each step is the same, so we don't need n-1 n-bit block CLA adders.

- If we reuse the same CLA repeatedly n-1 times, this is method of serial operation.


- The carry-save multiplier is parallel at the level of individual cell, which can also be serialized.

##### 5.3.2: Serial Multiplication 

- If the multiplication / AND step is also serialized, we need $2n$ AND gates.

- A single adder (block CLA for speed)

- Some memory to store partial products between steps.

- Significant reduction of silicon compared to the parallel version.


- The simpler version of serial multiplier:
    - Repeatedly using a single adder row and a single row of ANDs.


![](20230328195040.png)


##### 5.3.3: The algorithm of serial multiplication

- The sequence of the operations should be:
    - Load R and D, and reset P to 0.
    - Add the partial product $r_0$ AND D to P.
    - Shift R right 1 bit; Shift D left 1 bit.
    - Repeat from step 2 for 4 times.


![](20230328195829.png)

- Multiplying two n-digit numbers the result may be up to 2n digit wide.

- Adding two n-digit numbers the result may be up to n+1 digits wide.

- Shifting the R Register right makes it possible to AND the correct $r_i$.

- Shifting the D register left can ensure the last-digit on the left is zero in partial product register.


- Time control signals for the registers:

![](20230328201958.png)



##### 5.3.4: Improvement of Serial multiplication

- Half of the bits in the adder have 0 in each addition steps.
    - Only half of the adder is ever used at a time.
    - We can do this with a n-bit adder instead of 2n-bit adder.

- It may save registers and AND gates as well.

- So if we apply a smaller version, the size an be reduced if the output register shifts.

- For example of 13 x 11 (1101 x 1011):

![](20230329003725.png)

- In each calculation, we can right-shift the register instead of the D or R.

- Move one of the partial product when doing the adding:

![](20230329004621.png)

- As we are doing the right-shift for the R register, it is gradually empty from left to right.


- The right-hand cell storing the right-shifted value can be replaced by Multiplier R:

![](20230329010549.png)


- The carry bit is not necessory if the adder drops the result to the right by one bit (combine add with shift).


##### 5.3.5: Delay Calculation 

- After initialization, the multiplier takes n CLK cycle to multiply two n-bits numbers:

- Each addition takes one n-bit adder delay, which should be accomodate with the CLK cycle.

- Assuming using the CLA adder, the delay should be $n(4\tau\log_{4}{n})$ (the max of CLA block is 4).

- So it is O(n x log(n))

- For n = 16, the delay is 128$\tau$.

- CLA serial multiplier is slower, and the size also grow with n because of CLA trees.

##### 5.3.6: Carry-save in serial multiplier


- Carry-save in serial multipliers:
    - Carry-bits must be stored in a register betwen steps; If D is shifted, the partial product are accumulated at the same position and the carry is shifted to the left at each clock., which requires 2n single-bit adder.

![](20230329025807.png)


- Combining shift with add:
    - if the product register P is shifted and D remains the same, thesum outputs must be shifted right each clock and the carries remain at the same position, which requires n single-bit adders.

- As the steps are controlled by clocks, we cannot exploit the tolerance for late $C_{in}$ to produce $C_{out}$. S and $C_{out}$ must be ready at the clock edge.

![](20230329030042.png)

- However, the space savings from serialization, we can make the single-bit adders a bit bigger and use the sum-of-product truth table design which has two layers of gates for a delayed of $2\tau$

![](20230329031027.png)

- Carry-save allows the parallelization of carries, and the remaining carries must be added at the last step.
    - n-1 CLK steps needed, with D held at 0, to sort out the final carries (like ripple-carry scheme)

- Delay at each step is now only 1 adder delay ($2\tau$):
    - $t_{total} = (n+(n-1))\times 2\tau$

- 





