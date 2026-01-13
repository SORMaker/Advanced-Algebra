# Definition and properties of Euclidean space

## Def.1

Let $V$ be a linear space over the field $\R$. A binary real-valued function is defined on $V$, called an inner product, and is denoted by $(\alpha, \beta)$. 

It satisfies the following properties:

1. $(\alpha, \beta) = (\beta, \alpha)$
2. $(k\alpha, \beta) = k(\alpha, \beta)$
3. $(\alpha + \beta, \gamma) = (\alpha, \gamma) + (\beta, \gamma)$
4. $(\alpha, \alpha) \geq 0$, and $(\alpha, \alpha) = 0$ if and only if $\alpha = 0$.

where $\alpha, \beta, \gamma$ are arbitrary vectors in $V$, and $k$ is an arbitrary real number.

Such a linear space $V$ is called a Euclidean space.

## Def.2

The non-negative real number $\sqrt{(\alpha, \alpha)}$ is called the length of vector $\alpha$, denoted as $|\alpha|$.

Obviously, the length of a vector is generally a positive number.

The length is zero if and only if it's the zero vector.

The length defined in this way conforms to the well-known property:
$$
|k\alpha| = |k| \cdot |\alpha|.
$$
where $k \in \R$ and $\alpha \in V$.

A vector with a length of 1 is called a unit vector.

If $\alpha \neq 0$, then the vector 
$$
\frac{1}{|\alpha|}\alpha.
$$
is a unit vector.

Dividing the vector $\alpha$ by its length yields a unit vector proportional to $\alpha$. This process is commonly referred to as normalizing $\alpha$.

## Def.2.1

In order to introduce the concept of an angle in a general Euclidean space, we need to prove the inequality:
$$
\left| \frac{(\boldsymbol{\alpha}, \boldsymbol{\beta})}{|\boldsymbol{\alpha}| \cdot |\boldsymbol{\beta}|} \right| \le 1.
$$
This is the so-called Cauchy-Bunyakovsky inequality.

That is, for any vectors $\alpha$, $\beta$, we have:
$$
|(\alpha, \beta)| \leq |\alpha| \cdot |\beta|.
$$
The equality holds if and only if $\alpha$ and $\beta$ are linearly dependent.

### Pf.

Naturally, if $\beta = 0$, the equation $|(\alpha, \beta)| \leq |\alpha| \cdot |\beta|$ holds obviously.

Below, assume $\beta \neq 0$.

Let $t$ be a real variable, and construct the vector:
$$
\gamma = \alpha + t\beta.
$$
Regardless of the value of $t$, we must have:
$$
(\gamma, \gamma) = (\alpha + t\beta, \alpha + t\beta) \geq 0.
$$
That is:
$$
(\alpha, \alpha) + 2(\alpha, \beta)t + (\beta, \beta)t^2 \geq 0.
$$
Take
$$
t = - \frac{(\alpha, \beta)}{(\beta, \beta)},
$$
and substitute it into the equation above. We obtain:
$$
(\alpha, \alpha) - \frac{(\alpha, \beta)^2}{(\beta, \beta)} \geq 0,
$$
which implies:
$$
(\alpha, \beta)^2 \leq (\alpha, \alpha)(\beta, \beta).
$$
Taking the square root of both sides, we get:
$$
|(\alpha, \beta)| \leq |\alpha| \cdot |\beta|.
$$
When $\alpha$, $\beta$ are linearly dependent, the equality obviously holds.

Conversely, if the equality holds, it can be seen from the proof process above that either $\beta = 0$, or:
$$
\alpha - \frac{(\alpha, \beta)}{(\beta, \beta)}\beta = 0,
$$
which means $\alpha$ and $\beta$ are linearly dependent.

## Def.3

The angle between two non-zero vectors is 
$$
\langle \boldsymbol{\alpha}, \boldsymbol{\beta} \rangle = \arccos \frac{(\boldsymbol{\alpha}, \boldsymbol{\beta})}{|\boldsymbol{\alpha}| \cdot |\boldsymbol{\beta}|}, \quad 0 \le \langle \boldsymbol{\alpha}, \boldsymbol{\beta} \rangle \le \pi.
$$
Based on the Cauchy-Bunyakovsky inequality, we have the triangle inequality:
$$
|\alpha + \beta| \leq |\alpha| + |\beta|.
$$
Because:
$$
\begin{aligned}
|\alpha + \beta|^2 &= (\alpha + \beta, \alpha + \beta) \\
&= (\alpha, \alpha) + 2(\alpha, \beta) + (\beta, \beta) \\
&\leq |\alpha|^2 + 2|\alpha| \cdot |\beta| + |\beta|^2 \\
&= (|\alpha| + |\beta|)^2.
\end{aligned}
$$
Therefore:
$$
|\alpha + \beta| \leq |\alpha| + |\beta|.
$$

