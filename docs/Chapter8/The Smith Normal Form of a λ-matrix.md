# The Smith Normal Form of a $\lambda$-matrix

## Def.3

There are three elementary transformations of the $\lambda$-matrix.

1. $P(i,j)$: exchange the $row_i$ and the $row_j$.
2. $P(i(c))$: use a non-zero number $c$ to multiply the $row_i$.
3. $P(i,j(\varphi))$: add $\varphi(\lambda)$ times the $row_j$ to the $row_i$.

## Def.4

A $\lambda$ matrix $A(\lambda)$ is said to be equivalent to $B(\lambda)$. If $B(\lambda)$ can be obtained from $A(\lambda)$ through a series of elementary transformations.

Equivalence is a relationship between $\lambda$-matrices. This relationship obviously possesses the following three properties:

1. Reflexivity: Every $\lambda$-matrix is equivalent to itself.
2. Symmetry: If $A(\lambda)$ is equivalent to $B(\lambda)$, then $B(\lambda)$ is equivalent to $A(\lambda)$.
3. Transitivity: If $A(\lambda)$ is equivalent to $B(\lambda)$ and $B(\lambda)$ is equivalent to $C(\lambda)$, then $A(\lambda)$ is equivalent to $C(\lambda)$.

So $A(\lambda)$ is equivalent to $B(\lambda)$ if and only if there exists a series of elementary matrices $P_1, P_2, \cdots, P_l,Q_1,Q_2,\cdots,Q_t$, such that
$$
A(\lambda) = P_1P_2\cdots P_lB(\lambda)Q_1Q_2\cdots Q_t.
$$

## Lemma

Let $A(\lambda)$ be a $\lambda$-matrix with a non-zero top-left element $a_{11}(\lambda)$. If $A(\lambda)$ contains an element that is not divisible by $a_{11}(\lambda)$, then there exists an equivalent matrix $B(\lambda)$ whose top-left entry has a degree strictly less than that of $a_{11}(\lambda)$.

### Pf.

We proceed by distinguishing three cases based on the position of the element in $A(\lambda)$ that is not divisible by $a_{11}(\lambda)$.

Case 1:

Suppose the first column of $A(\lambda)$ contains an element $a_{i1}(\lambda)$ that is not divisible by $a_{11}(\lambda)$.

By the division algorithm, we have:
$$
a_{i1}(\lambda) = a_{11}(\lambda)q(\lambda) + r(\lambda).
$$
where $r(\lambda) \neq 0$ and $\text{deg}(r) < \text{deg}(a_{11})$.

So, we subtract $q(\lambda)$ times the first row from the $row_i$ 
$$
A(\lambda) = \begin{pmatrix} a_{11}(\lambda) & \cdots \\ \vdots & \vdots \\ a_{i1}(\lambda) & \cdots \\ \vdots & \vdots \end{pmatrix} \longrightarrow \begin{pmatrix} a_{11}(\lambda) & \cdots \\ \vdots & \vdots \\ r(\lambda) & \cdots \\ \vdots & \vdots \end{pmatrix}
$$
Then, we interchange the first row and the $i$-th row:
$$
A(\lambda) \longrightarrow \begin{pmatrix} r(\lambda) & \cdots \\ \vdots & \vdots \\ a_{11}(\lambda) & \cdots \\ \vdots & \vdots \end{pmatrix} = B(\lambda)
$$
The top-left element of $B(\lambda)$ is $r(\lambda)$, which satisfies the condition of the lemma.

Case 2:

Suppose the first row of $A(\lambda)$ contains an element $a_{1j}(\lambda)$ that is not divisible by $a_{11}(\lambda)$.

The case is similar to case 1.

Case 3:

Suppose every element in the first row and first column is divisible by $a_{11}(\lambda)$, but there exists another element $a_{ij}(\lambda)$ that is not divisible by $a_{11}(\lambda)$.

Let $a_{i1}(\lambda) = a_{11}(\lambda)\varphi(\lambda)$.

We perform the following elementary operations on $A(\lambda)$:

1. Subtract $\varphi(\lambda)$ times $\text{row}_1$ from $\text{row}_i$, this makes the $(i,1)$ entry zero.
2. Add $\text{row}_i$ to $\text{row}_1$.

