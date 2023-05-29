# Automatic Control Systems 

- **Control variables**: is the output of system that is measured or controlled.

- **Plant**: The plant is tge piece of equipment which performs a particular operation.

- **Dynamics**: properties describing the behavior of the system.

## 1: Dynamic Systems and Control 

### 1.1: System model 

- The model is derived from the ODE describing the system, which can be obtained by analyzing the physical processes.

#### 1.1.1: Electrical system 

![](image/2023-05-25-10-55-39.png)

#### 1.1.2: Mechanical System 

![](image/2023-05-25-10-56-15.png)


### 1.2: First-order ODE 

#### 1.2.1: Analytic Methods 

- Separating variables:

![](image/2023-05-25-11-03-43.png)

- Integrating factor:

![](image/2023-05-25-11-05-58.png)

#### 1.2.2: Numerical solution (using Simulink)

- For example of $Ax' +Bx = u$:

![](image/2023-05-25-11-13-21.png)

- Note that the initial condition can be changed in the integrator block.

#### 1.2.3: First-order ODE summary 

- The system is considered stable if reaches steady state.

- For sin input, output follows input after transient with changes in magnitude.


### 1.3: Second order ODE 

#### 1.3.1: Analytical solution 

- For real and not equal roots:

![](image/2023-05-25-16-05-40.png)

- For equal roots:

![](image/2023-05-25-16-06-40.png)

- For complex roots:

![](image/2023-05-25-16-07-49.png)


#### 1.3.2: Undamped system 

![](image/2023-05-25-16-25-54.png)

#### 1.3.3: Space of roots 

![](image/2023-05-25-16-26-18.png)

#### 1.3.4: Natural frequency, damping frequency and damp factor 

- For a second order ODE shown as below:

$$
x'' + 2\zeta \omega_n x' + \omega_n ^2x = 0
$$

- $\zeta$ is the damping factor and $\omega_n$ is the natural frequency of the system.

- The root can be gained from $\zeta$ and $\omega_n$.

![](image/2023-05-25-16-36-07.png)

#### 1.3.5: NonHomogeneous (NH) ODE 

- $x''+Ax'+Bx = u$

![](image/2023-05-25-16-42-39.png)


## 2: Transfer functions 

- Using the Laplace Transform, we can convert the the TF in time-domain to s-domain.

![](image/2023-05-25-17-02-14.png)

- Formula for differentiation:

![](image/2023-05-25-17-49-52.png)

### 2.1: Characteristic Equation and Order 

- The Characteristic equation (CE) is the denominator of transfer function.

- The order of the ODE is the order of the system.

- In s-domain, it can also be determined by the order of 's'.

### 2.2: Pole location in s-plane 

- In $G(s) = \frac{N(s)}{D(s)}$, the roots of numerator are called zeros and the roots of denominator is called poles.

![](image/2023-05-26-06-20-32.png)


- MATLAB methods to find roots of polynomial:

```MATLAB
num = [1 4];
den = [1 3 -6];
roots(num);
```

- MATLAB methods to find poles/zeros plot:

```MATLAB
num = [1 4];
den = [1 3 6];
G = tf(num,den);
pzmap(G);
[p,z] = pzmap[G];
```

![](image/2023-05-26-06-24-43.png)

- The function 'conv' can be used to combine two terms.

### 2.3: Final value theorem 

- The final-value theorem can be used to determine the ss value.

![](image/2023-05-26-06-30-06.png)

![](image/2023-05-26-06-30-36.png)

### 2.4: Block diagram 

![](image/2023-05-26-06-32-04.png)

- In matlab,

```MATLAB 
G = series(g1,g2);
G = parallel(g1,g2);
```


## 3: Time domain Characteristic 

- The input signals can be one of below:

![](image/2023-05-26-08-29-16.png)


- To find the step response using matlab:

```MATLAB
step(num,den,15);
```
![](image/2023-05-26-08-31-13.png)


- The transfer function can be expressed as form of:
$$
\displaystyle\frac{Y(s)}{X(s)}=\frac{k}{\tau s+1}
$$

- $\tau$ is the time constant.

### 3.1: Second order systems 

- The second order system can be expressed in the form of:

![](image/2023-05-26-08-46-17.png)

![](image/2023-05-26-08-40-30.png)

![](image/2023-05-26-08-41-13.png)

![](image/2023-05-26-08-41-35.png)

![](image/2023-05-26-08-42-07.png)

![](image/2023-05-26-08-43-44.png)


### 3.2: Time-domain Characteristic in graph 

![](image/2023-05-26-08-49-47.png)

### 3.4: Extra poles and zeros

- If we have only one pole (or pair of complex roots) that is closed to the real-axis then we say this pole is the **DOMINANT** pole for the system.

- The dominant poles must be at least five to ten times closer to the imaginary axis than others.

- If the pole is far away from i-axis, it can be ignored in TF.


