# Theoretical Derivation of the Jordan Normal Form

## Th.10

Each $n \times n$ complex matrix $A$ is similar to a Jordan matrix. This Jordan matrix is uniquely determined by matrix $A$, up to the ordering of the Jordan blocks. It is referred to as the Jordan Normal form of  $A$.

### Pf.

Let the elementary divisors of the matrix $A$ of order $n$ be 
$$
(\lambda - \lambda_1)^{k_1}, (\lambda - \lambda_2)^{k_2}, \cdots, (\lambda - \lambda_s)^{k_s}, \tag1
$$
where $\lambda_1, \lambda_2, \cdots, \lambda_s$ are not necessarily distinct, and the exponents $k_1, k_2, \cdots, k_s$ may also coincide.

Each elementary divisor $(\lambda - \lambda)^{k_i}$ corresponds to a Jordan block:
$$
\boldsymbol{J}_i = \begin{pmatrix} \lambda_i & 0 & \cdots & 0 & 0 \\ 1 & \lambda_i & \cdots & 0 & 0 \\ 0 & 1 & \cdots & 0 & 0 \\ \vdots & \vdots & & \vdots & \vdots \\ 0 & 0 & \cdots & 1 & \lambda_i \end{pmatrix}_{k_i \times k_i}, \quad i=1, 2, \cdots, s,
$$
These Jordan blocks constitute a matrix in Jordan form:
$$
\boldsymbol{J} = \begin{pmatrix} \boldsymbol{J}_1 & & & \\ & \boldsymbol{J}_2 & & \\ & & \ddots & \\ & & & \boldsymbol{J}_s \end{pmatrix}.
$$
Based on the construction above, the elementary divisors of $\boldsymbol{J}$ are also given by (1). 

Since $\boldsymbol{J}$ and $A$ share the same elementary divisors, they are similar.

If another matrix in Jordan form, $J'$, is similar to $A$, then $J'$ and $A$ must possess the same elementary divisors. 

Consequently, $J'$ and $J$ are identical except for the permutation of their Jordan blocks.

This establishes the uniqueness.

## Th.11

Let $\mathscr{A}$ be a linear transformation on an $n$-dimensional linear space $V$ over $\mathbb{C}$. There necessarily exists a basis in $V$ under which the matrix of $\mathscr{A}$ is in Jordan canonical form, unique up to the order of Jordan blocks. This is the linear transformation analogue of Theorem 10.

## Th.12

A complex matrix $\boldsymbol{A}$ is similar to a diagonal matrix if and only if all its elementary divisors are of degree 1. The Jordan blocks of a diagonal matrix are all of order 1.

## Th.13

A complex matrix $\boldsymbol{A}$ is similar to a diagonal matrix if and only if its invariant factors have no repeated roots (i.e., are square-free). The last invariant factor is equal to the product of the highest degree elementary divisors, which is also the minimal polynomial of $\boldsymbol{A}$.

**Others:**

- Calculating the transition matrix from a complex matrix $\boldsymbol{A}$ to its Jordan canonical form remains computationally difficult.
- The conclusions above remain unchanged if the Jordan blocks are defined as upper triangular matrices.