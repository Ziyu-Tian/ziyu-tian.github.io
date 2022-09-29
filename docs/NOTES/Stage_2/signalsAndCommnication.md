# Signals and Communications 

## I: Introduction to a Communication System

### 1: Communication Systems

![](image/2022-09-26-10-19-07.png)

- Noise in the systems: external noise and circuits noise reduces the quality of the output. 

### 2: General Digital Communication System Model 

![](image/2022-09-26-10-20-32.png)

- Source coding: compressing the signals 
- Error control coding: add extra bits (randoms)


#### 2.1: Coder/Decoder (CODEC)

![](image/2022-09-26-10-21-53.png)

- Sampling: signals at the particular time 
- Quantitation: reducing the binary code 



#### 2.2: Modulator/Demodulator (MODEM)

- Made of modulator and demodulator 


### 3: Radio Transmission 

-  Aerial dimensions are of the same order as the wavelength $\lambda$ of the signal.
-  $\lambda = \frac{c}{f}$, for $c=3\times 10^8$ m/s in free space. 



### 4: Modulation 

- A message information contains the control parameters of carrier signal.


#### 4.1: The Message 

- The message can be digital, analogue or multiple.


#### 4.2: The Carrier 

- The carrier can be a 'sin' or a 'pulse train': $$


## II: Amplitude Modulation 

### 1: Schematic Diagram of AM 

![](image/2022-09-26-10-26-19.png)

- $v_s(t)=(V_{DC}+m(t))\cos {(2\pi f_c t)}$
- $V_{DC}$ is a variable voltage, which can be 0 to V+ volts.



### 2: Equations for DSB-AM 

* **Double Sideband Amplitude Modulation - DSBAM**:

$v_s(t)=V_{DC}\cos{(2\pi f_c t)}+\frac{V_m}{2}\cos{(2\pi (f_c+f_m)t)}+\frac{V_m}{2}\cos{(2\pi (f_c-f_m)t)}$

![](image/2022-09-26-10-31-04.png)

### 3: Spectrum and Waveforms 

![](image/2022-09-26-10-46-56.png)

![](image/2022-09-26-10-47-16.png)

### 4: Modulation Depth 


### 5: Double Sideband Modulation Types 

- Double Sideband Amplitude Modulation, DSB-AM, with carrier 

- Double Sideband Diminished (Pilot) Carrier, DSB-DimC

- Double Sideband Suppressed Carrier, DSB-SC 

### 6: Graphical Representation of Modulation Depth and Modulation Types 

![](image/2022-09-26-10-53-53.png)

![](image/2022-09-26-10-54-19.png)

![](image/2022-09-26-10-55-31.png)

![](image/2022-09-26-10-56-27.png)

### 7: Trapezoid Method of Measuring Modulation Depth 

#### 7.1: Trapezoid when m < 1 

![](image/2022-09-26-10-59-57.png)

#### 7.2: Trapezoid when m = 1

![](image/2022-09-26-11-00-28.png)

#### 7.3: Trapezoid when m > 1

![](image/2022-09-26-11-01-10.png)

### 8: DSB-SC from a Balanced Modulator (Used in AM experiment)

![](image/2022-09-26-13-33-11.png)

### 9: Bandwidth Requirement for DSB-AM 


![](image/2022-09-26-13-35-36.png)

![](image/2022-09-26-13-35-57.png)


### 10: Power Considerations in DSB-AM 


![](image/2022-09-26-17-31-33.png)

* $P_T=\frac{V_{DC}^2}{R_L}(1+\frac{m^2}{2})$

* If we note $P_C=\frac{v_{DC}^2}{2R_L}$

$$
\frac{P_{USB}}{P_T}=\frac{P_c\frac{m^2}{4}}{P_c(1+\frac{m^2}{2})}=\frac{m^2}{4+2m}^2
$$

### 11: Single Sideband Amplitude Modulation 

![](image/2022-09-26-18-09-57.png)

![](image/2022-09-26-18-11-43.png)

![](image/2022-09-26-18-11-58.png)

* The BP filter removes the LSB then the SSB-AM will be:

$$
v_s(t)=V_{DC}\cos{(2\pi f_ct)}+\frac{V_m}{2}\cos{(2\pi (f_c+f_m)t)}
$$

* For SSB-SC, output signal will be:

$$
v_s(t)=\frac{V_m}{2}\cos{(2\pi (f_c+f_m)t)}
$$




### 12: Bandwidth Requirement for SSB-AM 

![](image/2022-09-26-18-17-11.png)


### 13: Power in SSB 

Same as the DSB Power 

### 14: Demodulation of AM Signals

#### 14.1: Envelope or Non-coherent Detection 

![](image/2022-09-26-18-45-53.png)

![](image/2022-09-26-18-48-58.png)


#### 14.2: Synchronous or Coherent Demodulation 

![](image/2022-09-26-18-50-38.png)

##### 14.2.1: Coherent Local Oscillator 

![](image/2022-09-26-18-53-40.png)

If DSB-AM input = $(V_{DC}+m(t))\cos{(2\pi f_ct)}$

$$
\begin{align*}
V_x &= (V_{DC}+m(t))\cos{(2\pi f_ct)}\cos{(2\pi f_ct)} \\
&= \frac{V_{DC}}{2}+\frac{V_{DC}}{2}\cos{(4\pi f_C t)}+\frac{m(t)}{2}+\frac{m(t)}{2}\cos{(4\pi f_ct)}
\end{align*}
$$

![](image/2022-09-26-19-11-46.png)

![](image/2022-09-26-19-12-00.png)


##### 14.2.2: Frequency and Phrase Errors in Synchronous Demodulation: DSB-SC 

![](image/2022-09-26-19-49-40.png)

The equation for DSB-SC:

$v_s(t)=m(t)\cos{(2\pi f_ct)}$, where $V_{DC}=0$

LPF remove the $2f_c$ component. 

$ V_{out}=\frac{m(t)}{2}\cos{(2\pi \Delta ft+ \Delta \phi)}$

##### 14.2.3: Frequency and Phrase Errors in Synchronous Demodulation: SSB-SC 

![](image/2022-09-26-19-59-49.png)

### 15: Comparison of DSB and SSB 　




<!--
MATLAB Simulink Lab need to be finished 
!-->

