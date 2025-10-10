# Chapter4-4

Now, let’s move to the inverse of matrices.

## Definition 7,8

If A and B are n by n matrices such that AB=BA=E(the identity matrix of order n), then we say that A is invertible and B is the inverse of A, written as $B = A^{-1}$.

## Definition 9

Let $A_{ij}$ be the cofactor of the element $a_{ij}$ in matrix A.

Then the matrix $A^*$ is called the adjugate matrix of A.

$$
A^*=\left. \begin{bmatrix} 
A_{11} & A_{21} & \cdots & A_{n1}\\
A_{12} & A_{22} & \cdots & A_{n2}\\
\vdots & \vdots & & \vdots \\
A_{1n} & A_{2n} & \cdots & A_{nn}
\end{bmatrix} \right.
$$

## Theorem 3

The matrix A is invertible if and only if A is non-degenerate, and $A^{-1}=\frac{1}{d}A^*(d = |A| \neq 0).$

### Proof

$$
A A^* =A^* A =\left[ \begin{array}{}
d & 0 & \cdots & 0\\
0 & d & \cdots & 0\\
\vdots & \vdots & & \vdots\\
0 & 0 & \cdots & d
 \end{array} \right] = dE,d = |A|.(1)
 $$

$\Longrightarrow$

If A is invertible, so $|AA^{-1}| = |E| = 1$. So $|A| \neq 0.$

$\Longleftarrow$

If $|A| \neq 0$, according to $(1)$, we know $A(\frac{1}{d}A^*) = (\frac{1}{d}A^*)A = E$. So A is invertible and $A^{-1} = \frac{1}{d}A^*$

## Corollary

If A and B are invertible, then $A^T$ and $AB$ are also invertible. And $(A^T)^{-1}=(A^{-1})^T,(AB)^{-1}=B^{-1}A^{-1}.$

### Proof

Because A and B are invertible, so $|A| \neq 0 , |B| \neq 0.$

So $|A^T| = |A| \neq 0, |AB| = |A||B| \neq 0.$

So $A^T$  and $AB$ are also invertible.

A is invertible, so $AA^{-1} = A^{-1}A = E$

Taking the transpose of both sides, we get:

$(A^{-1})^TA^T = A^T(A^{-1})^T = E$

So $(A^T)^{-1} = (A^{-1})^T.$

$(AB)(B^{-1}A^{-1}) = (B^{-1}A^{-1})(AB) = E$

So $(AB)^{-1} = B^{-1}A^{-1}.$

## Theorem 4

Let A be an $s \times n$ matrix. If P is an $s \times s$ invertible matrix and Q is an $n \times n$ invertible matrix, then rank(A) = rank(PA) = rank(AQ).

### Proof

Let B = PA, according to Theorem 2, we know $rank(B) \leq rank(A)$.

But we also have $A = P^{-1}B$, so $rank(A) \leq rank(B)$.

So $rank(A) = rank(B) = rank(AB).$