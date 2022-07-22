# I: Matrix and Vector 
## 1: Matrix 
### 1.1: Definition and Notation 
* A method of recording hundreds of equations in engineering.<font color=#87CEEB> (eg. infinite elements with 3D nodes)</font> 
* A matrix is called "lines by column", eg. 2x3 means 2 lines and 3 columns.
* Capital letter 'A' for a matrix and lower case '$a_{ij}$' for the element of 'A', 'i' is the line and 'j' is the column.
* $A=\begin{pmatrix}1&1\\1&1\end{pmatrix}$ which is a 2x2 matrix.

### 1.2: Special Matrix 

#### (1): Diagonal Matrix
All elements are '0' except the '\' diagonal, but the diagonal can be '0'.
e.g, $\begin{pmatrix}2&0&0\\0&3&0\\0&0&4\end{pmatrix}$

#### (2): Symmetric matrix 
$\begin{pmatrix}1&3&-7\\3&0&2\\-7&2&-5\end{pmatrix}$, $a_{ij}=a_{ji}$

#### (3): Antisymmetric matrix
$\begin{pmatrix}1&-3&7\\3&0&2\\-7&2&-5\end{pmatrix}$ , $a_{ij}=-a_{ji}$, $i\not ={j}$
    
#### (4): Upper/Lower triangular matrix 
 Upper refer to $i>j$, $a_{ij}=0$
 eg:
  $$

  \begin{pmatrix}
  a&b&c\\
  0&d&e\\
  0&0&f
  \end{pmatrix}

  $$ 
    - Lower refer to $i<j$, $a_{ij}=0$
      - eg:
        $$
        \begin{pmatrix}
        a&0&0\\
        b&c&0\\
        d&e&f
        \end{pmatrix}
        $$  

- $\textcircled{5}$ Matrix Transpose
  - (1): Transpose means <font color=#87CEEB> swap </font>
    - eg:
    $$  
    \begin{pmatrix}a&b&c\\d&e&f\\g&h&i\end{pmatrix}^T=\begin{pmatrix}a&d&g\\b&e&h\\c&f&i\end{pmatrix}
    $$
  - (2): $[A^T]^T$
### 1.2: Matrices Algebra 
- $\textcircled{1}$: Scalar multiply 
  - (1): Do the calculation directly
  - (2): Only same-size matrix can do
- $\textcircled{2}$: Matrix Multiplication 
  - eg:
  $$
  A=\begin{pmatrix}m&p\\n&q\end{pmatrix},\quad B=\begin{pmatrix}a&c\\b&d\end{pmatrix}
  $$
  $$
  AB=\begin{pmatrix}am+bp&cm+dp\\an+bq&cn+dq\end{pmatrix}
  $$
  - Notes that $A.B\not ={B.A}$ (mostly)
- $\textcircled{3}$ Identity Matrix 
  - eg:
  $$
  \begin{pmatrix}1&2\\0&1\end{pmatrix}
  $$
  - The 'I' could be 'N x N' matrix
  - $I.A=A=A.I$, whilst I is different 
- $\textcircled{4}$ The properties & rules of matrices 
  - (1): Equality 
    - All the elements are same, $a_{ij}=b_{ij}$ means '='.
  - (2): Properties of Transpose 
    - $(A+B)^T=A^T+B^T$
    - $(A^T)^T=A$
### 1.3: Simultaneous equations & Matrices
- $\textcircled{1}$ Transfer the Matrix and Simultaneous equations 
  - eg: 
    - Original equations:
    $$
    \begin{aligned}
    2x-3y=4 \\
    -x+2y=1
    \end{aligned}
    $$

# IV Functions and Curves
## 1: Functions- general ideas
### 1.1 What is a function
### 1.2 Combining of functions
### 1.3 Domain and Range
* Domain is all the possible input values.
* Range is all the possible output values.
### 1.4 Inverse Functions
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
## 2: Exponential and Logarithmic functions
### 2.1 Exponential function $e^x$ or exp$(x)$ 
#### 2.1.1 The application of $e^x$
* $e^{-x}$-the exponential decay
* $e^{-x^2}$-the normal distribution
* $xe^{-x}$-the Poisson distribution
#### 2.1.2 The hyperbolic cosine and hyperbolic sine
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


