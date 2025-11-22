# Linear Transformation 

> Hi, everyone. Today, we're moving into Chapter 7 to discuss one of the most critical concepts in all of linear algebra: the linear transformation.
>
> So, what's a linear transformation?
>
> The core idea is that a linear transformation is a mapping. It's a function, let's call it $\mathscr{A}$, that takes an input vector $\alpha$ from a linear space $V$ and produces an output vector $\mathscr{A}(\alpha)$ in a linear space $V^\prime$.
>
> But it's not any mapping; it must satisfy the two most important operations in a linear space: vector addition and scalar multiplication.
>
> So the definition one states:

## Def.1

Let $V$ and $V'$ be two linear spaces over the field $P$. A mapping $\mathscr{A}$ from $V$ to $V'$ is called a linear transformation if $\mathscr{A}$ preserves addition and scalar multiplication.
$$
\mathscr{A}(\alpha + \beta) = \mathscr{A}(\alpha) + \mathscr{A}(\beta), \quad \mathscr{A}(k\alpha) = k\mathscr{A}(\alpha)
$$

> It's not difficult to deduce from the definition the following simple properties of a linear transformation.

## Pt.

First, let $\mathscr{A}$ be a linear transformation of $V$, then
$$
\mathscr{A}(0) = 0, \quad \mathscr{A}(-\alpha) = -\mathscr{A}(\alpha).
$$
Second, a linear transformation preserves linear combinations.
$$
\mathscr{A}(k_1\alpha_1 + \cdots + k_r\alpha_r) = k_1\mathscr{A}(\alpha_1) + \cdots + k_r\mathscr{A}(\alpha_r).
$$
Third, a linear transformation maps a linearly dependent set of vectors to a linearly dependent set of vectors. 

However, it doesn't work the other way around.