# Computer Systems and Microprocessors 


## I: Background

### 1: Fundamentals of CMOS 

#### 1.1: Transistor fundamentals: NMOS 

* NMOS, i.e. Negative Metal Oxide Field Efficient Transistor.

![](image/2022-10-04-10-03-42.png)

* The drain / source area are both doping with electrons (n-type doping), while the substrate is doped with holes.

* The insulator is filled with oxide.

* The gate is a switch which controlled by the $V_{GS}$ (voltage between gate and source). The high potential voltage will attracts the minor electrons in substrate so that form the channel.

* The electrons will move from the source to the drain and inverse for the current.

* The symbol of NMOS is below (sometimes using 'inlet' arrow ):


![](image/2022-10-04-10-10-35.png)


#### 1.2: Transistor fundamentals: PMOS 

* The same mechanism as NMOS. 


|![](image/2022-10-04-10-12-56.png)|![](image/2022-10-04-10-13-04.png)|
|---|---|


#### 1.3: CMOS: complementary MOSFET

![](image/2022-10-04-10-15-04.png)

### 2: CMOS logic Circuits: Inverter


![](image/2022-10-04-10-15-41.png)

* Note that the positive voltage for gate for NMOS is ON, the negative voltage for PMOS is ON.

 * 2 transistors needed.

### 3: CMOS Logic Circuits: NAND 


![](image/2022-10-04-10-54-58.png)

- If we fix one input as '1', this can also be used as an inverter. 


### 4: CMOS Logic Circuits: NOR 


![](image/2022-10-04-10-58-27.png)

- If we fix one of the input as '0', this can be used as an inverter.

### 5: D-type flip-flop (Latches)


![](image/2022-10-04-10-59-09.png)

- '0' for reset and '1' for set when clock is '1'.









