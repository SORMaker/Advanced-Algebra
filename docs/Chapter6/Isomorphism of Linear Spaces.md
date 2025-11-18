# Isomorphism of Linear Spaces

> We have studied the coordinate relationship between a linear space $V$ and $P^n$. Now, we will elevate this 'correspondence' to a more general and profound level, which is 'isomorphism'.

## Def.11

Let $V$ and $V'$ be two linear spaces over a number field $P$. They are called isomorphic if there exists a bijection $\sigma$ from $V$ to $V'$ that has the following properties:

1. $\sigma(\alpha + \beta) = \sigma(\alpha) + \sigma(\beta)$
2. $\sigma(k\alpha) = k\sigma(\alpha)$, where $\alpha, \beta$ are any vectors in $V$, and $k$ is any number in $P$. 

Such a mapping $\sigma$ is called an isomorphic mapping(or an isomorphism).

$V \cong V' \Longleftrightarrow \exists \sigma:V \rightarrow V'$ s.t. 

1. $\sigma$ is a bijection.
2. $\sigma(\alpha + \beta) = \sigma(\alpha) + \sigma(\beta), \quad \forall\alpha,\beta \in V$
3. $\sigma(k\alpha) = k\sigma(\alpha), \forall \alpha \in V, \forall k \in P$.

> Before we discuss Theorem 12, let's see some properties of isomorphism.

1. $\sigma(0) = 0, \sigma(-\alpha) = -\sigma(\alpha).$
2. $\sigma(k_1\alpha_1 + \cdots + k_s\alpha_s) = k_1\sigma(\alpha_1) + \cdots + k_s\sigma(\alpha_s).$
3. A set of vectors $\alpha_1,\cdots, \alpha_s$ in $V$ is linearly dependent(or independent) if and only if their images $\sigma(\alpha_1), \cdots, \sigma(\alpha_s)$ are linearly dependent(or independent) in $V'$.
4. If $V_1$ is a subspace of $V$, then its image $\sigma(V_1) = \{  \sigma(\alpha)|\alpha \in V_1 \}$ is a subspace of $\sigma(V)$. And $dim(V_1) = dim(\sigma(V_1))$.
5. The inverse mapping $\sigma^{-1}$(from $V'$ to $V$) of an isomorphism is also an isomorphism.

> So, what property is shared by all isomorphic spaces and uniquely identifies them?
>
> Theorem 12 answers: dimension.

## Th.12

Two finite-dimensional linear spaces over the field $P$ are isomorphic if and only if they have the same dimension.

### Pf.

$\Longrightarrow$:

Suppose $V \cong V'$, and there exists an isomorphism $\sigma: V \rightarrow V'$.

Assume the dimension of $V$ is $n$.

According to the property above, we know that $\sigma(\alpha_1), \cdots, \sigma(\alpha_n)$ must be a basis of $V'$. 

So, the dimension of $V'$ is $n$.

$\Longleftarrow$:

Suppose $dim(V) = dim(V') = n$.

We know that any n-dimensional linear space is isomorphic to $P^n$

So, we established two isomorphisms $\sigma_1:V \rightarrow P^n, \sigma_2:V' \rightarrow P^n$.

Since $V$ and $V'$ are both isomorphic to $P^n$, then we can construct  $\sigma = \sigma_2^{-1}\sigma_1$ as the isomorphism from $V$ to $V'$.



