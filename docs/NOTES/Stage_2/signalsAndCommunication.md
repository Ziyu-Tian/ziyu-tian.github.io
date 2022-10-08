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

- A message information contains the control parameters of carrier signal of a carrier signal, so as to impress the information onto the carrier.


#### 4.1: The Message 

- The message can be digital, analogue or multiple.
- Analogue message, demoted by $*m(t)*$.
- Digital message, denoted by $d(t)$.


#### 4.2: The Carrier 

- The carrier can be a 'sin' or a 'pulse train'.
- If we use a 'cosine' carrier:

$$
v_s(t) = V_c\cos{(2\pi f_c t+\phi _c)}
$$

- The message can varies in amplitude, frequency and  phase, i.e the AM, FM and PM.


## II: Amplitude Modulation 

### 1: Schematic Diagram of AM 

![](image/2022-09-26-10-26-19.png)

- $v_s(t)=(V_{DC}+m(t))\cos {(2\pi f_c t)}$
- $V_{DC}$ is a variable voltage, which can be 0 to infinite volts.

### 2: Equations for DSB-AM 

* **Double Sideband Amplitude Modulation - DSBAM**:

- If we note the message: $m(t)=V_m\cos{(2\pi f_m t)}$.
- The trigonometric way can be usd to expand:


$v_s(t)=V_{DC}\cos{(2\pi f_c t)}+\frac{V_m}{2}\cos{(2\pi (f_c+f_m)t)}+\frac{V_m}{2}\cos{(2\pi (f_c-f_m)t)}$



![](image/2022-09-26-10-31-04.png)

### 3: Spectrum and Waveforms 

![](image/2022-09-26-10-46-56.png)

![](image/2022-09-26-10-47-16.png)

- It can be found that the message is stored twice in the double **envelope**.

### 4: Modulation Depth 

- The $\frac{V_{m}}{V_{DC}}$ is defined as the **modulation depth**.
- Modulation Depth $m=\frac{Message}{Carrier}$.


### 5: Double Sideband Modulation Types 

- Double Sideband Amplitude Modulation, DSB-AM, with carrier 

- Double Sideband Diminished (Pilot) Carrier, DSB-DimC ($V_{DC}$ is small)

- Double Sideband Suppressed Carrier, DSB-SC (no $V_{DC}$, no carrier).


### 6: Graphical Representation of Modulation Depth and Modulation Types 

![](image/2022-09-26-10-53-53.png)

![](image/2022-09-26-10-54-19.png)

![](image/2022-09-26-10-55-31.png)

![](image/2022-09-26-10-56-27.png)

- The phase shift may exist, while the information is stored.



### 7: Trapezoid Method of Measuring Modulation Depth 

- For the multiple message signals instead of only one 'sin' single tone, it is difficult to determine the modulation depth.
- So we use the X-Y mode in the oscilloscope, connecting the message signals
to the x-input and AM signals to y-input.
- The trapezoid can be used to justify the modulation depth.

#### 7.1: Trapezoid when m < 1 

![](image/2022-09-26-10-59-57.png)

#### 7.2: Trapezoid when m = 1

![](image/2022-09-26-11-00-28.png)

#### 7.3: Trapezoid when m > 1

![](image/2022-09-26-11-01-10.png)

### 8: DSB-SC from a Balanced Modulator (Used in AM experiment)

![](image/2022-09-26-13-33-11.png)

### 9: Bandwidth Requirement for DSB-AM 

- The message signals $m(t)$ will not be a single sine, but a band of frequencies extending up to $B$ Hz as shown.

![](image/2022-09-26-13-35-36.png)

![](image/2022-09-26-13-35-57.png)

- Bandwidth is two times of the highest frequency in the message.

### 10: Power Considerations in DSB-AM 

- For the AM: 

$$
v_s(t)=V_{DC}\cos{(2\pi f_c t)}+\frac{V_m}{2}\cos{(2\pi (f_c+f_m)t)}+\frac{V_m}{2}\cos{(2\pi (f_c-f_m)t)}

$$


![](image/2022-09-26-17-31-33.png)

- Noted that the $P_{RMS}=(\frac{V}{\sqrt{2}})^2\times \frac{1}{R_L}$ is only suitable for sin (cos) functions.

* $P_T=\frac{V_{DC}^2}{R_L}(1+\frac{m^2}{2})$

* If we note $P_C=\frac{v_{DC}^2}{2R_L}$

$$
\frac{P_{USB}}{P_T}=\frac{P_c\frac{m^2}{4}}{P_c(1+\frac{m^2}{2})}=\frac{m^2}{4+2m}
$$

### 11: Single Sideband Amplitude Modulation 

![](image/2022-09-26-18-09-57.png)

- We use BPF to filter one of the sideband.

![](image/2022-09-26-18-11-43.png)

- After the BPF:

![](image/2022-09-26-18-11-58.png)

* The BPF filter removes the LSB then the SSB-AM will be:

$$
v_s(t)=V_{DC}\cos{(2\pi f_ct)}+\frac{V_m}{2}\cos{(2\pi (f_c+f_m)t)}
$$

