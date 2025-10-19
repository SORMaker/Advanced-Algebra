# Positive Definite Quadratic Form

## Definition 4

A real quadratic form $f(x_1, x_2, \cdots, x_n)$ is called positive definite if for any set of real numbers $c_1, c_2, \cdots, c_n$ are not all zero, then we have $f(c_1, \cdots, c_n) > 0$.

- Real quadratic form $f(x_1, \cdots, x_n) = d_1x_1^2 + d_2x_2^2 + \cdots + d_nx_n^2$ is positive definite $\Longleftrightarrow$ $d_i > 0$.
- $f(x_1, x_2, \cdots, x_n)$ is positive definite, then after a non-degenerate linear substitution $X=CY$, we get $g(y_1, \cdots, y_n)$, and it is also positive definite.

## Theorem 6

An n-ary real quadratic form $f(x_1, x_2, \cdots, x_n)$ is positive definite if and only if its positive index of inertia equals $n$.

### Proof

After a non-degenerate real linear substitution, $f(x_1, \cdots, x_n)$ are transformed into $d_1y_1^2 + d_2y_2^2 + \cdots + d_ny_n^2$.

Then we have
$f(x_1, \cdots, x_n)$ is positive definite $\Longleftrightarrow$ $d_1y_1^2 + d_2y_2^2 + \cdots + d_ny_n^2$ is positive definite $\Longleftrightarrow$ $d_i > 0(i = 1,2,\cdots,n)$ $\Longleftrightarrow$ The positive index of inertia is $n$.

Theorem 6 tells us that the canonical form of the positive definite quadratic form is $y_1^2 + y_2^2 + \cdots + y_n^2$.

## Definition 5

A real symmetric matrix $A$ is called positive definite if the quadratic form $X^TAX$ is positive definite. 

A real symmetric matrix is positive definite if and only if it is congruent to the identity matrix.

## Corollary

The determinant of the symmetric matrix is greater than zero.

### Proof

Let A be a symmetric matrix.

A is congruent to the identity matrix. We have the invertible matrix $C$.

Then we have 
$$
A = C^TEC = C^TC
$$
Taking the determinant of both sides, we have
$$
|A| = |C^T||C| = |C|^2 > 0
$$

## Definition 6

The minor $H_i$
$$
H_i = \left| \begin{array}{} 
a_{11} & a_{12} & \cdots & a_{1i}\\
a_{21} & a_{22} & \cdots & a_{2i}\\
\vdots & \vdots & & \vdots\\
a_{i1} & a_{i2} & \cdots & a_{ii}
\end{array} \right|, \quad i=1,2,\cdots,n
$$
is called the leading principle minor of the matrix A.

## Theorem 7

A real quadratic form 
$$
f(x_1,\cdots,x_n)=\sum^n_{i=1}\sum_{j=1}^na_{ij}x_ix_j=X^TAX
$$
is positive definite if and only if all the leading principal minors of the matrix A are positive.

### Proof

$\Longrightarrow$

Let $f(x_1,\cdots,x_n)$ are positive definite.

Then for any $k(1 \leq k \leq n)$, we have 
$$
f_k(x_1,\cdots,x_k)=\sum^k_{i=1}\sum_{j=1}^ka_{ij}x_ix_j
$$
For any set of non-zero real numbers $(c_1, c_2, \cdots, c_k)$, we have 
$$
f_k(c_1, c_2, \cdots, c_k)=\sum^k_{i=1}\sum_{j=1}^ka_{ij}c_ic_j=f(c_1,c_2,\cdots,c_k,0,\cdots,0) > 0
$$
Therefore, $f_k(x_1, \cdots, x_k)$ is positive definite.

Hence, the determinant of the matrix of $f_k$
$$
\left|\begin{array}{} 
a_{11} & \cdots & a_{1k}\\
\vdots & & \vdots\\
a_{k1} & \cdots & a_{kk}
\end{array}    \right| > 0, \quad k=1,\cdots,n.
$$
This means all the leading principal minors of the matrix A are positive.

$\Longleftarrow$

We proceed by induction on the number of variables, n.

When $n=1$, $f(x_1) = a_{11}x_1^2$.

Obviously, $f(x_1)$ is positive definite.

Assume the conclusion holds for quadratic forms in $n-1$ variables; 

We now prove that it also holds for quadratic forms in $n$ variables.

 Let 
$$
A_1 = \begin{bmatrix} 
a_{11} & \cdots & a_{1,n-1}\\
\vdots & & \vdots\\
a_{n-1,1} & \cdots & a_{n-1,n-1}
\end{bmatrix}, \quad \alpha=\begin{bmatrix} a_{1n}\\ \vdots\\ a_{n-1,n} \end{bmatrix}
$$
Then we can express the matrix $A$ in block matrix form.
$$
A = \begin{bmatrix}
A_1 & \alpha\\
\alpha^T & a_{nn}
\end{bmatrix}
$$
Since all the leading principal minors of the matrix $A$ are positive, the leading principal minors of $A_1$ are also positive. 

So $A_1$ is a positive definite matrix.

