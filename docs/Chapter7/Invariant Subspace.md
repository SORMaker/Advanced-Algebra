# Invariant Subspace

In the last section, we discussed the range and kernel of the linear transformation.

In this section, let's introduce the other important concept, the invariant subspace.

First, let's define an invariant subspace.

## Def.7

Let $\mathscr{A}$ be a linear transformation on a linear space $V$ over a field $P$, and let $W$ be a subspace of $V$. If the image of any vector in $W$ under $\mathscr{A}$ remains in $W$.

In other words, for any vector $\xi \in W$, we have $\mathscr{A}\xi \in W$, then we call $W$ an invariant subspace of $\mathscr{A}$, or simply an $\mathscr{A}$ - subspace.

Now, let's discuss some theorems about invariant subspaces.

Furthermore, $\mathscr{A}$ can be regarded as a linear transformation on the subspace $W$, referred to as the restriction of $\mathscr{A}$ to $W$, denoted by $\mathscr{A}|W$, where:
$$
(\mathscr{A}|W)\xi = \mathscr{A}\xi, \forall \alpha \in W.
$$

## Th.11.1

The eigenspace $V_{\lambda_0}$ of the linear transformation $\mathscr{A}$ is an invariant subspace of $\mathscr{A}$.

### Pf.

We know $V_{\lambda_0} = \{ \alpha|\mathscr{A}\alpha = \lambda_0\alpha,\alpha \in V \}$.

For any vector $\xi \in V_{\lambda_0}$, we have $\mathscr{A}\xi = \lambda_0\xi \in V_{\lambda_0}$.

## Th.11.2

Let $\mathscr{A}$ and $\mathscr{B}$ be two linear transformations on $V$ such that $\mathscr{AB} = \mathscr{BA}$.

Then:

1. The range of $\mathscr{A}$, $\mathscr{A}V$, and the kernel of $\mathscr{A},$ $\mathscr{A}^{-1}(0)$, are all invariant subspaces of $\mathscr{B}$.
2. The eigenspaces of $\mathscr{A}$ are invariant subspaces of $B$.

### Pf.

**Part 1**

Let $\alpha \in \mathscr{A}^{-1}(0)$, then $\mathscr{A}\alpha = 0$.

Thus,
$$
\mathscr{A}(\mathscr{B}(\alpha)) = \mathscr{B}(\mathscr{A}(\alpha)) = \mathscr{B}(0) = 0.
$$
This indicates that $\mathscr{B}(\alpha) \in \mathscr{A}^{-1}(0)$.

Therefore, $\mathscr{A}^{-1}(0)$ is an invariant subspace of $\mathscr{B}$.

If $\alpha \in \mathscr{A}V$, then there exists an $\eta \in V$ such that $\mathscr{A}\eta = \alpha$.

Thus,
$$
\mathscr{B}(\alpha) = \mathscr{B}(\mathscr{A}(\eta)) = \mathscr{A}(\mathscr{B}(\eta)) \in \mathscr{A}V.
$$
This indicates that $\mathscr{A}V$ is an invariant subspace of $\mathscr{B}$.

**Part 2**

Let $V_{\lambda_0}$ be the eigenspace of the linear transformation $\mathscr{A}$ corresponding to the eigenvalue $\lambda_0$.

If $\alpha \in V_{\lambda_0}$, then $\mathscr{A}\alpha = \lambda\alpha$.

Thus,
$$
\mathscr{A}(\mathscr{B}(\alpha)) = \mathscr{B}(\mathscr{A}(\alpha)) = \mathscr{B}(\lambda_0\alpha) = \lambda_0\mathscr{B}(\alpha).
$$
 This indicates that $\mathscr{B}(\alpha)$ is an eigenvector of $\mathscr{A}$ corresponding to the eigenvalue $\lambda$, which means $\mathscr{B}(\alpha) \in V_{\lambda_0}$.

Therefore, $V_{\lambda_0}$ is an invariant subspace of $\mathscr{B}$.

Next, let's discuss some properties of an invariant subspace.

## Pt.

1. The sum and intersection of invariant subspaces of a linear transformation $\mathscr{A}$ remain invariant subspaces of $\mathscr{A}$.
2. Let $W = \text{span}\{ \alpha_1, \alpha_2, \cdots, \alpha_s \}$. Then, $W$ is an invariant subspace of $\mathscr{A}$ if and only if $\mathscr{A}(\alpha_i) \in W$, for all $1 \leq i \leq s$.

### Pf.

**Part 1**

Let $V$ be a linear space. Let $W, U$ be two $\mathscr{A}$-subspaces.

We have $\alpha \in W, \beta \in U$.

Then we have $\mathscr{A}\alpha \in W, \mathscr{A}\beta \in U$.

