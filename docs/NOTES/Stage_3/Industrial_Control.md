# Industrial Automation and Control Systems 

## I: ON-OFF (relay) Control 

### 1.1: Background 

- Often described as ON-OFF control or BANG-BANG Control.

- Could be implemented using simple RELAYS or by software implementation using PLC.

### 1.2: Washing Machine Example 

![](image/2023-09-25-10-21-21.png)

### 1.3: Type-1 RELAY 

![](image/2023-09-25-10-22-59.png)

- Using coils to control a different switch.

### 1.4: TYPE-2 Relay Latching and Reset Circuit 

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

### 1.5: Example of a water-level control system 

![](image/2023-09-25-10-46-58.png)

- If the level reaches the setting level or the emergency switch being pushed, the water-flow would be stopped.

