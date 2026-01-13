# Unitary Space

## Def.14

Let $V$ be a linear space over the complex field $\C$. 

Suppose there is a binary complex-valued function defined on $V$, referred to as the inner product and denoted by $(\alpha, \beta)$, which satisifies the following properties:

1. $(\boldsymbol{\alpha}, \boldsymbol{\beta}) = \overline{(\boldsymbol{\beta}, \boldsymbol{\alpha})}$, where $\overline{(\beta, \alpha)}$ is the complex conjugate of $(\beta, \alpha)$.
2. $(k\alpha, \beta) = k(\alpha, \beta)$.
3. $(\alpha + \beta, \gamma) = (\alpha, \gamma) + (\beta, \gamma)$.
4. $(\alpha, \alpha)$ is a non-negative real number, and $(\alpha, \alpha) = 0$ if and only if $\alpha = 0$.

Here, $\alpha, \beta, \gamma$ are arbitrary vectors in $V$, and $k$ is an arbitrary complex number.

Such a linear space is called a Unitary Space.

Here are some properties:

1. $(\alpha, k\beta) = \bar{k}(\alpha, \beta)$.

2. $(\alpha, \beta + \gamma) = (\alpha, \beta) + (\alpha, \gamma)$.

3. $\sqrt{(\alpha, \alpha)}$ is called the length of vector $\alpha$, denoted by $|\alpha|$.

4. For any vectors $\alpha,\beta$, we have: $|(\alpha, \beta)| \leq |\alpha| \cdot |\beta|$.

5. Vectors $\alpha$ and $\beta$ are called orthogonal if $(\alpha, \beta) = 0$.

6. Any set of linearly independent vectors can be orthogonalized using the Schmidt process and extended to form an orthonormal basis.

7. If $A$ satisfies $\bar{A}^TA = A\bar{A}^T = E$, then $A$ is called a Unitary Matrix. The absolute value of its determinant is equal to 1.

8. A linear transformation $\mathscr{A}$ on a Unitary Space $V$ is called a Unitary Transformation of $V$ if it satisfies: $(\mathscr{A}\alpha, \mathscr{A}\beta) = (\alpha, \beta)$. The matrix of a unitary transformation with respect to an orthonormal basis is a unitary matrix.

9. If a matrix satisfies $\bar{A}^T = A$. It is called a Hermitian matrix.
   In the unitary space $\C^n$, let $\mathscr{A}\begin{bmatrix}x_1\\x_2\\\vdots\\x_n \end{bmatrix} = A\begin{bmatrix}x_1\\x_2\\\vdots\\x_n \end{bmatrix}$, then $(\mathscr{A}\alpha, \beta) = (\alpha, \mathscr{A}\beta)$.

10. If $V$ is a unitary space and $V_1$ is a subspace, and $V_1^{\perp}$ is the orthogonal complement of $V_1$, then $V = V_1 \oplus V_1^{\perp}$. Furthermore, if $V_1$ is an invariant subspace of a symmetric transformation, then $V_1^{\perp}$ is also an invariant subspace.

11. The eigenvalues of a Hermitian matrix are real numbers. Eigenvectors belonging to distinct eigenvalues must be orthogonal.

12. If $A$ is a Hermitian matrix, then there exists a unitary matrix $C$ such that
    $$
    C^{-1}AC = \overline{C}^TAC
    $$
    is diagonal matrix.

13. Let $A$ be a Hermitian matrix. The quadratic form
    $$
    f(x_1, x_2, \cdots, x_n) = \sum_{i = 1}^n\sum_{j=1}^na_{ij}x_i\overline{x}_j = X^TA\overline{X}.
    $$
    is called a Hermitian Quadratic Form. There exists a unitary matrix $C$ such that when $X = CY$,
    $$
    f(x_1, x_2, \cdots, x_n) = d_1y_1\overline{y}_1 + d_2y_2\overline{y}_2 + \cdots + d_ny_n\overline{y}_n.
    $$
    