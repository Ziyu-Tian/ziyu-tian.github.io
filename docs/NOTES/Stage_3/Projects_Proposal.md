<div align='center' ><font size ='6'>Proposal of the FPGA Accelerator Individual Project </font> </div>

<div align='center' ><font size ='3'>Ziyu Tian</font> </div>


## <font size=5 face=Times New Roman>I: Introduction</font>
<font size=3 face=Times New Roman>

With the increasing demand of machine learning (ML) based Artificial Intelligence (AI), the acceleration for the training and classification tasks become a valuable subject in modern computer science researches. Compared to the software implementation, hardware acceleration based on Field Programmable Gate Arrays (FPGAs) is significantly faster and less energy demanding. In this project, a low-power ML algorithm base on propositional logic, namely Tsetlin Machine, which originates from Tsetlin Automata, would be implemented on PYNQ-Z1 FPGA board as an accelerator. 

</font>


## <font size=5 face=Times New Roman>II: Aims and Objectives</font>
<font size=3 face=Times New Roman> 

The global aim of this project is to complete a functional Tsetlin Machine accelerator design implemented on PYNQ-Z1 FPGA board. For a typical classification task, the binary testing data should be transmitted into the ZYNQ-Z1, and the result of the class should be outputted back to user with the performance data (throughput, latency and power, etc) measured.

To finish the total aim, the target could be divided into three staged objectives: RTL design of Tsetlin Machine, Interconnection design and Circuits Simulation, Board level verification and Performance Analysis:

- **RTL design of Tsetlin Machine**: Initiate the Verilog design of Tsetlin Machine algorithm, construct and package the functional module into a IP core. Finish the regional test with simple datasets (such as XOR).


- **Interconnection design and Circuits Simulation**: Apply interconnection wiring between the PYNQ-Z1 Processor Module, Tsetlin Machine IP and peripheral IO modules. Finish the first stage simulation and generate the sequential waves.


- **Board level verification and Performance Analysis**: Base on the Tsetlin Machine Module design and interconnection modules, set the constraint file (.xdc) as well as the Verilog source file. Generate bitstream file and program the PYNQ-Z1 board. Measure and analyze the performance using monitoring software (eg.Xilinx Vivado).


</font>



## <font size=5 face=Times New Roman>III: Achievable-Milestone Statements </font>
<font size=3 face=Times New Roman> 

In order to complete the global target on time, the following milestones should be achieved:

- Milestone-1: Familiarize with the process of designing and measuring RTL modules with PYNQ-Z1 in Xilinx Vivado environment. Complete a 16 bits multiplier with PYNQ-Z1 and do the performance analysis.

- Milestone-2: Design the Tsetlin Machine module including Tsetlin Automata Module, Summing Module, Comparing and multiplexer Module. Simulate and verify the Tsetlin IP with testbench such as XOR.

- Milestone-3: Build the interconnection module (UART/AXI) to test the communication between Processor System (PS) and Programmable Logic (PL). Complete a simple test program which read in the data from UART port in PS and return the output form PL.

- Milestone-4: Construct the PS block, interconnection block and Tsetlin IP block. Test the demo-design on board with simple datasets.

- Milestone-5: Collect and compare the performance data (throughput, latency and power) with software implementation. Draw the conclusive report with comparison data.

</font>


## <font size=5 face=Times New Roman>IV: Risks Judgement and Mitigation   </font>
<font size=3 face=Times New Roman> 

To complete the settled objectives above, it is essential to do the advanced risks judgement and the research of mitigation methods. The risks may occur in the designing process are shown as below:

- **Risk-1**: The core objective of this project is the translation of Tsetlin Machine Algorithm from C / Python to Verilog, and it may cause problems due to different structures between software and hardware. To avoid the risk of generate unaware errors, a series of regional tests could be applied as the verification. Verify the partial block with simple tests such as doing XOR test of TM IP core could ensure the accuracy of translating  HDL codes, so that avoiding the large error of the total design.


- **Risk-2**: Compared with the software implementation, another risk of hardware design is doing sequential constraint between each blocks in the circuit. To reduce or avoid the risks of sequential error, the advanced simulation between implementation could be carried. A detailed sequential wave form of each elements should be monitored to keep all the signals on track, which could reduce the sequential risks mostly. 




## <font size=5 face=Times New Roman>V: Scheduled Gantt Chart </font>
<font size=3 face=Times New Roman> 

Following the objectives and risks analysis above, the planned schedule of this project is drawn as the Gantt Chart below.


![](image/2023-10-23-11-22-18.png)












