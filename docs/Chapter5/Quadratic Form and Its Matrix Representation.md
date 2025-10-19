# Quadratic Form and Its Matrix Representation

$$
f(x_1, x_2, \cdots , x_n) = a_{11}x_1^2 + 2a_{12}x_1x_2 + \cdots + 2a_{1n}x_1x_n + \\ a_{22}x_2^2 + \cdots + 2a_{2n}x_2x_n + a_{nn}x_n^2
$$

$f(x_1, x_2, \cdots, x_n)$ is called a quadratic form in n variables over the field P, or simply a quadratic form.

## Definition 1

Let $x_1,x_2,\cdots,x_n$ and $y_1,y_2,\cdots,y_n$ be two sets of variables. A set of relations with coefficients in a field P is called a linear substitution from $x_1,x_2,\cdots,x_n$ to $y_1,y_2,\cdots,y_n$, or simply a linear substitution. 
$$
\left\{ \begin{array}{} 
x_1 = c_{11}y_1 + c_{12}y_2 + \cdots + c_{1n}y_n\\
x_2 = c_{21}y_1 + c_{22}y_2 + \cdots + c_{2n}y_n\\
\cdots \cdots \cdots\\
x_n = c_{n1}y_1 + c_{n2}y_2 + \cdots + c_{nn}y_n
\end{array}		\right.
$$


If the determinant of the coefficient matrix is not equal to zero
$$
\left[ \begin{array}{} 
c_{11} & c_{12} & \cdots & c_{1n}\\
c_{21} & c_{22} & \cdots & c_{2n}\\
\vdots & \vdots & & \vdots\\
c_{n1} & c_{n2} & \cdots & c_{nn}
\end{array}			\right] \neq 0
$$
Then the linear substitution is called non-degenerate.

For a quadratic form, we arrange its coefficient into an $n \times n$ matrix.

Then we get
$$
A = \left[	\begin{array}{} 
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{array}			\right]
$$
$A$ is called the quadratic form matrix, and $a_{ij} = a_{ji}$.

So $A^T = A$, we call such a matrix a symmetric matrix; therefore, the matrix of a quadratic form is always symmetric.

Then we can use the mulpitication of matrices to represent the quadratic form.
$$
f(x_1, x_2, \cdots, x_n) = X^TAX,\ 
X=\begin{bmatrix} 
x_1\\
x_2\\
\vdots\\
x_n
\end{bmatrix}
$$
After a non-degenerate linear substitution, the quadratic form is still a quadratic.

So suppose we have a quadratic form $f(x_1, x_2, \cdots, x_n) = X^TAX$ and a non-degenerate linear substitution $X=CY$.

After the linear substitution, the new quadratic form is $f(y_1,y_2,\cdots,y_n)=Y^TBY$.

Then we have
$$
f(x_1, x_2, \cdots, x_n) = X^TAX = (CY)^TACY = Y^TC^TACY
$$
Clearly, $B = C^TAC$.

## Definition 2

Let A and B be $n \times n$ matrices over a field P. They are called congruent if there exists an invertibale matrix $C$ over the field P such that 
$$
B = C^TAC
$$
The transformation from $A$ to $B$ is called a congruence transformation.

Congruence is a relationship among matrices, it is not difficult to see that it has:

- Reflexivity: $A = E^T A E$
- Symmetry: $B = C^TAC \Rightarrow A=(C^{-1})^TBC^{-1}$
- Transitivity: $A_1 = C_1^TAC_1,\ A_2=C_2^TA_1C_2 \Rightarrow A_2 = (C_1C_2)^TA(C_1C_2)$

Under a non-degenerate linear substitution, the matrix of the new quadratic form is congruent to the matrix of the original quadratic form.



