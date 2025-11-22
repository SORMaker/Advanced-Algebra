# Diagonal Matrix

Now, let's move to section 5 -- the diagonal matrix.

A diagonal matrix can be considered the simplest matrix.

We know that linear transformation matrices are generally different under different bases.

Can we choose a suitable set of bases so that our linear transformation matrix is diagonal?

What is the relationship between a diagonal matrix and the eigenvalues and eigenvectors discussed in Section 4?

Theorem 7 answers this question.

## Th.7

Let $\mathscr{A}$ be a linear transformation of an n-dimensional linear space $V$, the matrix of $\mathscr{A}$ is a diagonal matrix under a basis if and only if $\mathscr{A}$ has $n$ linearly independent eigenvectors.

## Pf.

$\Longrightarrow$

Suppose the linear transformation $\mathscr{A}$ has a diagonal matrix $A$ with respect to $\{ \epsilon_1, \epsilon_2, \cdots, \epsilon_n \}$.
$$
A = 
\begin{bmatrix}
\lambda_1 & & & \\
& \lambda_2 & & \\
& & \ddots & \\
& & & \lambda_n
\end{bmatrix}
$$
 This is to say,
$$
\mathscr{A}\epsilon_i = \lambda_i \epsilon_i, \quad i = 1,2, \cdots, n.
$$
So, $\{ \epsilon_i \}, i = 1,2,\cdots,n$ are n linearly independent eigenvectors.

$\Longleftarrow$

If the linear transformation $\mathscr{A}$ has n linearly independent eigenvectors $\{ \epsilon_i \}$, then we can take them as the basis.

The matrix of $\mathscr{A}$ is diagonal.

Theorem 7 tells us we need n linearly independent eigenvectors.

To further provide some discrimination conditions, we need to prove Theorem 9.

## Th.9

Let $\lambda_1, \cdots, \lambda_k$ be the distinct eigenvalues of a linear transformation $\mathscr{A}$ and let $\{ \alpha_{i1}, \cdots, \alpha_{ir_i} \}$ be a set of linearly independent eigenvectors associated with the eigenvalue $\lambda_i$.

Then, the combined set of all these vectors $\{ \alpha_{11}, \cdots, \alpha_{1r_1}, \cdots, \alpha_{k1}, \cdots, \alpha_{kr_k} \}$ is also linearly independent.

### Pf.

We will prove the theorem by mathematical induction on $k$, the number of distinct eigenvalues.

When $k=1$, the set of vectors is $S_1 = \{ \alpha_{11}, \cdots, \alpha_{1r_1} \}$. They are linearly independent, so the theorem is true.

Assume that the statement is true for $k$ distinct eigenvalues.

Now, let's consider $k+1$ distinct eigenvalues, $\lambda_1, \cdots, \lambda_{k+1}$, and their corresponding linearly independent sets of eigenvectors, $S_i = \{ \alpha_{i1}, \cdots, \alpha_{ir_i} \}, \quad i = 1,2, \cdots, k+1$.

So, we want to prove their union $S = S_1 \cup \cdots \cup S_k \cup S_{k+1}$ is linearly independent.

Suppose we have
$$
\sum_{i = 1}^{r_1}l_{1i}\alpha_{1i} + \cdots + \sum_{i = 1}^{r_{k+1}}l_{k+1, i}\alpha_{k+1, i} = 0. \tag1
$$
First, multiply equation $(1)$ by $\lambda_{k+1}$:
$$
\sum_{i = 1}^{r_1}l_{1i}\lambda_{k+1}\alpha_{1i} + \cdots + \sum_{i = 1}^{r_{k+1}}l_{k+1, i}\lambda_{k+1}\alpha_{k+1, i} = 0. \tag2
$$
Second, apply the linear transformation $\mathscr{A}$ to both sides of equation $(1)$.

Since they are eigenvectors, we have:
$$
\sum_{i = 1}^{r_1}l_{1i}\lambda_1\alpha_{1i} + \cdots + \sum_{i = 1}^{r_{k+1}}l_{k+1, i}\lambda_{k+1}\alpha_{k+1, i} = 0. \tag3
$$
Now, we use equation $(3)$ to subtract equation $(2)$. The terms for $i = k+1$ cancel out, leaving:
$$
\sum_{i = 1}^{r_1}l_{1i}(\lambda_1 - \lambda_{k+1})\alpha_{1i} + \cdots + \sum_{i = 1}^{r_{k}}l_{k, i}(\lambda_{k} - \lambda_{k+1})\alpha_{k, i} = 0. \tag4
$$
The equation $(4)$ is a linear combination of the vectors in $S_1 \cup \cdots \cup S_k$.

According to the inductive hypothesis, this set of vectors is linearly independent.

Therefore, all coefficients in equation $(4)$ are zero:
$$
l_{ij}(\lambda_i - \lambda_{k+1}) = 0, \quad i,j = 1,2,\cdots,k.
$$
 Because all eigenvalues are distinct, which means $(\lambda_i - \lambda_{k+1}) \neq 0$.

Consequently, we have:
$$
l_{ij} = 0, \quad i,j = 1,2,\cdots,k.
$$
Finally, we get:
$$
\sum_{i = 1}^{r_{k+1}}l_{k+1, i}\alpha_{k+1, i} = 0. \tag5
$$
By the assumption, we know $\alpha_{k+1, 1}, \cdots, \alpha_{k+1,r_{k+1}}$ are linearly independent.

Thus, all its coefficients are zero: $l_{k+1,j} = 0, j = 1,\cdots, r_{k+1}$.

Therefore, the set $S = S_1 \cup \cdots \cup S_{k+1}$ is linearly independent.

This proof is done.

According to Theorem 9, for a linear transformation, the union of linearly independent eigenvectors obtained from each eigenvalue is still linearly independent.

If the number of eigenvectors equals the dimension of the space, then the matrix of $\mathscr{A}$ is a diagonal matrix under a basis.

In other words, the linear transformation $\mathscr{A}$ is diagonalizable if and only if the sum of the dimensions of the eigenspaces $V_{\lambda_i}$ equals $n$, where $\lambda_i$ are the distinct eigenvalues and $n$ is the dimension of the space.

We can quickly get two corollaries.

## Co.1

In an n-dimensional linear space $V$, if the characteristic polynomial of the linear transformation $\mathscr{A}$ has $n$ distinct roots in the field $P$---that is, if $\mathscr{A}$ has $n$ distinct eigenvalues---then the matrix of $\mathscr{A}$ with respect to some basis is diagonal.

### Pf.

If $\mathscr{A}$ has $n$ distinct eigenvalues, which means $k = n$.

For any eigenvalue $\lambda_i$, we know the dimension of the eigenspace $V_{\lambda_i}$ is grater or equal to 1.

So the sum of the dimensions is
$$
\sum_{i = 1}^{n}dim(V_{\lambda_i}) \geq \sum_{i = 1}^{n}1 = n.
$$
We know
$$
\sum_{i = 1}^{n}dim(V_{\lambda_i}) \leq n.
$$
So, the sum of the dimensions is equal to $n$.

Then the matrix of $\mathscr{A}$ with respect to some basis is diagonal.

Because over the complex field, any polynomial of degree $n$ has $n$ roots, we have

## Co.2

In a linear space over the complex field, if the characteristic polynomial of the linear transformation $\mathscr{A}$ has no multiple roots, then the matrix of $\mathscr{A}$ with respect to some basis is diagonal.