## 4: Closed loop system 


- For the system, with inputs back to system to sees output, this is called Feedback.

- A system with feedback is called a closed-loop system.

![](image/2023-05-27-07-26-03.png)

- For a general CL system:

![](image/2023-05-27-07-26-41.png)

- Use the MATLAB instruction to calculate feedback CLTF:

```MATLAB 
gcl = feedback(gol,h);
```

- $\omega_n$ and $\zeta$ can also be found:

![](image/2023-05-27-07-43-46.png)

### 4.1: Systems classification 

![](image/2023-05-27-07-45-40.png)

- The systems can also can be classified by the number of poles at the origin OL system:

![](image/2023-05-27-07-48-40.png)

### 4.2: Error constants 

![](image/2023-05-27-07-55-41.png)
![](image/2023-05-27-10-35-17.png)
![](image/2023-05-27-10-35-28.png)
![](image/2023-05-27-10-36-16.png)
![](image/2023-05-27-07-56-46.png)

- Marginally stable means the poles are in the i-axis, so $ s = j\omega$:

![](image/2023-05-27-10-49-37.png)

## 5: Root Locus 


- For example of a first-order system:

![](image/2023-05-27-12-42-23.png)

![](image/2023-05-27-12-42-47.png)

- For a second-order system:

![](image/2023-05-27-12-45-08.png)

![](image/2023-05-27-12-45-15.png)

- Matlab instruction to draw root locus:

```MATLAB 
rlocus(g1);
```

### 5.1: Graphical method 

![](image/2023-05-27-12-55-40.png)

![](image/2023-05-27-12-56-41.png)

### 5.2: Angle and magnitude conditions 

- For the transfer function:

$$
G_{CL}(s) = \displaystyle\frac{G(s)}{1+G(s)H(s)}
$$

- To make sure the poles in the roots locus:

$$
|G(s)H(s)| = -1
$$

and 

![](image/2023-05-28-06-40-19.png)

![](image/2023-05-28-06-40-58.png)


### 5.3: The graphical and analytic method to justufy the root-locus point 

- Graphical methods:

![](image/2023-05-28-08-12-09.png)

![](image/2023-05-28-08-13-29.png)

![](image/2023-05-28-08-13-46.png)

- Analytic methods:

![](image/2023-05-28-08-14-22.png)


### 5.4: Design Summary of root locus 

![](image/2023-05-28-10-11-52.png)


## 6: PID control 

- 'P' for proportional, 'I' for integration, 'D' for differentiation.

![](image/2023-05-28-10-57-45.png)

- For a PID controller:

![](image/2023-05-28-10-56-01.png)

![](image/2023-05-28-10-56-32.png)

### 6.1: PID tuning 

- Ziegler Nichols I:

![](image/2023-05-28-10-59-34.png)

![](image/2023-05-28-10-59-53.png)


- Ziegler Nichols II:

![](image/2023-05-28-11-15-31.png)


![](image/2023-05-28-11-19-48.png)

## 7: Design Based on Root Locus 

### 7.1: Lead Control 

- Lead control is similar to PD control. It is used when ss properties of the system is fine but poor performance of response time, i.e. we want to move poles without changing the gain very much.


![](image/2023-05-29-02-14-36.png)

- The method is add a zero and a pole simultaneously (according to the Argument Criterion, $\sigma \arg{poles} - \sigma \arg{zeros} = \pi$).

- The pole would be moved left, so that increase the response time.

#### 7.1.1: Design Strategy 

- Using the desired condition of $\omega_n$ and $\zeta$ to find the roots of CLTF.

- Check if a P-controller is enough.

- Place the zero at the real-part of the desired pole location (diminished pole and zero argument).

- Using Magnitude Angle Criterion finding position of compensated pole:

![](image/2023-05-29-02-22-06.png)

- Using Magnitude Criterion ($|GH| = 1$)finding the K.

#### 7.1.2: Example of lead control 

![](image/2023-05-29-02-23-48.png)

- Try P-controller firstly.

- The CL poles can be found:

![](image/2023-05-29-02-26-12.png)

- Finding the K:

![](image/2023-05-29-02-26-57.png)

- The result not suitable for the desired system:

![](image/2023-05-29-02-29-11.png)

- Try Lead-Controller:

- The desired roots of poles:

![](image/2023-05-29-02-31-43.png)

![](image/2023-05-29-02-32-23.png)

- Finding compensated pole location:

![](image/2023-05-29-02-33-00.png)

- The system response faster compared to the P-controller:

|---|---|
|![](image/2023-05-29-02-36-30.png)|![](image/2023-05-29-02-36-49.png)|


### 7.2: Lag Control 

![](image/2023-05-29-02-37-33.png)

### 7.2.1: Example of Lag Control 

![](image/2023-05-29-02-38-31.png)

![](image/2023-05-29-02-39-12.png)

![](image/2023-05-29-02-39-35.png)