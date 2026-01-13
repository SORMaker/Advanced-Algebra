# The Standard Form of Real Symmetric Matrix

## Lemma 1

Let $A$ be a real symmetric matrix. Then, all complex eigenvalues of $A$ are real numbers.

### Pf.

Let $\lambda_0$ be an eigenvalue of $A$.

Then there exists a non-zero vector
$$
\xi = \begin{bmatrix} x_1\\ x_2\\ \vdots\\ x_n \end{bmatrix}
$$
satisfying
$$
A\xi = \lambda_0\xi.
$$
Let
$$
\bar{\xi} = \begin{bmatrix} \bar{x}_1\\ \bar{x}_2\\ \vdots\\ \bar{x}_n  \end{bmatrix},
$$
where $\bar{x}_i$ is the complex conjugate of $x_i$.

Then $A\bar{\xi} = \bar{\lambda}_0 \bar{\xi}$.

Consider the equation:
$$
\bar{\boldsymbol{\xi}}^T (A \boldsymbol{\xi}) = \bar{\boldsymbol{\xi}}^T A^T \boldsymbol{\xi} = (A \bar{\boldsymbol{\xi}})^T \boldsymbol{\xi} = (\overline{A \boldsymbol{\xi}})^T \boldsymbol{\xi}
$$
LHS is $\lambda_0\bar{\xi}^T\xi$, RHS is $\bar{\lambda}_0\bar{\xi}^T\xi$.

Thus,
$$
\lambda_0\bar{\xi}^T\xi = \bar{\lambda}_0\bar{\xi}^T\xi.
$$
Since $\xi$ is a non-zero vector,
$$
\bar{\xi}^T\xi = \bar{x}_1x_1 + \cdots + \bar{x}_nx_n \neq 0.
$$
Therefore, $\lambda_0 = \bar{\lambda}_0$, which means $\lambda_0$ is a real number.

## Lemma 2

Let $A$ be a real symmetric matrix,.

let $\mathscr{A}$ be defined as below.
$$
\mathscr{A}\begin{bmatrix} x_1\\ x_2\\ \vdots\\ x_n \end{bmatrix} = A\begin{bmatrix} x_1\\ x_2\\ \vdots\\ x_n \end{bmatrix}
$$
 Then for any $\alpha,\beta \in \R^n$, we have:
$$
(\mathscr{A}\alpha, \beta) = (\alpha, \mathscr{A}\beta)
$$
or equivalently:
$$
\beta^T(A\alpha) = \alpha^TA\beta.
$$

### Pf.

It is easy to prove:
$$
(\mathscr{A}\alpha, \beta) = \beta^T(A\alpha) = \beta^TA^T\alpha = (A\beta)^T\alpha = (\alpha, \mathscr{A}\beta) = (\mathscr{A}\beta, \alpha) = \alpha^T(A\beta) .
$$

## Def.12

A linear transforamtion in a Euclidean space that satisfies $(\mathscr{A}\alpha, \beta) = (\alpha, \mathscr{A}\beta)$ is called a symmetric transformation.

## Lemma 3

Let $\mathscr{A}$ be a symmetric transformation, and let $V_1$ be an $\mathscr{A}$-invariant subspace. 

Then $V_1^{\perp}$ is also an $\mathscr{A}$-invariant subspace.

### Pf.

Let $\alpha \in V_1^{\perp}$. Then we need to prove that $\mathscr{A}\alpha \in V_1^{\perp}$, which is equivalent to showing that $\mathscr{A}\alpha \perp V_1$.

Take any arbitrary $\beta \in V_1$. We know that $\mathscr{A}\beta \in V_1$.

Because $\alpha \perp V_1$, we have:
$$
(\alpha, \mathscr{A}\beta) = 0
$$
 Therefore, using the property of symmetric transforamtions:
$$
(\mathscr{A}\alpha, \beta) = (\alpha, \mathscr{A}\beta) = 0.
$$
This implies that $\mathscr{A}\alpha \perp V_1$, so $\mathscr{A}\alpha \in V_1^{\perp}$.

Thus, $V_1^{\perp}$ is also an $\mathscr{A}$-invariant subspace.

## Lemma 4

Let $A$ ba a real symmetric matrix. Then, eigenvectors in $\R^n$ belonging to distinct eigenvalues of $A$ must be orthogonal.

### Pf.

Let $\lambda, \mu$ be two distinct eigenvalues of $A$, and let $\alpha, \beta$ be the eigenvectors belonging to $\lambda$ and $\mu$ respectively, such that:
$$
A\alpha = \lambda \alpha, A\beta = \mu \beta
$$
Let the linear transformation $\mathscr{A}$ be the symmetric transformation.

Thus, $\mathscr{A}\alpha = \lambda \alpha$ and $\mathscr{A}\beta = \mu \beta$.

From the property $(\mathscr{A}\alpha, \beta) = (\alpha, \mathscr{A}\beta)$, we have:
$$
\lambda(\alpha, \beta) = \mu(\alpha, \beta)
$$
Since $\lambda \neq \mu$, it must be that $(\alpha, \beta) = 0$.

That is to say, $\alpha$ and $\beta$ are orthogonal.

## Th.7

For any real symmetric matrix $A$ of order $n$, there exists an orthogonal matrix $T$ of order $n$ such that $T^TAT = T^{-1}AT$ becomes a diagonal matrix.

### Pf.

Due to the relationship between real symmetric matrices and symmetric transformations, it suffices to prove that the symmetric transformation $\mathscr{A}$ has $n$ eigenvectors that form an orthonormal basis.

We use mathematical induction on the dimension $n$ of the space.

First, when $n = 1$, the conclusion of the theorem holds.

Second, Assume the conclusion of the theorem holds for dimension $n - 1$.

For the $n$-dimensional Euclidean space $\R^n$, the linear transformation $\mathscr{A}$ has at least one eigenvector $\alpha_1$, and its corresponding eigenvalue is a real number $\lambda_1$.

Then, we normalize $\alpha_1$, and still denote it by $\alpha_1$. Construct the orthogonal complement of the subspace spanned by $\alpha_1$, and let this complement be $V_1$.

By Lemma 3, $V_1$ is an $\mathscr{A}$-invariant subspace, and its dimension is $n - 1$. Furthermore, the restriction of $\mathscr{A}$ to $V_1$ clearly also satisfies $(\mathscr{A}\alpha, \beta) = (\alpha, \mathscr{A}\beta)$, so it remains a symmetric transformation.

According to the induction hypothesis, $\mathscr{A}|v_1$ has $n-1$ eigenvectors $\alpha_2, \cdots, \alpha_n$ that form an orthonormal basis for $V_1$.

Consequently, the set $\alpha_1, \alpha_2, \cdots, \alpha_n$ constitutes an orthonormal basis for the entire space $\R^n$, and they are all eigenvectors of $\mathscr{A}$.

The theorem is proven.

## Th.8

Any real quadratic form 
$$
\sum_{i = 1}^{n}\sum_{j = 1}^{n}a_{ij}x_ix_j, \quad a_{ij} = a_{ji}
$$
Can be transformed into a sum of squares via an orthogonal linear transformation:
$$
\lambda_1y_1^2 + \lambda_2y_2^2 + \cdots + \lambda_ny_n^2,
$$
Where the coefficients of the squared terms, $\lambda_1, \lambda_2, \cdots, \lambda_n$, are exactly all the roots of the characteristic polynomial of the matrix $A$.