Let the resulting matrix be $A_1(\lambda)$.

In the first row of $A_1(\lambda)$, there is an element:
$$
a_{ij}(\lambda) + (1 - \varphi(\lambda))a_{1j}(\lambda)
$$
This element is not divisible by the top-left element $a_{11}(\lambda)$.

This is the same as case 2.

## Th.2

Every non-zero $s \times n$ $\lambda$-matrix $A(\lambda)$ is equivalent to a matrix of the following form:
$$
\begin{pmatrix}
d_1(\lambda) & & & & & \\
& d_2(\lambda) & & & & \\
& & \ddots & & & \\
& & & d_r(\lambda) & & \\
& & & & 0 & \\
& & & & & \ddots \\
& & & & & & 0
\end{pmatrix}
$$
where $r \geq 1$, and $d_i(\lambda)(i = 1,2,\cdots,r)$ are monic polynomials, such that:
$$
d_i(\lambda) | d_{i+1}(\lambda), i = 1,2,\cdots,r-1.
$$

### Pf.

By interchanging rows and columns, we can ensure that the top-left element of $A(\lambda)$, denoted as $a_{11}(\lambda)$, is non-zero. If $a_{11}(\lambda)$ does not divide every element of $A(\lambda)$, then by the Lemma, we can find a matrix $B_1(\lambda)$ equivalent to $A(\lambda)$ whose top-left element $b_1(\lambda) \neq 0$ has a degree less than that of $a_{11}(\lambda)$.

If $b_1(\lambda)$ still does not divide every element of $B_1(\lambda)$, applying the Lemma again, we can find a matrix $B_2(\lambda)$ equivalent to $B_1(\lambda)$ with a non-zero top-left element $b_2(\lambda)$ of even lower degree. Continuing this process produces a sequence of equivalent $\lambda$-matrices $A(\lambda), B_1(\lambda), B_2(\lambda), \dots$ with top-left element of strictly decreasing degrees. Since the degree of a polynomial is a non-negative integer, this sequence cannot decrease indefinitely. Therefore, after a finite number of steps, we must terminate at a $\lambda$-matrix $B_s(\lambda)$ whose top-left element $b_s(\lambda) \neq 0$ divides every element $b_{ij}(\lambda)$ of $B_s(\lambda)$, that is:
$$
b_{ij}(\lambda) = b_s(\lambda)q_{ij}(\lambda)
$$
We perform elementary operations on $B_s(\lambda)$:
$$
B_s(\lambda) = \begin{pmatrix} b_s(\lambda) & \cdots & b_{ij}(\lambda) & \cdots \\ \vdots & & \vdots & \\ b_{i1}(\lambda) & \cdots & \cdots & \cdots \\ \vdots & & \vdots & \end{pmatrix} \longrightarrow \begin{pmatrix} b_s(\lambda) & 0 & \cdots & 0 \\ 0 & & & \\ \vdots & & A_1(\lambda) & \\ 0 & & & \end{pmatrix}
$$
In the resulting submatrix $A_1(\lambda)$ at the bottom right, every element is divisible by $b_s(\lambda)$, because all entries in $A_1(\lambda)$ are linear combinations of the elements of $B_s(\lambda)$.

If $A_1(\lambda) \neq O$, we can repeat the above procedure for $A_1(\lambda)$, reducing the matrix to the form:
$$
\begin{pmatrix} d_1(\lambda) & 0 & \cdots & 0 \\ 0 & d_2(\lambda) & \cdots & 0 \\ 0 & 0 & & \\ \vdots & \vdots & A_2(\lambda) & \\ 0 & 0 & & \end{pmatrix}
$$
Here, $d_1(\lambda)$ and $d_2(\lambda)$ are both monic polynomials (note that $d_1(\lambda)$ differs from $b_s(\lambda)$ only by a constant factor), and $d_1(\lambda) \mid d_2(\lambda)$, since $d_1(\lambda)$ divides every element of $A_2(\lambda)$.

By continuing this process, $A(\lambda)$ is eventually reduced to the required form. The final matrix obtained is called the Smith Normal Form (or simply the Normal Form) of $A(\lambda)$.