So, $\mathscr{A}(\alpha + \beta) = \mathscr{A}\alpha + \mathscr{A}\beta \in W + U$.

This indicates that the sum of invariant subspaces is still an invariant subspace.

Let $V$ be a linear space. Let $W, U$ be two $\mathscr{A}$-subspaces.

If we have $\alpha \in W \cap U$.

Then, we have $\mathscr{A}\alpha \in W, \mathscr{A}\alpha \in U$.

So, $\mathscr{A}\alpha \in W \cap U$.

This indicates that the intersection of invariant subspaces is still an invariant subspace.

**Part 2**

$\Longrightarrow$

Suppose $W$ is $\mathscr{A}$-subspace.

$\alpha_i \in W, i = 1,2,\cdots,s$.

Then, we know $\mathscr{A}\alpha_i \in W$.

$\Longleftarrow$

Suppose $\mathscr{A}\alpha_i \in W, i = 1,2,\cdots,s$.

$\forall \xi \in W$, $\xi$ can be linearly represented by $\alpha_i$.

So, we have $\xi = \sum_{i = 1}^{s}k_i\alpha_i$.

Then, $\mathscr{A}\xi = \sum_{i = 1}^{s}k_i\mathscr{A}\alpha \in W$.

Thus, $W$ is an invariant subspace of $\mathscr{A}$.

Now, let's discuss the relationship between the matrix of a linear transformation $\mathscr{A}$ and an invariant subspace of $\mathscr{A}$.

**Part 1**

Let $V$ be an n-dimensional linear space. 

Let $\mathscr{A}$ be the linear transformation of $V$.

Let $W$ is the invariant subspace of $\mathscr{A}$.

$\{ \alpha_i \},i=1,\cdots,r$ is a set of bases for $W$, $\{ \alpha_j \},j=1,\cdots,n$ is a set of bases for $V$.

Now, I want to find the matrix of $\mathscr{A}$ under the basis $\{ \alpha_j \}$.

Since $\mathscr{A}(W)$ is the subspace of $W$, then $\mathscr{A}(\alpha_1), \cdots, \mathscr{A}(\alpha_r)$ are the linear combinations of $\{ \alpha_i \}$, $\mathscr{A}(\alpha_1), \cdots, \mathscr{A}(\alpha_n)$ are the linear combinations of $\{ \alpha_j \}$.

That is:
$$
\begin{cases}
\mathscr{A}(\alpha_1) = a_{11}\alpha_1 + a_{21}\alpha_2 + \cdots + a_{r1}\alpha_r,\\
\mathscr{A}(\alpha_2) = a_{12}\alpha_1 + a_{22}\alpha_2 + \cdots + a_{r2}\alpha_r,\\
\cdots\\
\mathscr{A}(\alpha_r) = a_{1r}\alpha_1 + a_{2r}\alpha_2 + \cdots + a_{rr}\alpha_r,\\
\mathscr{A}(\alpha_{r+1}) = a_{1,r+1}\alpha_1 + a_{2,r+1}\alpha_2 + \cdots + a_{r,r+1}\alpha_r + a_{r+1,r+1}\alpha_{r+1} + \cdots + a_{n,r+1}\alpha_n,\\
\cdots\\
\mathscr{A}(\alpha_{n}) = a_{1n}\alpha_1 + a_{2n}\alpha_2 + \cdots + a_{rn}\alpha_r + a_{r+1,n}\alpha_{r+1} + \cdots + a_{nn}\alpha_n,
\end{cases}
$$
Converting back into the matrix form:
$$
A = 
\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1r} & a_{1,r+1} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2r} & a_{2,r+1} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots & \vdots & & \vdots\\
a_{r1} & a_{r2} & \cdots & a_{rr} & a_{r,r+1} & \cdots & a_{rn}\\
 &  &  &  & a_{r+1,r+1} & \cdots & a_{r+1,n}\\
 &  0 &  &  & \vdots & & \vdots\\
 &  &  &  & a_{n,r+1} & \cdots & a_{nn}\\
\end{bmatrix}
=
\begin{bmatrix}
A_1 & A_2\\
0 & A_3
\end{bmatrix} \tag1
$$
On the other hand, if the matrix of $\mathscr{A}$ under the basis $\{ \alpha_j \}$ is $(1)$.

It is easy to prove that the subspace spanned by $\{ \alpha_i \}$ is the invariant subspace of $\mathscr{A}$.

**Part 2**

Now, let's consider the relationship between the matrix of $\mathscr{A}$ is a block diagonal matrix and the invariant subspace.

Here is the theorem 11.3.

## Th.11.3