In other words, there exists an $n-1$ by $n-1$ invertible matrix G, such that
$$
G^TA_1G = E_{n-1}
$$
So, let 
$$
C_1 = 
\begin{bmatrix}
G & 0\\
0 & 1 
\end{bmatrix}
$$
Then we have
$$
C_1^TAC_1 = 
\begin{bmatrix}
G^T & 0\\
0 & 1 
\end{bmatrix}
\begin{bmatrix}
A_1 & \alpha\\
\alpha^T & a_{nn}
\end{bmatrix}
\begin{bmatrix}
G & 0\\
0 & 1 
\end{bmatrix}=
\begin{bmatrix}
E_{n-1} & G^T\alpha\\
\alpha^TG & a_{nn} 
\end{bmatrix}
$$
Let
$$
C_2=
\begin{bmatrix}
E_{n-1} & -G^T\alpha\\
0 & 1 
\end{bmatrix}
$$
Then we have
$$
C_2^TC_1^TAC_1C_2 = 
\begin{bmatrix}
E_{n-1} & 0\\
-G^T\alpha & 1 
\end{bmatrix}
\begin{bmatrix}
E_{n-1} & G^T\alpha\\
\alpha^TG & a_{nn} 
\end{bmatrix}
\begin{bmatrix}
E_{n-1} & -G^T\alpha\\
0 & 1 
\end{bmatrix}
=
\begin{bmatrix}
E_{n-1} & 0\alpha\\
0 & a_{nn}-\alpha^TGG^T\alpha 
\end{bmatrix}.
$$
Let $C=C_1C_2, \quad a_{nn}^{\prime} = a_{nn}-\alpha^TGG^T$.

We have
$$
C^TAC = \begin{bmatrix} 
1 & & &\\
& \ddots & &\\
& & 1 &\\
& & & a_{nn}^{\prime}
\end{bmatrix}.
$$
Taking the determinant both sides, we get
$$
|C|^2|A| = a_{nn}^{\prime}.
$$
Because $|A| > 0$, $a > 0$.

Therefore,
$$
C^TAC = \begin{bmatrix} 
1 & & &\\
& \ddots & &\\
& & 1 &\\
& & & a_{nn}^{\prime}
\end{bmatrix} = 
\begin{bmatrix} 
1 & & &\\
& \ddots & &\\
& & 1 &\\
& & & \sqrt{a_{nn}^{\prime}}
\end{bmatrix}
\begin{bmatrix} 
1 & & &\\
& \ddots & &\\
& & 1 &\\
& & & 1
\end{bmatrix}
\begin{bmatrix} 
1 & & &\\
& \ddots & &\\
& & 1 &\\
& & & \sqrt{a_{nn}^{\prime}}
\end{bmatrix}
$$
So the matrix $A$ is congruent to the identity matrix.

Hence the matrix $A$ is positive definite.

In other words, the quadratic form $f$ is positive definite.

## Definition 7

Lef $f(x_1,\cdots,x_n)$ be a real quadratic form.

- If $f(x_1, \cdots, x_n) < 0$ for all non-zero vectors $x$, then $f(x_1, \cdots, x_n)$ is called negative definite. 
- If $f(x_1, \cdots, x_n) \geq 0$ for all non-zero vectors $x$, then $f(x_1, \cdots, x_n)$ is called positive semi-definite. 
- If $f(x_1, \cdots, x_n) \leq 0$ for all non-zero vectors $x$, then $f(x_1, \cdots, x_n)$ is called negative semi-definite. 
- If $f(x_1, \cdots, x_n)$ is neither positive semi-positive definite nor semi-negative definite, then $f(x_1, \cdots, x_n)$ is called indefinite. 

$f(x_1, \cdots, x_n)$ is negative definite $\Longleftrightarrow$ $-f(x_1, \cdots, x_n)$ is positive definite 

$f(x_1, \cdots, x_n)$ is negative semi-definite $\Longleftrightarrow$ $-f(x_1, \cdots, x_n)$ is positive simi-definite 

## Theorem 8

For a real quadratic form $f(x_1,\cdots,x_n)=X^TAX$, where $A$ is a symmetric matrix, the following conditions are equivalent:

- $f(x_1,\cdots,x_n)$ is positive semi-definite.

- Its positive index of inertia is equal to its rank.

- There exists a real invertible matrix $C$ such that 
  $$
  C^TAC=\begin{bmatrix}
  d_1 & & &\\ 
  & d_2 & &\\
  & & \ddots &\\
  & & & d_n
  \end{bmatrix}, \quad d_i \geq 0(i=1,2,\cdots,n)
  $$

- There exists a real matrix $C$, such that $A=C^TC$
- All principal minors of $A$ are greater than or equal to zero.

### Proof

Part1: 1 $\Longrightarrow$ 3 $\Longrightarrow$ 2 $\Longrightarrow$ 1

1 $\Longrightarrow$ 3

$f(x_1, \cdots, x_n) \geq 0$ $\Longrightarrow$ $d_1y_1^2 + d_2y_2^2 + \cdots + d_ny_n^2 \geq 0$.

If there exists $d_j < 0$, then we can take $y_j = 1$, other $y_i = 0$.

Then $d_1y_1^2 + d_2y_2^2 + \cdots + d_ny_n^2 < 0$, there is a contradiction.

So $d_i \geq 0(i = 1,2,\cdots,n)$.

So there exists $C^TAC=\begin{bmatrix}
d_1 & & &\\ 
& d_2 & &\\
& & \ddots &\\
& & & d_n
\end{bmatrix}$.

3 $\Longrightarrow$ 2

There exists $D = C^TAC = diag(d_1,d_2,\cdots,d_n)$.

Therefore, D is congruent to A. 

So they have the same rank, a positive index of inertia, and a negative index of inertia.

Because $d_i \geq 0$, so $q = r - p = 0$ $\Longrightarrow$ $r = p$.

Its positive index of inertia is equal to its rank.

2 $\Longrightarrow$ 1

$r = p$ $\Longrightarrow$ $q = r-p = 0$.

So

 $f(x_1, x_2, \cdots, x_n) \Longrightarrow$

$z_1^2 + z_2^2 + \cdots + z_p^2 - z_{p+1}^2 - \cdots - z_r^2 = z_1^2 + \cdots + z_r^2$

Then we know $f(x_i)$ is positive semi-definite.

Part2: 1 $\Longleftrightarrow$ 4

Part3: 1 $\Longleftrightarrow$ 5