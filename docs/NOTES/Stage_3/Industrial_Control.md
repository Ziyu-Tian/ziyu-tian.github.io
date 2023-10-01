# Industrial Automation and PLCs 

## I: ON-OFF (relay) Control 

### 1: Background 

- Often described as ON-OFF control or BANG-BANG Control.

- Could be implemented using simple RELAYS or by software implementation using PLC.

### 2: Washing Machine Example 

![](image/2023-09-25-10-21-21.png)

### 3: Type-1 RELAY 

![](image/2023-09-25-10-22-59.png)

- Using coils to control a different switch.

### 4: TYPE-2 Relay Latching and Reset Circuit 

- We need a mechanism which will latch the relay when
the button is pressed and released. We also need a mechanism to reset the latch.

![](image/2023-09-25-10-25-54.png)

- We could implement Logical Expression using Relays. 

- Buffer should be like:
![](image/2023-09-25-10-29-11.png)

- NOT Gate should be like:
![](image/2023-09-25-10-29-32.png)

- AND Gate:

![](image/2023-09-25-10-30-02.png)

- OR Gate:

![](image/2023-09-25-10-30-30.png)

- XOR Gate:

![](image/2023-09-25-10-36-41.png)

### 5: Example of a water-level control system 

![](image/2023-09-25-10-46-58.png)

- If the level reaches the setting level or the emergency switch being pushed, the water-flow would be stopped.


### 6: Type-3 Timers 

- There is often a need in control applications where we want a relay to energise
after some fixed time delay has passed following a button being presse

- A timer unit integrated into the relay system can achieve this.

- There are two topology variations of the timer (simple and latching) which can operate in two ‘DELAY’ modes, either ON or OFF. 

![](image/2023-09-25-10-56-01.png)

- A latch could also be added:

![](image/2023-09-25-10-56-51.png)


### 7: Type-4 Counters 

- Counters are used for the counting of a specific number of operations (switchings) of the system contacts.

- A simple counter will have two inputs: a Reset (R) that resets the counter and an input (In) which provides the pulses that are counted.

![](image/2023-10-01-21-00-50.png)


### 8: Reality and Switching Relay Characteristic 

- Our discussion so far has assumed that the relay is an ideal switch: as the input signal goes from negative to positive the switch immediately changes state from
OFF to ON and if the input signal goes from positive to negative the switch state changes from ON to OFF.

![](image/2023-10-01-21-02-45.png)

- In practice relays exhibit hysteresis: as the
input signal goes from negative to positive it actually needs to reach a threshold value (+t) before the switch state changes. Likewise as the input signal goes from positive to negative it must reach a threshold value (-t) before the switch state changes from ON to OFF.

![](image/2023-10-01-21-03-45.png)

- So the relay in Simulink is:

![](image/2023-10-01-21-04-11.png)

### 9: Example of a bank-control system 

![](image/2023-10-01-21-09-23.png)

