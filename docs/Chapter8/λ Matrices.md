# λ Matrices

## Def.

A lambda matrix is a matrix whose elements are polynomials in the variable $\lambda$.

## Def.1

If the $\lambda$ matrix $A(\lambda)$ has an r-th order minor that is not equal to zero, and any other $r+1$ minors are all zero, then the rank of $A(\lambda)$ is $r$.

## Def.2

If we have $A(\lambda)B(\lambda) = B(\lambda)A(\lambda) = E$.

Then we say that $A(\lambda)$ is invertible, $B(\lambda)$ is the inverse matrix of $A(\lambda)$, denoted as $A^{-1}(\lambda)$.

## Th.1

The $n \times n$ $\lambda$ matrix $A(\lambda)$ is invertible if and only if the determinant of $A(\lambda)$ is a non-zero number.

### Pf.

$\Longleftarrow$

Suppose $d = |A(\lambda)|$ is a non-zero number. $A^*(\lambda)$ is the adjugate matrix of $A(\lambda)$, it is also a $\lambda$ matrix.

So we have
$$
A(\lambda)\frac{1}{d}A^*(\lambda) = \frac{1}{d}A^*(\lambda)A(\lambda) = E.
$$
So, $A(\lambda)$ is invertible.

$\Longrightarrow$

If $A(\lambda)$ is invertible, then we have $A(\lambda)B(\lambda) = E$.

So, we take the determinant on the both sides.
$$
|A(\lambda)||B(\lambda)| = |E| = 1
$$
Since $|A(\lambda)|$,$|B(\lambda)|$ are all the polynomials of $\lambda$, and the product of them is 1.

So they are all non-zero numbers.





