## I: Matrix and Vector 
### 1: Matrix 
#### 1.1: Definition and Notation 
* A method of recording hundreds of equations in engineering.<font color=#87CEEB> (eg. infinite elements with 3D nodes)</font> 
* A matrix is called "lines by column", eg. 2x3 means 2 lines and 3 columns.
* Capital letter 'A' for a matrix and lower case '$a_{ij}$' for the element of 'A', 'i' is the line and 'j' is the column.
* $A=\begin{pmatrix}1&1\\1&1\end{pmatrix}$ which is a 2x2 matrix.

#### 1.2: Special Matrix 

##### (1): Diagonal Matrix
All elements are '0' except the '\' diagonal, but the diagonal can be '0'.
e.g, $\begin{pmatrix}2&0&0\\0&3&0\\0&0&4\end{pmatrix}$

##### (2): Symmetric matrix 
$\begin{pmatrix}1&3&-7\\3&0&2\\-7&2&-5\end{pmatrix}$, $a_{ij}=a_{ji}$

##### (3): Antisymmetric matrix
$\begin{pmatrix}1&-3&7\\3&0&2\\-7&2&-5\end{pmatrix}$ , $a_{ij}=-a_{ji}$, $i\not ={j}$
    
##### (4): Upper/Lower triangular matrix 
$\begin{pmatrix}1&1&1\\0&1&1\\0&0&1\end{pmatrix}$, $i>j$, $a_{ij}=0$,which is **Upper** . 

$\begin{pmatrix}1&0&0\\1&1&0\\1&1&1\end{pmatrix}$, $i>j$, $a_{ij}=0$, which is **Lower**.

#### 1.3: Matrix Transpose
##### (1): Transpose means <font color=#87CEEB> swap </font>
$\begin{pmatrix}a&b&c \\ d&e&f\\ g&h&i \end{pmatrix}^T=\begin{pmatrix}a&d&g\\ b&e&h\\ c&f&i \end{pmatrix}$
##### (2): The Transpose of transposed matrix
$[A^T]^T=T$