Let $\mathscr{A}$ be the linear transforamtion of a linear space, then $V$ decomposes into a direct sum of $\mathscr{A}$-invariant subspaces 
$$
V = W_1 \oplus W_2 \oplus \cdots \oplus W_s
$$
if and only if the matrix of $\mathscr{A}$ under some basis is the block diagonal matrix.
$$
\text{diag}\{ A_1, \cdots, A_s \}
$$
$A_i$ is the matrix of $\mathscr{A}|W_i$ under the corresponding basis.

### Pf.

$\Longrightarrow$

Suppose we have $V = W_1 \oplus W_2 \oplus \cdots \oplus W_s$,

Let $W_i = \text{span}\{ \alpha_{i1}, \alpha_{i2}, \cdots, \alpha_{i,n_i} \}$.

Then:
$$
\mathscr{A}(\alpha_{i1}, \alpha_{i2}, \cdots, \alpha_{i,n_i}) = (\alpha_{i1}, \alpha_{i2}, \cdots, \alpha_{i,n_i})A_i,\ i = 1,2,\cdots, s
$$
Furthermore, $A_i$ is $n_i \times n_i$ matrix, and $n_1 + n_2 + \cdots + n_s = n$.

So
$$
\begin{aligned}
&\mathscr{A}(\alpha_{11}, \cdots, \alpha_{1n}, \cdots, \alpha_{s1}, \cdots, \alpha_{sn})\\
&= (\alpha_{11}, \cdots, \alpha_{1n}, \cdots, \alpha_{s1}, \cdots, \alpha_{sn})\begin{bmatrix}A_1 & & &\\& A_2 & &\\& & \ddots &\\& & & A_s \end{bmatrix}
\end{aligned}
$$
$\Longleftarrow$

Let the matrix of $\mathscr{A}$ under some basis $\{ \alpha_{11}, \cdots, \alpha_{1n_1}, \cdots, \alpha_{s1}, \cdots, \alpha_{sn} \},\ n_1 + n_2 + \cdots + n_s = n$ be 
$$
\begin{bmatrix}A_1 & & &\\& A_2 & &\\& & \ddots &\\& & & A_s \end{bmatrix}
$$
$A_i$ is $n_i \times n_i$ matrix.

Let $W_i = \text{span}\{ \alpha_{i1}, \alpha_{i2}, \cdots, \alpha_{i,n_i} \}, \quad i = 1,2,\cdots, s$.

Then:
$$
\mathscr{A}(\alpha_{i1}, \alpha_{i2}, \cdots, \alpha_{i,n_i}) = (\alpha_{i1}, \alpha_{i2}, \cdots, \alpha_{i,n_i})A_i,\ i = 1,2,\cdots, s
$$
which means $\mathscr{A}(\alpha_{ij}) \in W_i, \quad j = 1,2,\cdots,n_i$.

So $W_i$ is the invariant subspace of $\mathscr{A}$, and $V = W_1 \oplus W_2 \oplus \cdots \oplus W_s$.

Then, let's discuss one of the most important subspaces of linear transformation, the generalized eigenspace.

## Th.12

Let $\mathscr{A}$ be the linear transformation. Let $f(\lambda)$ be the characteristic polynomial of $\mathscr{A}$.

If the characteristic polynomial splits into linear factors,
$$
f(\lambda) = (\lambda - \lambda_1)^{r_1}(\lambda - \lambda_2)^{r_2}\cdots(\lambda - \lambda_s)^{r_s}
$$
Then the vector space $V$ decomposes into a direct sum of invariant subspaces.
$$
V = V_1 \oplus V_2 \oplus \cdots \oplus V_s
$$

$$
V_i = \{ \xi \in V|(\mathscr{A} - \lambda_i\mathscr{E})^{r_i}\xi = 0 \}
$$

$V_i$ is the generalized eigenspace of $\mathscr{A}$ corresponding to the eigenvalue $\lambda_i$, denoted by $V^{\lambda_i}$

### Pf.

**Proof Strategy**

1. Construct the subspace $W_i = f_i(\mathscr{A})V$, where $f_i(\lambda) = \frac{f(\lambda)}{(\lambda - \lambda_i)^{r_1}}$. Prove that $W_i \sub V_i$.
2. Prove that $V = W_1 \oplus W_2 \oplus \cdots \oplus W_s$.
3. Prove that $W_i \supset V_i$.

**Part 1**

Let $f(\lambda_i) = \frac{f(\lambda)}{(\lambda - \lambda_i)} = (\lambda - \lambda_1)^{r_1}\cdots(\lambda - \lambda_{i-1})^{r_{i-1}}(\lambda - \lambda_{i+1})^{r_{i+1}}\cdots(\lambda - \lambda_s)^{r_s}$.

Let $W_i = f_i(\mathscr{A})V$.

Then, $W_i$ is the range of $f_i(\mathscr{A})$.

According to Theorem 11.2, we know that $W_i$ is a $\mathscr{A}$-subspace.

