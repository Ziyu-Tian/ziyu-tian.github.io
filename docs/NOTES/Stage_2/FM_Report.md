<div align='center' ><font size ='6'>Frequency  Modulation and Frequency Shift Keying Lab Report</font> </div>


## Abstract 

This experiment calculated the frequency conversion factor $\alpha$, generated and validated the frequency spectrum of narrow-band FM (NBFM) and wide-band frequency modulation (WBFM) with FM theory, verified the composition ratio of FM carrier power and total power in final result. Carried out the frequency shift keying (FSK) and frequency demodulation with the plotted measurement graph of demodulated frequency response of slope detector and ratio detector, which satisfied the theoretical properties.

## Introduction

The main principle of this experiment is using the formula of linear voltage-frequency convertor to calculated frequency conversion factor $\alpha$:
$$
\alpha = \frac{\Delta f_{OUT}}{\Delta V_{IN}}\tag{1}
$$
with the modulation index $\beta$ [1] calculated by:
$$
\beta = \frac{\Delta f}{f_m}\tag{2}
$$
then measuring the narrow-band FM, wide-band FM properties and frequency response of FSK to validate the result.

With these theory, this experiment mainly aimed at determining frequency conversion factor $\alpha$, using this value to verify the frequency spectrum of suppressed carrier FM, NBFM and WBFM, calculating and comparing the total power and sideband power of FM, finally research the difference type of slope detector and ratio detector. To achieve the aims above, the tasks have been done as below:

- Determine the $\alpha$ using equation (1).

- Calculate the $\beta$ using equation (1) and equation (2) when no carrier-component in frequency spectrum, then comparing the result with Bessel Function Table (Fig.1).


- Determine the max voltage of NBFM and the max voltage of WBFM when $\beta = 10$, then find the bandwidth of both spectrum.

- Calculate the total power and sideband power when $\beta = 1$.

- Plot and compare the frequency response of slope-detector and ratio-detector.


![](image/2022-12-04-22-21-11.png)
<font size=2><center>[2]Fig.1.Bessel Function Table</center></font>

## Procedure 

- To calculate the $\alpha$, we set $V_1 = 0$ for the initial condition and $V_2 = 1 V$. According to the measurement on oscilloscope, note down the $f_1$ and $f_2$ for two conditions.

- Connect the AC signal output of 1 kHz, varying the $V_m$ values, so that the number of the sidebands may change until the carrier component being suppressed, then record and compare the spectrum of signal.

- Narrow-band means there is only one pairs of sideband in spectrum[3]. Change the $V_m$ until only have one pair of sideband, record the spectrum and modulation index $\beta$.

- Determine the value of $V_m$ of WBFM with $\beta =10$ using equation (1) and equation (2), record the spectrum and bandwidth.

- Determine the total power using the formula:

$$
P_T = \frac{V_{RMS}}{R_L}\tag{3.1}
$$
and determine the sideband voltage using:
$$
P_{BL} = \displaystyle\frac{1}{R_L}\sum_{n=-\infty}^{\infty}[V_{RMS}J_n(\beta)]^2\tag{3.2}
$$

- Add square wave to oscilloscope, using FFT generate and record the spectrum of FSK signal, then calculate the $\Delta f$ between two peaks.

- Connect the wave generator as input, vary the frequencies between 4.0 MHz to 6.0 MHz, record the response value of slope detector and ratio detector.

## Result and Discussion 

In terms of the measurement, we record the values of $f_1$ adn $f_2$ using x-cursor, for the $V_1=0$ and $V_2 = 1V$ respectively in Fig.2. As the formula:
$$
\Delta f_{OUT} = f_2 -f_1\tag{4.1} 
$$
and 
$$
\Delta V_{IN} = V_2 - V_1\tag{4.2}
$$
In consequence, the $\displaystyle\alpha = \frac{f_1-f_2}{V_2 -V_1}=7.3$ kHz/V.

When there is no sine wave connect, according to equation(1) and equation(2):
$$
\beta = \frac{\alpha V_m}{f_m}\tag{5}
$$
as $V_m = 0$ of sine wave disconnected, $\beta = 0$, there is only one carrier component in spectrum as shown in Fig.3.

Varying the max voltage (shown as $V_{pp}$) in oscilloscope, we found the carrier component suppressed when $V_{pp}=600$ mV, i.e. $V_m = 300$ mV shown in Fig.4. Using equation (5), the $\beta = \displaystyle\frac{7.3 \times 0.3}{1} = 2.19$ V/kHz. Compared with Bessel Function Tables in Fig.1, the $\beta$ is close to $\beta = 2$, which have four pairs of sidebands, just as Fig.4 shown.

Continue varying the max voltage until the signal is NBFM, it is noted the $V_{pp} = 60$ mV (i.e. $V_m = 30$ mV) in Fig.5. According to equation (5), $\beta = \displaystyle\frac{7.3 \times 0.03}{1}$ V/kHz. Compared to the Bessel Function Tables in Fig.1, $\beta = 0.219$ closes to $\beta = 0.2$, which has 1 pair of sideband, verify the experimental result of NBFM.









![](image/2022-12-04-22-58-03.png)
<font size=2><center>Fig.2. $f_1$ and $f_2$</center></font>

![](image/2022-12-05-05-51-18.png)
<font size=2><center>Fig.3. Spectrum when $\beta =0$</center></font>

![](image/2022-12-05-05-51-43.png)
<font size=2><center>Fig.4. Suppressed Carrier Spectrum </center></font>

![](image/2022-12-05-06-03-05.png)
<font size=2><center>Fig.5. NBFM Spectrum </center></font>





## Reference 

[1]: S.S.Haykin, *Communication Systems*, New York: Wiley, 2010, pp. 110–111. 

[2]: L.E.Frenzel, *Principles of Electronic Communication Systems*, New York, NY: McGraw-Hill, a business unit of The McGraw-Hill Companies, Inc., 2014, pp. 159. 

[3]:L.E.Frenzel, *Principles of Electronic Communication Systems*, New York, NY: McGraw-Hill, a business unit of The McGraw-Hill Companies, Inc., 2014, pp. 160.