#### 1.2: Matrices Algebra 
##### Scalar multiply 
- (1): Do the calculation directly. 
- (2): Only same-size matrix can do
##### Matrix Multiplication 
- Example:
$A=\begin{pmatrix}m&p\\n&q\end{pmatrix},\quad B=\begin{pmatrix}a&c\\b&d\end{pmatrix}$
- $AB=\begin{pmatrix}m&p\\n&q\end{pmatrix}.\begin{pmatrix}a&c\\b&d\end{pmatrix}=\begin{pmatrix}am+bp&cm+dp\\an+bq&cn+dq\end{pmatrix}$
- Notes that $A.B\not ={B.A}$ (mostly)
#### 1.3: Identity Matrix 
- Example:
$\begin{pmatrix}1&2\\0&1\end{pmatrix}$
- The 'I' could be 'N x N' matrix
- $I.A=A=A.I$, whilst I is different 
#### 1.4: The properties & rules of matrices 
##### (1): Equality 
All the elements are same, $a_{ij}=b_{ij}$ means '='.
##### (2): Properties of Transpose 
$(A+B)^T=A^T+B^T$, $(A^T)^T=A$
#### 1.5: Simultaneous equations & Matrices
##### Transfer the Matrix and Simultaneous equations 
- Original equations: $\begin{aligned} 2x-3y=4 \\-x+2y=1\end{aligned}$
- Matrix form: $\begin{pmatrix}2&-3\\-1&2\end{pmatrix} . \begin{pmatrix} x \\ y\end{pmatrix}=\begin{pmatrix} 4 \\ 1\end{pmatrix}$
##### (1): Determinant
- If the matrix $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, written $\det A \left| \begin{array}{cccc}a&b\\ c&d 
\end{array} \right |=ad-bc$
- If $\det A=0$, the matrix is singular.
##### (2): Inverse of a matrix 
- To solve the equation $\vec{A}X=\vec{b}$, according to $A.I=I.A$, **$X=A^{-1}\vec{b}$**.
#### 1.4: Solve the simulations equation by Gauss's Elimination 
##### (1): Elementary Row Operations (ERO)
- Firstly, change it to extended matrix form: $\left[\begin{array}{lcr|r} 1 & -3 & 1 & 1 \\ 2 & 5 & 3 &24 \\ -1 & 2 & 1 &1 \end{array}\right]$.
- Use 'add','minus','multiply' and 'divide' to change the left matrix into a upper-triangular matrix.
- Follow the rule of 'from up to down' and 'from left to right', i.e '2'$\rightarrow$'-1'$\rightarrow$'2'.
- Finally got $\left[\begin{array}{lcr|r}1&-3&1&-9\\ 0&1&2&-8 \\ 0&0&23&-46\end{array}\right]$, the solution can be solved easily.
##### (2): Finding inverse matrix by EROs 
- For Example, $A=\begin{pmatrix}2&3\\-1&4\end{pmatrix}$.
- Change $A$ and $I$ to extended matrix form, $(A|I)=\left[\begin{array}{lcr|r}2&3&1&0 \\ -1&4&0&1 \end{array}\right]$.
- Using EROs changing left-side to $I$, the right will be $A^{-1}$, $\left[\begin{array}{lcr|r} 1&0&4/11&-3/11 \\ 0&1&1/11&2/11\end{array}\right]$.
- To find the inverse matrix of 2x2 matrix,if $A=\begin{pmatrix}a&b \\ c&d\end{pmatrix}$, $A^{-1}=\frac{1}{|A|}\times A^{*}=\frac{1}{\det A}\times \begin{pmatrix}d&-b\\-c&a\end{pmatrix}$
##### (3): Determinant of 3x3 matrix 
- For Example, $\left | \begin{array}{cccc}2&3&-1 \\ 4&1&2 \\ -1&0&3\end{array} \right |=2\left | \begin{array}{cccc}1&2 \\ 0&3 \end{array} \right |-(3)\left |\begin{array}{cccc}4&2 \\ -1&3 \end{array} \right |+(-1)\left | \begin{array}{cccc} 4&1 \\ -1&0 \end{array} \right |=-37$
### 2: Vectors
#### 2.1: Definition 
- Cartesian form in right-hand set are (2,3,1) or $2\vec{i}+3\vec{j}+\vec{k}$
#### 2.2: Scalar Product (Dot product)
- Example: $W=\vec{F}.\cos\theta\vec{d}=|\vec{F}||\vec{d}|\cos\theta$, the result is a **scalar**.
- $\vec{i}.\vec{j}=0$, two vectors are perpendicular.
- $\cos\theta=\frac{\vec{a}.\vec{b}}{|\vec{a}||\vec{b}|}$
- Unit vectors: $\hat{a}=\frac{\vec{a}}{|a|}$.
- Component in one direction: $|\vec{F_1}|=\vec{F}.\hat{a}$, $\vec{F_1}=(\vec{F}.\hat{a})\hat{a}$
#### 2.3: Vector Product (Cross Product)
- In 2D, $\vec{M}=|\vec{d}||\vec{F}|\sin\theta$
- In 3D, $\vec{M}=\vec{d}\times\vec{F}=|\vec{d}||\vec{F}|\sin\theta\hat{n}$
- Corkscrew rule can justify the direction.
- $\vec{m}\times \vec{n}=\left|\begin{array}{cccc}\vec{i}&\vec{j}&\vec{k}\\ a&b&c \\ d&e&f\end{array} \right |=(ae-bd)-(af-dc)+(ae-bd)$


## II: Complex numbers
### 1: Basic Concepts
- $i^2=-1$, use 'j' in electrical engineering
- The coefficient of real number is the **real part**, the one of imaginary number is the **imaginary part**.
- If $z=a+bi$, $\bar{z}=a-bi$, which is called **complex conjugate**.
- $|z|=|a+bi|=\sqrt{a^2+b^2}$, which is the **modulus** of $z$.
### 2: Argument 
- $\arg(z_1)+\arg(z_2)=\arg(z_1z_2)$
### 3: Exponential form and applications
#### (1): Exponential Form / Polar Form 
- $z=x+yi=re^{i\theta}$, <font color=#87CEEB> $\theta=\arg(z)$, $r=|z|$ </font>
- <font color=#87CEEB> Euler's Identity:</font> $e^{i\pi}=-1$
#### (2): Sine/cosine form 
- $\cos\theta +i\sin\theta =e^{i\theta}$
#### (3): Complex roots of equations
- Try '0','$\pm 1$' and '$\pm 2$' to find a real root.
- Use **long division** find the roots of the quadratic equation.










