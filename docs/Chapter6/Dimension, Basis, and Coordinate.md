# Dimension, Basis, and Coordinate

## Def.5

Let $V$ be a linear space. If there are $n$ linearly independent vectors in $V$, and any $n+1$ vectors in V are linearly dependent, then V is called an n-dimensional linear space.

If a linear space $V$ is not finite-dimensional, then V is called infinite-dimensional.

## Def.6

In an n-dimensional linear space $V$, $n$ linearly independent vectors $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ are called a basis for $V$.

Then any vector $\alpha$ in V can be linearly represented by $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$.

That is,
$$
\alpha = a_1\epsilon_1 + a_2\epsilon_2 + \cdots + a_n\epsilon_n
$$
The unique set of numbers $(a_1, a_2,\cdots,a_n)$ is called the coordinates of $\alpha$ relative to the basis $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$.

## Th.1

If there are n linearly independent vectors $\alpha_1, \alpha_2, \cdots, \alpha_n$ in linear space $V$, and any vector in $V$ can be linearly represented by them.

Then $V$ is n-dimensional and $\alpha_1, \alpha_2, \cdots, \alpha_n$ is a basis for V.

### Pf.

We need to prove that any $n+1$ vectors in V are linearly dependent.

Suppose we have $\beta_1, \beta_2, \cdots, \beta_{n+1}$.

We know that any vector in $V$ can be linearly represented by $\alpha_1, \alpha_2, \cdots, \alpha_n$.

So, we have
$$
\beta_i = k_1\alpha_1 + k_2\alpha_2 + \cdots + k_n\alpha_n,\quad (i = 1,2,\cdots,n+1).
$$
If $\beta_i$ are linearly independent, then we have $n+1 \leq n$.

This is a contradiction.

So $\beta_i$ are linearly dependent, V is n-dimensional, and $\alpha_1, \alpha_2, \cdots, \alpha_n$ are a basis for $V$.



