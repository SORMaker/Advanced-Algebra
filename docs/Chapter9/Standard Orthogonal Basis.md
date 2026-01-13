# Standard Orthogonal Basis

## Def.5

Let $V$ be a Euclidean space. And $\alpha_1, \cdots, \alpha_s$ is a set of vectors in $V$, if they are pairwise orthogonal, they are called a set of orthogonal vectors.

It is easy to prove that the set of orthogonal vectors is linearly independent.

## Def.6

In an n-dimensional Euclidean space, an orthogonal set consisting of n vectors is called an orthogonal basis.

An orthogonal basis consisting of unit vectors is called an orthonormal basis.

Normalizing an orthogonal basis yields an orthonormal basis.

The Gramian Matrix of a set of standard orthogonal bases is:
$$
(\epsilon_i, \epsilon_j) = \begin{cases} 1, i = j\\ 0, i \neq j \end{cases}
$$
In other words, a set of bases is standard orthogonal bases if and only if its Gramian Matrix is a unit matrix.

Under the standard orthogonal basis, the inner product of $\alpha, \beta$ is:
$$
(\alpha, \beta) = x_1y_1 + x_2y_2 + \cdots + x_ny_n = X^TY.
$$

## Th.1

Any set of orthogonal vectors in n-dimensional Euclidean space can be extended into an orthogonal basis.

### Pf.

Let $\alpha_1, \alpha_2, \cdots, \alpha_m$ be an orthogonal set of vectors. We proceed by mathematical induction on $n - m$.

When $n - m = 0$, $\alpha_1, \cdots, \alpha_m$ is already an orthogonal basis.

Assume the theorem holds when $n - m = k$.

That is to say, we can find vectors $\beta_1, \cdots, \beta_k$ such that,
$$
\alpha_1, \cdots, \alpha_m, \beta_1, \cdots, \beta_k.
$$
becomes an orthogonal basis.

Now consider the case where $n - m = k + 1$.

Since $m < n$, there must exist a vector $\beta$ that cannot be linearly expressed by $\alpha_1, \cdots, \alpha_m$.

Construct the vector
$$
\alpha_{m+1} = \beta - k_1\alpha_1 - \cdots - k_m\alpha_m,
$$
where $k_1, \cdots, k_m$ are coefficients to be determined.

Taking the inner product of $\alpha_i$ with $\alpha_{m+1}$, we obtain
$$
(\alpha_i, \alpha_{m+1} ) = ( \beta, \alpha_i ) - k_i( \alpha_1, \alpha_i ), \quad i = 1,2,\cdots,m.
$$
Take 
$$
k_i = \frac{(\beta, \alpha_i)}{(\alpha_i, \alpha_i)}, \quad i = 1,2,\cdots,m.
$$
We have
$$
(\alpha_i, \alpha_{m+1}) = 0, \quad i = 1,2,\cdots,m.
$$
From the choice of $\beta$,  we know that $\alpha_{m+1} \neq 0$.

Therefore, $\alpha_1, \cdots, \alpha_m, \alpha_{m+1}$ is an orthogonal set of vectors.

According to the inductive hypothesis, $\alpha_1, \cdots, \alpha_m, \alpha_{m+1}$ can be extended to an orthogonal basis.

The theorem is proved. 

## Th.2

For any basis $\epsilon_1, \cdots, \epsilon_n$ in an n-dimensional Euclidean space, one can find an orthonormal basis $\eta_1, \cdots, \eta_n$ such that
$$
L(\epsilon_1, \cdots, \epsilon_i) = L(\eta_1, \cdots, \eta_i), \quad i = 1,2,\cdots, n.
$$

### Pf.

Let $\epsilon_1, \cdots, \epsilon_n$ be a basis. We will determine the vectors $\eta_1, \cdots, \eta_n$ one by one.

First, we can take $\eta_1 = \frac{1}{|\epsilon_1|}\epsilon_1$.

Generally, assume that $\eta_1, \cdots, \eta_m$ have already been found.

They are orthonormal and possess the property
$$
L(\epsilon_1, \cdots, \epsilon_i) = L(\eta_1, \cdots, \eta_m), \quad i = 1,2,\cdots,m.
$$
Next, we seek $\eta_{m+1}$.

Since $L(\epsilon_1, \cdots, \epsilon_m) = L(\eta_1, \cdots, \eta_m)$, $\epsilon_{m+1}$ cannot be linearly expressed by $\eta_1, \cdots, \eta_m$.

Following the method in the proof of Theorem 1, construct the vector
$$
\xi_{m+1} = \epsilon_{m+1} - \sum_{i = 1}^{m}(\epsilon_{m+1}, \eta_i)\eta_i.
$$
$\xi_{m+1} \neq 0$, and
$$
(\xi_{m+1}, \eta_i) = 0, \quad i = 1,2,\cdots,m.
$$
Let
$$
\eta_{m+1} = \frac{\xi_{m+1}}{|\xi_{m+1}|}.
$$
Then $\eta_1, \cdots, \eta_m, \eta_{m+1}$ is an orthonormal set of vectors.

At the same time
$$
L(\epsilon_1, \cdots, \epsilon_{m+1}) = L(\eta_1, \cdots, \eta_{m+1}).
$$
By the principle of induction, Theorem 2 is proved.

## Def.7

The above discussed the method for finding an orthonormal basis.

Since orthonormal bases occupy a special position in Euclidean space, it is necessary to discuss the change of basis formula from one orthonormal basis to another orthonormal basis.

Let $\epsilon_1, \cdots, \epsilon_n$ and $\eta_1, \cdots, \eta_n$ be two orthonormal bases in the Euclidean space $V$.

The transition matrix between them is 
$$
A = (a_{ij})_{n \times n},
$$
that is,
$$
(\eta_1, \cdots, \eta_n) = (\epsilon_1, \cdots, \epsilon_n)\begin{bmatrix}a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{bmatrix}
$$
Because $\eta_1 ,\cdots, \eta_n$ is an orthonormal basis, we have
$$
(\eta_i, \eta_j) = \begin{cases} 1, i = j, \\ 0, i \neq j. \end{cases}
$$
The columns of matrix $A$ are the coordinates of $\eta_1, \cdots, \eta_n$ under the orthonormal basis $\epsilon_1, \cdots, \epsilon_n$.

According to the inner product formula, the equation can be expressed as
$$
a_{1i}a_{1j} + a_{2i}a_{2j} + \cdots + a_{ni}a_{nj} = \begin{cases}1, i = j,\\0, i \neq j. \end{cases}
$$
The equation is equivalent to a matrix equality:
$$
A^TA = E,
$$
or
$$
A^{-1} = A^T.
$$
