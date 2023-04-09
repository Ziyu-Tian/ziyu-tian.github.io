<div align='center' ><font size ='6'>Crops Production Optimization Analysis</font> </div>

<div align='center' ><font size ='2'>Ziyu Tian</font> </div>




- **Note that using the Surname as the file name**.

- Properly Beginning with headings and problem description with diagrams.

- Assumptions and simplifications 

- Equations and solutions for the basic problem:
    - Give the formula of optimum value of L.
    - Try **2-3** simple examples to show this formula is correct.
    - Find the optimum value of average yield.
    - Show a range of results of different values of a, b, c (d=25), compare which parameter is more critical.

- Application of solutions.

- Comments with considerable simplification in other conditions.

- Final conclusion about effectiveness.


## Introduction 

To investigate the optimum time point to harvest the crops (or replanted the machine), which could make the average yield maximum during the crops production or machine working lifetime, we set the initial model to describe the *Output - Age* relationship shown in Fig.1.1.

![](20230408203914.png)

<font size=2><center>Fig.1.1 Initial Modelling of *Output - Age* Relationship</center></font>


For this model, an initial period of zero output is to be followed by a gradually increase to max output, which is maintained for some time, before a period of decline. The target is to find the expression of the optimum value of age (time length 'L') to maximum the average output.

## Assumptions and Simplifications 

To simplify the conditions, we assume that the crops or machines working normally without any interruption and the internal properties keep unchanged during the producing lifetime.

As the graph shown in Fig.1.2, we use the maximum value of '1' refer to 100% output efficiency. From 0 to *a* is the zero region, *a* to *b*, *c* to *d* is treated as linear relationship for the purpose of simplification, and *b* to *c* is the flat region of the curve.

We fix the value of *d* is 25 in this condition.


![](20230408204117.png)

<font size=2><center>Fig.1.2 Simplified Model of *Output - Age* Relationship</center></font>

## First-stage Solutions 

#### Model Construction

If we note the output in the Y-axis is *y* ($ y\le 1$) and $L$ stand for the length of the continuous production ages. The average yield $\bar{Y}$ can be expressed by the integration of output divided by the stopped age $L'$:

$$
\bar{Y} = \displaystyle\frac{\int _0 ^{L'}y{\rm d}L}{L'}\tag{1.1}
$$

After the simplification of the formula, we can get the expression below:

$$
\bar{Y} = - \displaystyle\frac{1}{2(d-c)}L + \frac{d}{d-c} + \frac{1}{L}[\frac{1}{d-c}(\frac{1}{2}c^2-dc)+ c - \frac{a+b}{2}]\tag{1.2}
$$

Using the formula 1.2 above, the optimum length $L'$ can be found:

$$
L' = \sqrt{(d-c)(a+b-2c)+2cd-c^2}\tag{2}
$$


#### Testing and Feedback
Now that we got the expression of the optimum length, we have done several simple test of this model with different values of *a*, *b* and *c* shown in table.1:

![](20230409111247.png)
<font size=2><center>Table.1 Simplified Model of *Output - Age* Relationship</center></font>
