# Analog Electronics 

## I: Introduction & Overview

### 1: Introduction 

- Consider what can affect these circuits (noise etc)

- Consider how to improve designing circuits 

- Focus on 2 examples:
    - instrumentation amplifier for sensors
    - Power amplifier 

### 2: Basic Laws 

#### 2.1: Kirchoff's Law 

![](image/2022-11-14-08-10-54.png)

#### 2.2: The diode basics 

![](image/2022-11-14-08-11-27.png)

![](image/2022-11-14-08-11-57.png)

#### 2.3: Ideal Sources 

![](image/2022-11-14-08-12-24.png)

#### 2.4: Equivalent circuits 

![](image/2022-11-14-08-13-07.png)

#### 2.5: Small and Large signal modelling 

![](image/2022-11-14-08-15-04.png)

- The input signal can be separated to the large signal (DC component) and small signal (AC component).

- The DC component is called **the DC bias** (Quiescent point, Q point, or the operating point, bias point)

![](image/2022-11-14-08-18-37.png)

![](image/2022-11-14-08-21-00.png)

#### 2.6: Small signal conductance 

For AC model:

![](image/2022-11-14-11-14-12.png)

we tend to think in terms of conductance g:

$$
\frac{1}{r_{AC}} = g_{ac} = \frac{\Delta I_{AC}}{\Delta V_{AC}}
$$

noted that we typically use $i_{ac}$ and $v_{ac}$ short for $\Delta I_{AC}$ and $\Delta I_{AC}$。

![](image/2022-11-14-11-30-56.png)

#### 2.7: Load line analysis 

![](image/2022-11-14-11-31-57.png)

![](image/2022-11-14-11-32-07.png)

### 3: Noise 

- Noise refers to unwanted signals.

- Noise can originate in the sensor, lines or amps.

![](image/2022-11-14-11-34-02.png)

#### 3.1: Thermal Noise 

- Also known as Johnson-Nyquist noise.

- Thermal noise from random motions of electrons in conductors.

#### 3.2: Shot noise 

- Also known as Poisson noise.

- From the quantum nature of charge flow.

## II: Filters & Bode Plots 

### 1: Passive frequency filtering 

#### 1.1: Low Pass filter 

![](image/2022-11-14-11-38-41.png)

- For resistance, $Z_R=R$; for capacitance, $Z_C = X_C = \frac{1}{j\omega C} = \frac{1}{2\pi f C}$

- Low pass filter can be considered as a potential divider:

$$
V_{OUT} = V_{in}\times (\frac{Z_C}{Z_{total}})
$$

The total impedance $Z_{total}$ is given by:

$$
Z_{total} = \sqrt{R^2 +X_C ^2}
$$

So 

$$
V_{out} = V_{in} \times (\frac{X_C}{\sqrt{R^2+X_c ^2}})
$$

- If we increase the frequency, the output voltage will be:

![](image/2022-11-14-11-45-04.png)

And the gain in dB = 20log(Vout/Vin):

![](image/2022-11-14-11-46-18.png)

- This plot is known as a **Bode Plot**.

- There is a frequency at which $X_c = R$, which is know as the cut-off frequency ($f_c$).

- The cut-off frequency is 100 Hz as above.

- The gain in dB in $f_c$ usually defines the band-width.

#### 1.2: High Pass Filter 

![](image/2022-11-14-11-48-19.png)

Use the same method, the formula is:

$$
V_{out} = V_{in} \times (\frac{R}{\sqrt{R^2 +X_c^2}})
$$

- If we increase the frequency, the output will be:

![](image/2022-11-14-12-48-12.png)

![](image/2022-11-14-12-48-31.png)

#### 1.3: Multi-stage Filter 

![](image/2022-11-14-12-51-07.png)

$$
V_{out2} = V_{in1} * (\frac{R_1^2}{R_1^2+X_{c1}^2})
$$

#### 1.4: Passive bandpass filter 

![](image/2022-11-14-13-07-20.png)

**A band pass filter** is to be constructed using RC components will only allow a range of frequencies to pass, calculating the 