# Linear Subspace

## Def.7

A non-empty subset $W$ of a linear space $V$ is a linear subspace of $V$ if and only if $W$ is closed under the two operations of $V$:

1. Closed under addition
2. Closed under scalar multiplication 

Before we introduce Theorem 3, let me first talk about the subspace spanned by the set of vectors.

Let $V$ be a linear space over a field $P$, and $\alpha_1, \alpha_2, \cdots, \alpha_r$ in $V$.

$W$ consisting of all possible linear combinations of these vectors, then $W$ is called the subspace spanned by $\alpha_1, \alpha_2, \cdots, \alpha_r$, denoted as:
$$
W = L(\alpha_1, \alpha_2, \cdots, \alpha_r) = \{ k_1\alpha_1 + k_2\alpha_2 + \cdots + k_r\alpha_r|\ k_1,k_2,\cdots,k_r \in P \}
$$

## Th.3

1. Two sets of vectors to span the same subspace if and only if the two sets of vectors are equivalent.
2. The dimension of the subspace $L(\alpha_1, \alpha_2, \cdots, \alpha_r)$ is equal to the rank of the set of vectors $(\alpha_1, \alpha_2, \cdots, \alpha_r)$.

### pf.

1. $\Longrightarrow$:
   We know $L(\alpha_1, \alpha_2, \cdots, \alpha_r) = L(\beta_1, \beta_2, \cdots, \beta_r)$.
   So, each $\alpha_i (i=1,2,\cdots,r)$ can be linearly represented by the set of vectors $\beta_1, \beta_2, \cdots, \beta_r$.
   Similarly, each $\beta_j(j=1,2,\cdots,r)$ can be linearly represented by the set of vectors $\alpha_1, \alpha_2, \cdots, \alpha_r$.
   So the two sets of vectors are equivalent.
   $\Longleftarrow$:
   If $\{ \alpha_i \}$ is equivalent to $\{ \beta_j \}$.
   Then any vector that can be linearly represented by the set of vectors $\{\alpha_i\}$  can also be linearly represented by the set of vectors $\{\beta_j\}$.
   And the converse is also true.

2. The rank of the set of vectors $\alpha_1, \alpha_2, \cdots, \alpha_r$ is $s(s \leq r)$. Suppose $(\alpha_1,\alpha_2, \cdots, \alpha_s)$ is the maximal linearly independent set of $(\alpha_1, \alpha_2, \cdots, \alpha_r)$.
   Which means:
   $$
   \alpha_1,\alpha_2,\cdots,\alpha_r \Longleftrightarrow \alpha_1, \alpha_2, \cdots, \alpha_s
   $$
   Then the linear subspace spanned by $\alpha_1, \alpha_2, \cdots, \alpha_r$ is equal to the linear subspace spanned by $\alpha_1, \alpha_2, \cdots, \alpha_s$.

   So, the dimension of $L(\alpha_1, \alpha_2, \cdots, \alpha_r)$ is equal to $s$.

## Th.4

Let $V$ be a linear space over a field $P$, and the dimension of $V$ is equal to $n$.

Let $W$ be a linear subspace of $V$, and the dimension of $W$ is equal to $m$.

$m < n$, then:

1. There exists a basis for $W$: $\alpha_1, \alpha_2, \cdots, \alpha_m$
2. $\alpha_1, \alpha_2, \cdots, \alpha_m$ can be extended to a basis for $V$. That is, there exists $n-m$ vectors $\alpha_{m+1}, \alpha_{m+2}, \cdots, \alpha_n \in V$, such that $\alpha_1, \cdots, \alpha_m, \alpha_{m+1}, \cdots, \alpha_n$ is a basis for $V$.

### Pf.

We use induction on the dimension difference $n-m$.

When $n-m = 0$, theorem is obviously true.

Assume the theorem holds for $n-m = k$, we consider the case $n-m = k+1$.

Because $\alpha_1, \alpha_2, \cdots, \alpha_m$ is not a basis for $V$, and they are linearly independent. 

Then there exists a vector $\alpha_{m+1}$ in $V$ which can not be linearly represented by $\alpha_1, \alpha_2, \cdots, \alpha_m$.

So $\alpha_1, \alpha_2, \cdots, \alpha_m,\alpha_{m+1}$ must be linearly independent.

Then the dimension of $L(\alpha_1, \alpha_2, \cdots, \alpha_m,\alpha_{m+1}) = m+1$, so the $n - (m-1) = n-m-1=k$.

By the induction hypothesis, $\alpha_1, \alpha_2, \cdots, \alpha_m,\alpha_{m+1}$ can be extended to a basis of $V$.

