# Fundamentals of Electric Circuits
> The source textbook is the *Fundamentals of Electric Circuits,The Seventh Edition*, written by Charles Alexander and Matthew Sadiku.
> The index of this note are not following the same number of the textbook. 


## 1: Basic Concepts 

### 1.1: Passive sign convention
- Passive sign convention is the convention we commonly used, which is satisfied when the current enters through the *positive terminal (+)*of an element. For the voltage analysis (eg. mesh analysis), if we follow a vested direction (mostly clockwise) of a loop, if the direction arrow enter the *positive terminal (+)* of a element, that voltage will be marked as *'+'* and vice versa.
- For example, the 5 V source in the Loop 1 should be marked as '-' as the following image.
![](image/2022-08-17-18-10-38.png)

### 1.2: Type of the Sources 
- **Ideal Independent sources** is an active elements(could generate power) that provides a specified voltage or current is *completely independent* of other elements. We use the 'circled sources' refer to **independent sources**.

![](image/2022-08-17-18-23-51.png)

- **Ideal dependent (controlled) source** is an active element in which the source quantity is controlled by another voltage or current. There are four types of dependent sources, namely:  VCVS (voltage-controlled voltage source), CCVS, VCCS, CCCS. We use the 'diamond-shaped symbols' refer to **dependent source**.

![](image/2022-08-17-18-30-36.png)

## 2: Basic Laws 

### Ohm's Law & Conductance 

- Ohm's Law which is $v\propto i$, or more commonly $v=iR$. The unit of resistance is Ohm.
- A useful quantity in circuit analysis is the reciprocal of resistance $R$, **Conductance**,$G=\frac{1}{R}$. The unit of the conductance is *mho* ($\mho$) or *Siemens* ($S$).

### Nodes, Branches, and Loops 

![](image/2022-08-18-10-15-52.png)

- A **branch** represents a single element such as a voltage source or a resistor. Such as the 10-V voltage source, the 2-A current source and three resistors.
- A **node** is the point of the connection between two or more branches.(the point with same electric potential).
- A **Loop** is a closed path formed by starting at a node. A loop is said to be independent if it is a single circle which doesn't contain another loop. (a brief understanding) The circuit in the graph have 3 independent loops for example.
- According to the topology, we have $*b=l+n-1*$.