Then, for any $\eta_i = f_i(\mathscr{A})\xi_i \in W_i, \xi_i \in V$.
$$
\begin{aligned}
(\mathscr{A} - \lambda\mathscr{E})^{r_i}\eta_i &= (\mathscr{A} - \lambda\mathscr{E})^{r_i}f_i(\mathscr{A})\xi_i\\
&= f(\mathscr{A})\xi_i\\
&= \mathscr{0}\xi_i\\
&= \{0\}.
\end{aligned}
$$
So, $\eta_i \in V_i$.

So, $W_i \sub V_i$.

**Part 2**

Now we need to prove that $V = W_1 \oplus W_2 \oplus \cdots \oplus W_s$.

First, we prove that $V = W_1 + W_2 + \cdots + W_s$.

Because $(f_1(\lambda), f_2(\lambda), \cdots, f_s(\lambda)) = 1$, then there exists some polynomial $u_1(\lambda), u_2(\lambda), \cdots, u_s(\lambda)$ such that
$$
u_1(\lambda)f_1(\lambda) + u_2(\lambda)f_2(\lambda) + \cdots + u_s(\lambda)f_s(\lambda) = 1
$$

> This is in Page 11.

Then, we have:
$$
u_1(\mathscr{A})f_1(\mathscr{A}) + u_2(\mathscr{A})f_2(\mathscr{A}) + \cdots + u_s(\mathscr{A})f_s(\mathscr{A}) = \mathscr{E}.
$$
For any vector $\alpha \in V$,
$$
\alpha = \mathscr{E}\alpha = u_1(\mathscr{A})f_1(\mathscr{A})\alpha + u_2(\mathscr{A})f_2(\mathscr{A})\alpha + \cdots + u_s(\mathscr{A})f_s(\mathscr{A})\alpha
$$
And $u_i(\mathscr{A})(f_i(\mathscr{A})(\alpha)) = f_i(\mathscr{A})(u_i(\mathscr{A})(\alpha)) \in W_i$

So $V = W_1 + W_2 + \cdots + W_s$.

Second, we prove that the representation of the zero vector is unique.

If the representation of zero vector is unique, then $V = W_1 \oplus W_2 \oplus \cdots \oplus W_s$.

Suppose $\beta_1 + \cdots + \beta_s = 0$, $\beta_i \in V_i$.

When $i \neq j$, we know $(\lambda - \lambda_i)^{r_j}|f_i(\lambda)$, $(\mathscr{A} - \lambda_j\mathscr{E})^{r_j}\beta_j = 0$.

Then:
$$
\begin{aligned}
f_i(\mathscr{A})\beta_j &= \frac{f(\mathscr{A})}{(\lambda - \lambda_i)}\beta_j\\
&= \frac{f_j(\mathscr{A})}{(\lambda - \lambda_i)}(\mathscr{A} - \lambda_j\mathscr{E})^{r_j}\beta_j\\
&= 0
\end{aligned}
$$
So, $f_i(\mathscr{A})(\beta_1 + \beta_2 + \cdots + \beta_s) = f_i(\mathscr{A})\beta_i = 0$.

Notice $(f_i(\lambda), (\lambda - \lambda_i)^{r_i}) = 1$, there exists $u(\lambda), v(\lambda)$ such that
$$
u(\lambda)f_i(\lambda) + v(\lambda)(\lambda - \lambda_i)^{r_i} = 1.
$$
So,
$$
\beta_i = \mathscr{E}\beta_i = u(\mathscr{A})f_i(\mathscr{A})\beta_i + v(\mathscr{A})(\mathscr{A} - \lambda_i\mathscr{E})^{r_i}\beta_i = 0
$$
Suppose $\alpha_1 + \alpha_2 + \cdots + \alpha_s = 0$, $\alpha_i \in W_i \sub V_i$.

According to the above, we know $\alpha_1 = \cdots = \alpha_s = 0$.

So, $V = W_1 \oplus W_2 \oplus \cdots \oplus W_s$.

**Part 3**

Suppose $\alpha \in V_i$, then we have $\alpha = \alpha_1 + \cdots + \alpha_s$, where $\alpha_i \in W_i \sub V$.

So $\alpha_1 + \cdots + (\alpha_i - \alpha) + \cdots + \alpha_s = 0$.

Notice that $\alpha_i, \alpha \in V_i$, so $\alpha_i - \alpha \in V_i$.

According to part 2, we know that the representation of zero vector is unique.

So $\alpha_1 = \cdots = \alpha_i - \alpha = \cdots = \alpha_s = 0$.

Then $\alpha = \alpha_i \in W_i$.

Which means $W_i \supset V_i$, so $W_i = V_i$.

Finally, we have $V = V_1 \oplus V_2 \oplus \cdots \oplus V_s$.

