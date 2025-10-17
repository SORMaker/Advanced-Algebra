# Chapter4-6

Elementary Matrix

## Definition 10

A matrix obtained by performing a single elementary transformation on an identity matrix E is called an elementary matrix.

Obviously, elementary matrices are all square matrices. 

We have three elementary transformations, so there exists three elementary matrices.

- $P(i,j)$: exchange the i-th row and the j-th row.
- $P(i(c))$: use a non-zero number $c$ to multiply the i-th row.
- $P(i,j(k))$: add k times the j-th row to the i-th row.

## Lemma

Performing an elementary row operation on an $s \times n$ Matrix A is equivalent to left-multiplying A by the corresponding $s \times s$ elementary matrix. Similarly, performing an elementary column operation on A is equivalent to right-multiplying A by the corresponding $n \times n$ elementary matrix.

### Proof

We just focus on the case of row operations。

According to the multiplication of block matrices. 

Let $B = (b_{ij})$ be any $s \times s$ matrix, and $A_1, A_2, \cdots, A_s$ are the row vectors of the matrix $A$.

Then we know
$$
BA = \left[ \begin{array}{} 
b_{11}A_1 + b_{12}A_2 + \cdots + b_{1s}A_s \\
b_{21}A_1 + b_{22}A_2 + \cdots + b_{2s}A_s \\
\cdots\cdots\cdots \\
b_{s1}A_1 + b_{s2}A_2 + \cdots + b_{ss}A_s
\end{array}   \right]
$$
In particular, if we set $B = P(i,j), P(i(c)),P(i,j(k))$, respectively, we get:
$$
P(i,j)A = \left[ \begin{array}{}
A_1 \\
\vdots \\
A_j\\
\vdots\\
A_i\\
\vdots\\
A_s
\end{array}    \right],\ 
P(i(c))A = \left[ \begin{array}{}
A_1 \\
\vdots \\
cA_i\\
\vdots\\
A_s
\end{array}    \right],\ 
P(i,j(k))A = \left[ \begin{array}{}
A_1 \\
\vdots \\
A_i + kA_j\\
\vdots\\
A_j\\
\vdots\\
A_s
\end{array}    \right]
$$
The elementary matrices are all invertible, and their invert matrices are still elementary matrices.

In fact,
$$
P(i,j)^{-1}=P(i,j),\quad P(i(c))^{-1} = P(i(c^{-1})),\quad P(i,j(k))^{-1} = P(i,j(-k)).
$$

## Definition 11

Two matrices A and B are called equivalent if one can be obtained from the other by a finite sequence of elementary operations (row or column).

Equivalent is a relationship among matrices, obviouly it has reflexivity, symmetry and transitivity.

## Theorem 5

Any $s \times n$ matrix A is equivalent to
$$
\left[ \begin{array}{} 
1 & 0 & \cdots & 0 & \cdots & 0 \\
0 & 1 & \cdots & 0 & \cdots & 0 \\
\vdots & \vdots & & \vdots & & \vdots\\
0 & 0 & \cdots & 1 & \cdots & 0\\
0 & 0 & \cdots & 0 & \cdots & 0 \\
\vdots & \vdots & & \vdots & & \vdots\\
0 & 0 & \cdots & 0 & \cdots & 0 \\
\end{array}   \right]
$$
It is called the canonical form of matrix A, and the number of pivots is equal to the rank of A (the number of pivots can equal zero).

### Proof

If $A = \mathbf{0}$, then it has already been the canonical form. 

So let's suppose $A \neq \mathbf{0}$.

After elementary transforming, we can definitely get a matrix $A$ which its upper left element is not equal to zero.

When $a_{11} \neq 0$, then we can subtract $a_{11}^{-1}a_{i1}$ times $row_1$ from the other rows, and subtract $a_{11}^{-1}a_{1j}$ times $column_1$ from the other columns.

Then we get:
$$
\left[ \begin{array}{} 
1 & 0 & \cdots & 0\\
0\\
\vdots & & A_1 &\\
0
\end{array}    \right]
$$
$A_1$ is a $(s-1) \times (n-1)$ matrix. 

Then we do the same operations for $A_1$.

Finally, we can get the canonical form.

Obviously, the rank of the canonical form is equal to the number of pivots, and elementary transformations won't change the rank of matrices, so pivots number is also the rank of A.

---

Two matrices A and B are equivalent if and only if there exist elementary matrices $P_1,\cdots,P_l,Q_1,\cdots,Q_t$ such that
$$
A = P_1 P_2 \cdots P_l B Q_1 Q_2 \cdots Q_t
$$

## Theorem 6

N-th order matrix A is invertible if and only if it can be represented a multiplication of a series of elementary matrices.
$$
A = Q_1 Q_2 \cdots Q_m
$$

### Proof

$\Longrightarrow$

$A_{n \times n}$ is invertible $\Rightarrow$ the rank of $A$ is n $\Rightarrow$ $A$ is equivalent to $E_n$ $\Rightarrow$ $A = P_1 P_2 \cdots P_l E Q_1 Q_2 \cdots Q_t = Q_1 Q_2 \cdots Q_m$ 

$\Longleftarrow$

$A = Q_1 Q_2 \cdots Q_m$ $\Rightarrow$ $A = Q_1 \cdots Q_r E_n Q_{r+1} \cdots Q_m$ $\Rightarrow$ $A$ is equivalent to $E_n$ 

$\Rightarrow$ the rank of $A$ is n $\Rightarrow$ $A$ is invertible

## Corollary 1

Two $s \times n$ matrices A and B are equivalent if and only if there exist an invertible $s \times s$ matrix P and an invertible $n \times n$ matrix Q such that
$$
A = PBQ
$$
Let $P_1 P_2 \cdots P_l = P, \ Q_1 Q_2 \cdots Q_t = Q$ , then we can get the corollary.

## Corollary 2

Every invertible matrix is row-equivalent to the identity matrix.

### Proof

According to theorem 6, we have
$$
Q_1^{-1} Q_2^{-1} \cdots Q_m^{-1} A = E
$$
Since the inverse of an elementary matrix is also an elementary matrix, and since left-multiplying a matrix A by an elementary matrix is equivalent to performing an elementary row operation on A.