## IV: Functions and Curves
### 1: Functions- general ideas
#### 1.1 What is a function
#### 1.2 Combining of functions
#### 1.3 Domain and Range
* Domain is all the possible input values.
* Range is all the possible output values.
#### 1.4 Inverse Functions
* We use $f^{-1}$ to mean inverse.
* Examples:
  * If $f(x)=1-2x$, we write $f=1-2x$
  * And we can write it as a function of x :$f=1-2x$ 
     $x=\displaystyle\frac{1-f}{2}$
  * $f^{-1}(x)=\displaystyle\frac{1-x}{2}$
  * The graph of the functions and its inverse are reflections of each other in the line $y=x$.
* Domain of $f(x)$ is equal to the Range of $f^{-1}$ and vice versa.
* Other important functions and their inverses:
   * $e^x$ and $\ln{x}$
   * $\sin x$ and $sin^{-1} x$
### 2: Exponential and Logarithmic functions
#### 2.1 Exponential function $e^x$ or exp$(x)$ 
##### 2.1.1 The application of $e^x$
* $e^{-x}$-the exponential decay
* $e^{-x^2}$-the normal distribution
* $xe^{-x}$-the Poisson distribution
##### 2.1.2 The hyperbolic cosine and hyperbolic sine
* $\cosh x=\displaystyle\frac{(e^x+e^{-x})}{2}$
* $\sinh x=\displaystyle\frac{(e^x-e^{-x})}{2}$
* Their properties:
   * $(\cosh x)^2-(\sinh x)^2=1$
    $$
    \displaystyle\frac{d}{dx}\cosh x=\sinh x
    $$

    $$
    \displaystyle\frac{d}{dx}\sinh x=\cosh x
    $$
  * $\cosh (ix)= \cos(x)$
  * $\sinh (ix)= i\sin(x)$
### 2.2 Logarithm and powers
## 3: Sine and Cosine functions 
### 3.1 Combination of sine and cosine functions
The combination of the sine and cosine produce more complicated shapes, such as Fourier Series.
## 4: Transformation
### 4.1 Translation and Magnifications
### 4.2 Plotting a quadratic graph
### 4.4 Odd,even and periodic functions
* Even function:$f(-x)=f(-x)$ 
* Odd function:$f(-x)=-f(-x)$
* Periodic function: like $\sin x$
## 5: Curve sketching
### 5.1 Aims and strategy
* Cross or touch the axes.
* Max, min and inflection points
### 5.2 Stationary points- First derivation
Using the first derivation to find the gradient each side.
### 5.3 Stationary points- Secondary derivation
* The inflection points means the $\displaystyle\frac{dy}{dx}\not ={}0$ and $\displaystyle\frac{d^2y}{dx^2}=0$.
* The gradient of the function reach a max or min at the infection points.
* It is useful only if the $\displaystyle\frac{dy}{dx}\not ={0}$
## 6: Asymptotes and Rational Functions
### 6.1 Definitions
* The function that is a quotient of two polynomial functions
* As the denominator of the fraction takes the value zero, the function becomes infinite, we get a vertical line called vertical asymptote. The function may have horizontal , sloping and vertical asymptote.
* Theses lines may cross.
### 6.2 Rewriting the functions by long division
 * This is a way to separate the function to make to curves graphing easier.
 * Examples:
   * $\displaystyle\frac{x^2}{x+1}=\displaystyle\frac{(x-1)(x+1)+1}{x+1}=x-1+\displaystyle\frac{1}{x+1}$
    $\quad$
   * $\displaystyle\frac{x+1}{x-3}=\displaystyle\frac{(x-3)+5}{x-3}=1+\displaystyle\frac{5}{x-3}$

## 7: Curve Sketching Examples

### 7.1: Example 1
  $$
  y=\displaystyle\frac{2x+1}{(x-1)(x+2)}
  $$
  * Finding the roots of the denominator, which is the vertical asymptotes.
  * Finding the monotony of each parts of the function.
  * Finding the infinite of the function.

### 7.2: Example 2
$$
  y=\displaystyle\frac{x^3-2x^2+x-2}{1-x^2}
$$
* Separating the factors as $(x-2)(x^2+1)$.
* Following the example 1 to get the vertical asymptotes and the monopoly.
* Using the long division to separate the constant to find the slope asymptotes:
$$
 y=\displaystyle\frac{(1-x^2)(2-x)}{1-x^2}
$$
i.e.:
$$
y=-x+2+\displaystyle\frac{2x-4}{1-x^2}
$$
As the last part of the term is really small, the slope asymptote is the $y=-x+2$.

### 7.3: Example 3 (modulus function)
* $y=|x+3|+|x-1|$
* The graph can be drawn by apart the functions.


