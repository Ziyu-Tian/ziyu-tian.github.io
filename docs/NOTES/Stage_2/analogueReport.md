<div align='center' ><font size ='6'>Operational Amplifier Lab Report</font> </div>

<div align='center' ><font size ='2'>Ziyu Tian</font> </div>

## Abstract 

This experiment explored the properties of inverting operational amplifier (op-amp in short), which contain the plotted frequency response graphs, Gain-Bandwidth Product, slew rate and offset voltage, validated the mathematical operation of the summing op-amp and difference op-amp, discussed how the Common Mode Rejection Ratio (CMRR in short) affect the efficiency of amplifier.

## Introduction 

The op-amp is a very high-gain (open-loop gain tending to infinity), DC-coupled differential voltage amplifier with very large (tending to infinity) input impedance and extremely low output impedance[1], which has six terminals: one non-inverting input is denoted by positive (+) sign, one inverting denoted by (−) sign, two where positive and negative power supplies (+VCC and −VCC or V+, & V−), as shown in Fig.1. As a active circuit element, op-amp is designed to perform mathematical operations of addition, subtraction, multiplication, division, differentiation, and integration[2].

This experiment aimed at validating the bandwidth, cut-off frequency, slew rate, distortion phenomenon and the offset voltage of inverting op-amps, exploring the operation of the summing and difference op-amps with CMRR properties. To achieve the aims above, the tasks have been done as below:

- Calculate the total gain with the $V_{out}$ and $V_{in}$ in oscilloscope.

- Determine the bandwidth using the gain-bandwidth product provided in data sheet shown in Fig.2.

- Plot the frequency response and determine the cut-off frequency, then change another set of resistance repeat the test above.

- Increasing the frequency, observe the full power bandwidth then calculated the slew rate.

- Reconnect the circuit, determine the offset-voltage.

- Change the circuit to summing op-amp and difference op-amp, observing the operations and calculating the CMRR.


![](image/2023-01-03-08-02-48.png)
<font size=2><center>Fig.1. The Op-amp in symbolic (left) and IC (right) form  </center></font>

![](image/2023-01-03-08-33-08.png)
<font size=2><center>Fig.2. The Op-amp data sheet </center></font>

## Procedure 

- For inverting amplifier experiment, we use the op-amp designed as Fig.3 with $R_1=1\quad k\Omega$. Apply the input as 1 kHz, 0.1 $V_{pp}$, then observe and record the $V_{in}$ and $V_{out}$ to calculate the gain using formula:
$$
A_{experiment}= \displaystyle\frac{V_{out}}{V_{in}}\tag{1.1}
$$

$$
A_{theory}= -\displaystyle\frac{R_2}{R_1}\tag{1.2}
$$

then compare the gain with theoretical value calculated by formula 1.2. Change $R_2$ to 470 $\Omega$ and voltage to 0.025 $V_{pp}$ do above procedure again.

- Increasing the frequency, measuring the gain up to the cut-off frequency and plotting the data. Observe the cut-off frequency from the graph and calculate the the bandwidth using the formula:

$$
Bandwidth = \displaystyle\frac{GBP}{Gain}\tag{2}
$$

- Change $R_2$ to 10 k$\Omega$ and repeat the steps measuring frequency response. Compare these result with the theoretical values in data sheet (Fig.2).

- Change the values of both $R_1$ and $R_2$ to 10 k$\Omega$ with the input signal of 1 kHz.

- Adjust the input signal until the output signal has a $V_{pp}$ of 10 V.

- Keep the input signal in same level, increase the frequency until the output signal distorts. Record the full power bandwidth at the frequency distortion begin point. Then keep increasing the frequency until the triangle wave occurs, record this value of frequency.

- Add $V_{pp}$ and period measurements in the oscilloscope, calculate the slew rate of this op-amp using the formula:

$$
Slew\quad rate = \displaystyle\frac{dV}{dt} = \frac{V_{pp}}{\frac{1}{2}T}\tag{3}
$$

then compare this value with the theoretical slew rate in data sheet Fig.2.

- Reconnect the circuit with Fig.4 and set $R_1$ = 1 k$\Omega$ and $R_2$ = 470 k$\Omega$. 

- According to the formula:

$$
V_o = (1+\displaystyle\frac{R_2}{R_1})V_{off}\tag{4}
$$

measuring the output voltage $V_o$, then calculate the offset voltage.

- Construct the summing circuit designed as Fig.5, with $R_1$ = 10 k$\Omega$ and $R_2$ = 22 k$\Omega$.

- Connect one of the summing op-amp input to 1 kHz sine wave with 100 $mV_{pp}$.

- Connect the lower terminal of potentiometer to ground and the upper terminal to +15 V pin, then connect the potentiometer output to another input of the summing op-amp. So that the input voltage of the op-amp can be changed easily.

- Increase the DC input using potentiometer, then observe and record the summing effect of the output signal.

- Construct the difference amplifier designed as Fig.6 with $R_1$ = 1 k$\Omega$, $R_2$ = 22 k$\Omega$.

- Connect the both input of the op-amp to 1 $V_{pp}$, 1 Hz sine wave, which is the common mode of amplifier.Measure the output using multimeter, calculated the gain in this condition, $A_{CM}$.

- Keep one of the op-amp input 1 kHz sine wave, change another input to the ground. Measure the output suing multimeter, calculated the gain in this condition, $A_{DM}$.

- Determine the Common Mode Rejection Ratio (CMRR) using the formula given by:

$$
CMRR = 20\log_{10}{\displaystyle\frac{A_{DM}}{A_{CM}}}(dB)\tag{5}
$$


![](image/2023-01-03-09-43-59.png)
<font size=2><center>Fig.3. The inverting op-amp </center></font>

![](image/2023-01-03-17-53-23.png)
<font size=2><center>Fig.4. Off-set voltage Calculation </center></font>

![](image/2023-01-03-18-08-47.png)
<font size=2><center>Fig.5. Summing op-amp </center></font>

![](image/2023-01-03-20-29-30.png)
<font size=2><center>Fig.6. Difference op-amp </center></font>


## Results and Discussion 

- Ensure the demonstration and the figure in the same page and using the figure number.
- Describe the results with figures.
- Explain the results - why do they look like that.
- Connect with the FM theory (validate the result)

## Conclusion

- Summary of the experiment and result
- Passive voice needed


## References 

[1]:R.Prasad, *Analog and Digital Electronic Circuits*. Springer, 2021, p.678.

[2]C.K.Alexander and M.N.O.Sadiku, *Fundamentals of electric circuits*. New York, Ny: Mcgraw-Hill Education, 2017, p.599.
‌
‌


