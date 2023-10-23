<div align='center' ><font size ='6'>Proposal of the FPGA Accelerator Individual Project </font> </div>

<div align='center' ><font size ='2'>Ziyu Tian</font> </div>


## <font size=5 face=Times New Roman>I: Introduction</font>
<font size=3 face=Times New Roman>

With the increasing demand of machine learning (ML) based Artificial Intelligence (AI), the acceleration for the training and classification tasks become a valuable subject in modern computer science researches. Compared to the software implementation, hardware acceleration based on Field Programmable Gate Arrays (FPGAs) is significantly faster and less energy demanding. In this project, a low-power ML algorithm base on propositional logic, namely Tsetlin Machine [1], which originates from Tsetlin Automata [2], would be implemented on PYNQ-Z1 FPGA board as an accelerator. 

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



## <font size=5 face=Times New Roman>IV: Scheduled Gantt Chart  </font>
<font size=3 face=Times New Roman> 

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       FPGA Accelerator Project Schedule 
    excludes    

    section Technical Design
    Vivado Familiarize                     : des1, 2023-10-23,2024-01-08
    Multiplier Performance Analysis        :milestone, 2023-10-27, 0d
    task2                     :         des2, 2024-01-09, 3d
    task3                     :         des3, after des2, 5d
    task4                     :         des4, after des3, 5d


```
</font>



## <font size=5 face=Times New Roman> References </font>
<font size=3 face=Times New Roman>


[1]:J.Lei, A.Wheeldon, R.Shafik, A.Yakovlev and O. -C. Granmo, "*From Arithmetic to Logic based AI: A Comparative Analysis of Neural Networks and Tsetlin Machin*e," 2020 27th IEEE International Conference on Electronics, Circuits and Systems (ICECS), Glasgow, UK, 2020, pp. 1-4, doi: 10.1109/ICECS49266.2020.9294877.

[2] M. L. Tsetlin, ‘‘On behaviour of finite automata in random medium,’’ Avtomatika I Telemekhanika, vol. 22, no. 10, pp. 1345–1354, 1961.


</font>









