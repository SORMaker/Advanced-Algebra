# Chapter4-3

Let’s introduce some theorems about the multiplication of matrices.

## Theorem 1

$|AB|=|A||B|$

### Proof

We already proved this theorem in Chapter 2.

## Corollary 1

$|A_1 A_2 \cdots A_m| = |A_1| |A_2| \cdots |A_m|.$

## Definition 6

If $|A_{n \times n}| \neq 0$, then the matrix A is called non-degenerate(or non-singular, invertible).

## Theorem 2

We have two n by n matrices A and B; AB is degenerate if and only if at least one of A or B is degenerate.

### Proof

$\Longleftarrow$

If A is degenerate, then $|A| = 0$. 

So $|AB|=|A||B|=0.$

If B is degenerate, we will get the same result.

So AB is degenerate.

$\Longrightarrow$

If AB is degenerate, then $|AB|=0.$

So $|AB|=|A||B|=0.$

So we get $|A|=0$  or $|B|=0$.

So at least one of A or B is degenerate.

## Theorem 2

Let A be an n by m matrix, and B be an m by s matrix.

So we have $Rank(AB) \leq \min{[Rank(A), Rank(B)]}$

### Proof

We need to prove $Rank(AB) \leq Rank(A)$ and $Rank(AB) \leq Rank(B)$.

$A_{n \times m}B_{m \times s} = C_{n \times s},B=\begin{bmatrix} 
B_1\\
B_2\\
\vdots\\
B_m
\end{bmatrix},C=\begin{bmatrix}
C_1\\
C_2\\
\vdots\\
C_n
 \end{bmatrix}$

So $C_i = \sum_{k=1}^{m}a_{ik}B_k, i=1,2,\cdots,n.$

Which means $C_i$ can be linearly represented by the set of row vectors $\set{B_i}$.

So $R(AB) \leq R(B)$

Similarly, $A=\begin{bmatrix} 
A_1 & A_2 & \cdots & A_m
\end{bmatrix}, C=\begin{bmatrix}
C_1 & C_2 & \cdots & C_s \end{bmatrix}$

So $C_j=\sum^m_{k=1}A_kb_{kj}, j=1,2,\cdots,s.$

So $R(AB) \leq R(A)$

Therefore, $R(AB) \leq \min{[R(A), R(B)]}$

## Corollary

If $A=A_1 A_2 \cdots A_t$, then $R(A) \leq \min_{1 \leq j \leq t}R(A_j)$