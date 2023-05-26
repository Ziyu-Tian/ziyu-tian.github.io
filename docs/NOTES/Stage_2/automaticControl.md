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