## Def.4

If the inner product of two vectors $\alpha$, $\beta$ is zero, which means:
$$
(\alpha, \beta) = 0.
$$
Then $\alpha$, $\beta$ are called orthogonal or perpendicular to each other, denoted as $\alpha \perp \beta$.

Two vectors are orthogonal if and only if their angle is $\frac{\pi}{2}$.

Only the zero vector is orthogonal to itself.

The Pythagorean theorem similarly holds in Euclidean space.

That is, when $\alpha$ and $\beta$ are orthogonal,
$$
|\alpha + \beta|^2 = |\alpha|^2 + |\beta|^2
$$
In fact,
$$
\begin{aligned}
|\alpha + \beta|^2 &= (\alpha + \beta, \alpha + \beta) \\
&= (\alpha, \alpha) + 2(\alpha,\beta) + (\beta, \beta) \\
&= |\alpha|^2 + |\beta|^2.
\end{aligned}
$$
It is not difficult to generalize the Pythagorean theorem to the case of multiple vectors.

That is to say, if the vectors $\alpha_1, \alpha_2, \cdots, \alpha_m$ are pairwise orthogonal, then
$$
|\alpha_1 + \alpha_2 + \cdots + \alpha_m|^2 = |\alpha_1|^2 + |\alpha_2|^2 + \cdots + |\alpha_m|^2.
$$
Let $V$ be an n-dimensional Euclidean space, and let $\epsilon_1, \cdots, \epsilon_n$ be a set of bases of $V$, then for any two vectors of $V$.

We have:
$$
\alpha = x_1\epsilon_1 + \cdots + x_n\epsilon_n, \quad \beta = y_1\epsilon_1 + \cdots + y_n\epsilon_n.
$$
According to the property of the inner product:
$$
(\alpha, \beta) = (x_1\epsilon_1 + \cdots + x_n\epsilon_n, y_1\epsilon_1 + \cdots + y_n\epsilon_n) = \sum_{i = 1}^n\sum_{j=1}^n(\epsilon_i, \epsilon_j)x_iy_j.
$$
Let $a_{ij} = (\epsilon_i, \epsilon_j), \quad i,j = 1,2,\cdots,n$.

Obviously, $a_{ij} = (\epsilon_i, \epsilon_j) = (\epsilon_j, \epsilon_i) = a_{ji}$,

So, $(\alpha, \beta) = \sum_{i = 1}^n\sum_{j=1}^na_{ij}x_iy_j.$

Using matrices, $(\alpha, \beta)$ can be rewritten as:
$$
(\alpha, \beta) = X^TAY,
$$
where
$$
X = \begin{bmatrix}x_1\\ x_2\\ \vdots\\ x_n \end{bmatrix},
Y = \begin{bmatrix}y_1\\ y_2\\ \vdots\\ y_n \end{bmatrix}
$$
are the coordinates of $\alpha$ and $\beta$ separately, and the matrix
$$
A = \begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{bmatrix}
$$
is called the Gramian Matrix, denoted as $\mathscr{G}(\epsilon_1, \cdots, \epsilon_n)$.

Suppose $\eta_1, \cdots, \eta_n$ is a basis of $V$, and the transition matrix from $\epsilon_i$ to $\eta_j$ is $C$, which means:
$$
(\eta_1, \cdots, \eta_n) = (\epsilon_1, \cdots, \epsilon_n)C.
$$
Then the Gramian Matrix of $(\eta_1, \cdots, \eta_n)$ is:
$$
\begin{aligned}
B &= \text{Gram}(\eta_1, \cdots, \eta_n)\\ 
&= (\eta_1, \cdots, \eta_n)^T(\eta_1, \cdots, \eta_n)\\
&= ((\epsilon_1, \cdots, \epsilon_n)C)^T((\epsilon_1, \cdots, \epsilon_n)C) \\
&= C^T \text{Gram}(\epsilon_1, \cdots, \epsilon_n) C.
\end{aligned}
$$
That is to say, the Gramian Matrices with different bases are congruent.

And we know that for a non-zero vector $\alpha$, the coordinate of $\alpha$ is not all zero.

So we have $(\alpha, \alpha) = X^TAX > 0$, that is to say the Gramian Matrix is positive definite.
