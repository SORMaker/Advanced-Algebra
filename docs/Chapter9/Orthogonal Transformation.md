# Orthogonal Transformation

## Def.9

A linear transformation $\mathscr{A}$ of a Euclidean space $V$ is called an orthogonal transformation if it preserves the inner product of vectors.

That is to say, for any $\alpha, \beta \in V$, we have:
$$
(\mathscr{A}\alpha, \mathscr{A}\beta) = (\alpha, \beta).
$$

## Th.4

Let $\mathscr{A}$ be a linear transformation of an n-dimensional Euclidean space $V$.

The following four propositions are equivalent:

1. $\mathscr{A}$ is an orthogonal transformation.
2. $\mathscr{A}$ preserves the length of vectors. That is to say, for any $\alpha \in V$, $|\mathscr{A}\alpha| = |\alpha|$.
3. If $\epsilon_1, \cdots, \epsilon_n$ is a standard orthogonal basis, then $\mathscr{A}\epsilon_1, \cdots, \mathscr{A}\epsilon_n$ is also a standard orthogonal basis.
4. The matrix of $\mathscr{A}$ under any standard orthogonal basis is an orthogonal matrix.

### Pf.

$1 \Leftrightarrow 2$

If $\mathscr{A}$ is an orthogonal transformation, then:
$$
(\mathscr{A}\alpha, \mathscr{A}\alpha) = (\alpha, \alpha)
$$
Taking the square root of both sides, we obtain
$$
|\mathscr{A}\alpha| = \alpha
$$
Conversely, if $\mathscr{A}$ preserves the length of vectors, then
$$
(\mathscr{A}\alpha, \mathscr{A}\alpha) = (\alpha, \alpha), \quad (\mathscr{A}\beta, \mathscr{A}\beta) = (\beta, \beta)\\
(\mathscr{A}(\alpha + \beta), \mathscr{A}(\alpha + \beta)) = (\alpha + \beta, \alpha + \beta)
$$
Expanding the last equation, we get
$$
(\mathscr{A}\alpha, \mathscr{A}\alpha) + 2(\mathscr{A}\alpha, \mathscr{A}\beta) + (\mathscr{A}\beta, \mathscr{A}\beta) = (\alpha, \alpha) + 2(\alpha, \beta) + (\beta, \beta).
$$
Using the first two equations to simplify, we have
$$
(\mathscr{A}\alpha, \mathscr{A}\beta) = (\alpha, \beta).
$$
That is to say, $\mathscr{A}$ is an orthogonal transformation.

$1 \Leftrightarrow 3$

Let $\epsilon_1, \cdots, \epsilon_n$ be a standard orthogonal basis, i.e.,
$$
(\epsilon_i, \epsilon_j) = \begin{cases} 1, i = j\\ 0, i \neq j \end{cases} \quad i,j = 1,2, \cdots, n.
$$
If $\mathscr{A}$ is an orthogonal transformation, then
$$
(\mathscr{A}\epsilon_i, \mathscr{A}\epsilon_j) = \begin{cases} 1, i = j\\ 0, i \neq j \end{cases} \quad i,j = 1,2, \cdots, n
$$
This means that $\mathscr{A}\epsilon_1, \mathscr{A}\epsilon_2, \cdots, \mathscr{A}\epsilon_n$ is a standard orthogonal basis.

Conversely, if $\mathscr{A}\epsilon_1, \cdots, \mathscr{A}\epsilon_n$ is a standard orghogonal basis, then given
$$
\alpha = x_1\epsilon_1 + x_2\epsilon_2 + \cdots + x_n\epsilon_n, \quad \beta = y_1\epsilon_1 + y_2\epsilon_2 + \cdots + y_n\epsilon_n
$$
and
$$
\mathscr{A}\alpha = x_1\mathscr{A}\epsilon_1 + \cdots + x_n\mathscr{A}\epsilon_n, \quad \mathscr{A}\beta = y_1\mathscr{A}\epsilon_1 + \cdots + y_n\mathscr{A}\epsilon_n.
$$
We obtain
$$
(\alpha, \beta) = x_1y_1 + \cdots + x_ny_n = (\mathscr{A}\alpha, \mathscr{A}\beta).
$$
Therefore, $\mathscr{A}$ is an orthogonal transformation.

$3 \Leftrightarrow 4$

Let the matrix of $\mathscr{A}$ under the standard orthogonal basis $\epsilon_1, \epsilon_2, \cdots, \epsilon_n$ be $A$, i.e.,
$$
(\mathscr{A}\epsilon_1, \cdots, \mathscr{A}\epsilon_n) = (\epsilon_1, \cdots, \epsilon_n)A.
$$
If $\mathscr{A}\epsilon_1, \cdots, \mathscr{A}\epsilon_n$ is a standard orthogonal basis, then $A$ can be viewed as the transition matrix from the standard orthogonal basis $\epsilon_1, \epsilon_2, \cdots, \epsilon_n$ to $\mathscr{A}\epsilon_1, \mathscr{A}\epsilon_2, \cdots, \mathscr{A}\epsilon_n$.

Therefore, it is an orthogonal matrix.

Conversely, if $A$ is an orthogonal matrix, then $\mathscr{A}\epsilon_1, \cdots, \mathscr{A}\epsilon_n$ is a standard orthogonal basis.

Thus, we have proven the equivalence of 1, 2, 3, and 4.

If $A$ is an orthogonal matrix, then from
$$
A^TA = E.
$$
It follows that
$$
|A^2| = 1 \quad \text{or} \quad |A| = \pm 1.
$$
Therefore, the determinant of an orthogonal transformation is equal to $1$ or $-1$.

An orthogonal transformation with a determinant equal to $1$ is usually a rotation, or referred to as being of the first kind.

An orthogonal transformation with a determinant equal to $-1$ is referred to as being of the second kind.