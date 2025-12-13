# Invariant Factors

## Def.5

Let $A(\lambda)$ be a $\lambda$-matrix of rank $r$. For any positive integer $k(1 \leq k \leq r)$, there exist non-zero minors of order $k$ in $A(\lambda)$. The monic greatest common divisor of all $k$-th order minors of $A(\lambda)$ is denoted by $D_k(\lambda)$ and is called the $k$-th determinantal divisor of $A(\lambda)$.

## Th.3

Equivalent $\lambda$-matrices have the same rank and the same determinantal divisor $D_k(\lambda)$.

### Pf.

It suffices to demonstrate that the rank and the determinant divisors of a $\lambda$-matrix remain invariant under a single elementary row operation.

Let $A(\lambda)$ be obtained from $B(\lambda)$ via one elementary row operation. Let $f(\lambda)$ and $g(\lambda)$ denote the $k$-th determinant divisors of $A(\lambda)$ and $B(\lambda)$, respectively. We aim to prove that $f(\lambda) = g(\lambda)$. We consider the three types of elementary row operations.

First, interchanging two rows:

If $A(\lambda)$ is obtained from $B(\lambda)$ by swapping two rows, every $k \times k$ minor of $B(\lambda)$ is either equal to the corresponding minor in $A(\lambda)$ or differs only by a sign. 

Consequently, $f(\lambda)$ remains a common divisor of all $k \times k$ minors of $B(\lambda)$. Thus, $f(\lambda)$ divides $g(\lambda)$, denoted as $f(\lambda)|g(\lambda)$.

Second, multiplying a row by a non-zero constant:

If $A(\lambda)$ is obtained from $B(\lambda)$ by multiplying a row by a non-zero constant $c$, every $k \times k$ minor of $B(\lambda)$ is either equal to the corresponding minor in $A(\lambda)$ or is $c$ times that minor.

Therefore, $f(\lambda)$ is still a common divisor of the minors of $B(\lambda)$, implying $f(\lambda) \mid g(\lambda)$.

Third, adding a multiple of one row to another:

Suppose $B(\lambda)$ is obtained by adding $\varphi(\lambda)$ times row $j$ to row $i$.

- Minors involving both row $i$ and row $j$, as well as those involving neither, remain identical to the corresponding minors in $A(\lambda)$.
- For minors containing row $i$ but not row $j$, we can use the linearity property of determinants to expand them. Such a minor in $B(\lambda)$ equals the sum of the corresponding minor in $A(\lambda)$ and $\pm \varphi(\lambda)$ times another $k \times k$ minor of $A(\lambda)$. In other words, it is a linear combination of two minors from $A(\lambda)$.
- Since $f(\lambda)$ divides every $k \times k$ minor of $A(\lambda)$, it must divide these linear combinations. Therefore, $f(\lambda)$ is a common divisor of the minors of $B(\lambda)$, so $f(\lambda) \mid g(\lambda)$.

The argument for elementary column operations is analogous.

In summary, if $A(\lambda)$ is obtained from $B(\lambda)$ by an elementary operation, then $f(\lambda) \mid g(\lambda)$. However, since elementary matrices are invertible, $B(\lambda)$ can be transformed back into $A(\lambda)$ via an elementary operation. Following the logic above, we must also have $g(\lambda) \mid f(\lambda)$. Since $f(\lambda)$ and $g(\lambda)$ are both monic polynomials, it follows that $f(\lambda) = g(\lambda)$.

Furthermore, if all $k$-th order minors of $A(\lambda)$ are zero, then all $k$-th order minors of $B(\lambda)$ must also be zero, and vice versa. Therefore, $A(\lambda)$ and $B(\lambda)$ share not only the same determinantal divisors but also the same rank.

## Th.4

The standard form of $\lambda$-matrix is unique.

### Pf.

Let $D(\lambda) = \text{diag}(d_1(\lambda), d_2(\lambda), \cdots, d_k(\lambda), 0, \cdots, 0)$ is the standard form of $\lambda$-matrix. $A(\lambda)$ is equivalent to $D(\lambda)$, they have the same rank and the same determinantal divisors.

Therefore, the rank of $A(\lambda)$ is the number of non-zero elements of the standard form on the main diagonal.

The k-th determinantal divisors of $A(\lambda)$ are 
$$
D_k(\lambda) = d_1(\lambda)d_2(\lambda)\cdots d_k(\lambda), k=1,2,\cdots,r. \tag{1}
$$
So, we know
$$
d_1(\lambda) = D_1(\lambda), d_2(\lambda) = \frac{D_2(\lambda)}{D_1(\lambda)}, \cdots, d_r(\lambda) = \frac{D_r(\lambda)}{D_{r - 1}(\lambda)}. \tag{2}
$$
This implies that the non-zero elements on the main diagonal of the Smith normal form of $A(\lambda)$ are uniquely determined by the determinantal divisors of $A(\lambda)$.

Consequently, the Smith normal form of $A(\lambda)$ is unique.

## Def.6

The non-zero elements $d_1(\lambda), d_2(\lambda), \cdots, d_r(\lambda)$ on the main diagonal of the Smith normal form are called the invariant factors of the $\lambda$-matrix $A(\lambda)$.

## Th.5

Two $\lambda$-matrices are equivalent if and only if they have the same determinantal divisors, or equivalently, the same invariant factors.

### Pf.

Equations $(1)$ and $(2)$ establish the relationship between the determinantal divisors and the invariant factors of a $\lambda$-matrix. 

This relationship indicates that determinantal divisors and invariant factors are mutually determined.

Therefore, the condition that two matrices possess identical determinantal divisors of all orders is equivalent to the condition that they possess identical invariant factors of all orders.

The necessity has already been proven in Theorem 3.

The sufficiency is evident. Indeed, if $\lambda$-matrices $A(\lambda)$ and $B(\lambda)$ share the same invariant factors, then both are equivalent to the same Smith normal form.

Consequently, $A(\lambda)$ is equivalent to $B(\lambda)$.

## Th.6

$A(\lambda)$ is invertible if and only if it can be expressed as a product of elementary matrices.

## Co.

Two $s \times n$ $\lambda$-matrices $A(\lambda)$ and $B(\lambda)$ are equivalent if and only if there exist an $s \times s$ invertible matrix $P(\lambda)$ and an $n \times n$ invertible matrix $Q(\lambda)$ such that:
$$
B(\lambda) = P(\lambda)A(\lambda)Q(\lambda)
$$