* For SSB-SC, output signal will be:

$$
v_s(t)=\frac{V_m}{2}\cos{(2\pi (f_c+f_m)t)}
$$




### 12: Bandwidth Requirement for SSB-AM 

![](image/2022-09-26-18-17-11.png)

For the SSB-SC the bandwidth is reduced since there is no carrier component.

### 13: Power in SSB 

For the SSB signal $v_s(t)=V_{DC}\cos{(2\pi f_c t)}+\frac{V_m}{2}\cos {(2\pi (f_m +f_c))t}$ 

the power is:

$$

P_{SSB}=\frac{v_{DC}^2}{2R_L}+\frac{V_m ^2}{8R_L}

$$




### 14: Demodulation of AM Signals

#### 14.1: Envelope or Non-coherent Detection 

![](image/2022-09-26-18-45-53.png)

* The capacitor charges rapidly and thereby follows the applied voltages up to the positive peak when the diode is conducting, so: 

$$
R_sC << 1/f_c
$$




* After the positive peak, the voltage reduced so that the diode switched off and the capacitor begin to discharging in $R_L$. The discharging continue slowly between the positives peaks of the carrier voltage but no longer than the message period.


$$
\frac{1}{f_c} << R_L C << \frac{1}{W}
$$


![](image/2022-09-26-18-48-58.png)


#### 14.2: Synchronous or Coherent Demodulation 

![](image/2022-09-26-18-50-38.png)

* The local oscillator must be coherent in both frequency and phrase with the carrier wave.

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

- DSB-AM signals can be demodulated with envelope detector simply.
- DSB-SC and SSB-SC require much less power than DSB-AM and SSB-AM, but more complicated receiver.
- SSB-AM use half the bandwidth of DSB-AM.
- SSB-SC can cope better with small changes in frequencies and phases caused by local oscillator.


## III: Frequency Modulation and Demodulation

### 1: Angle Modulation - FM

* Consider the general carrier $v_s(t) = V_c\cos{(2\pi f_c t + \phi _c)}$

* $2\pi f_c t + \phi _C$ is the angle of the carrier.

* Frequency Modulation by varying f_c$, or phase modulation by varying $\varphi _c$.

### 2: Frequency Modulation 

- In FM, if we note the carrier as 

$$
v_s (t) = V_c\cos{(2\pi f)}
$$

- A frequency modulated carrier can be expressed as:

$$
v_s(t)=V_c\cos{(2\pi (f_c+ frequency \quad deviation)t)}
$$

where the frequency deviation depend on the *m(t)*.


- As the carrier frequency may change so a instantaneous carrier signal is needed. We note:

$$
V_c\cos{(2\pi f_i t)} = V_c\cos{(\varphi_i)}
$$

where $\varphi _i$ is the instantaneous angle which is $2\pi f_i t$ and $f_i$ is the instantaneous frequency,
$f_i = f_c + frequency \quad deviation$.

- Now we need some re-arranges of the angle $\varphi$. 

- As $\varphi _i= 2\pi f_i t$, the $\varphi_i$ is a instantaneous value, so we can get $\frac{d\varphi _i}{dt}=2\pi f_i$, or $f_i = \frac{1}{2\pi}\frac{d\varphi _i}{dt}$

We can find that frequency is proportional to the rate of change of angle.

- If we note the $f_c$ is the unmodulated carrier and $f_m$ is the modulating frequency, then we may deduce:

$$
\begin{align*}
f_i &=f_c +frequency\quad deviation \\
 &= f_c +\Delta f_c\cos{(2\pi f_m t)}  \\
 &= f_c +f_i \\
 &= \frac{1}{2\pi}\frac{d\varphi _i}{dt}  
\end{align*}
$$

Where the $\Delta f_c$ called the **peak deviation** of the carrier.

- Then we can get the equation:

$$
\displaystyle\frac{d\varphi_i}{dt} = 2\pi f_c + 2\pi \Delta f_c\cos{(2\pi f_m t)}
$$

- Integrate the both side:

$$
\int{\frac{d\varphi _i}{dt}}{\rm d}t = \int{[2\pi f_c + 2\pi \Delta f_c\cos{(2\pi f_m t)}]}{\rm d}t
$$

- Therefore:

$$
\varphi _i = 2\pi f_c t + \displaystyle\frac{2\pi \Delta f_c\sin{2\pi f_m t}}{2\pi f_m}
$$

- Get back to the carrier signal:

$$
v_s (t) = V_c \cos{(2\pi f_c t+\displaystyle\frac{\Delta f_c\sin{2\pi f_m t}}{f_m})}
$$

- The ratio $\displaystyle\frac{\Delta f_c}{f_m}$ is called the **Modulation Index** denoted $\beta$.

$$
\beta = \displaystyle\frac{Peak\quad frequency\quad Deviation}{Modulating\quad frequency}
$$

- $m(t)$ is usually considered as 'a single tone modulating signal' of the form:

$$
m(t) = V_m \cos{(2\pi f_m t)}
$$

- The equation of $v_s(t)$ can be expressed as a **Bessel Series**：

$$
v_s(t) = V_c\int 
$$