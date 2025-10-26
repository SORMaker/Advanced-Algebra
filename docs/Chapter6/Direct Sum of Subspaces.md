# Direct Sum of Subspaces

## Def.9

Suppose $V_1, V_2$ are the subspaces of a linear space $V$.

If for every vector $\alpha$ in the sum $V_1 + V_2$, its decomposition
$$
\alpha = \alpha_1 + \alpha_2, \quad \alpha_1 \in V_1, \alpha_2 \in V_2.
$$
is unique, then this sum is called the direct sum of $V_1$ and $V_2$, denoted as $V_1 \bigoplus V_2$.

## Th.8

The sum of $V_1$ and $V_2$ is a direct sum if and only if the equality $\alpha_1 + \alpha_2 = 0, \alpha_i \in V_i, i=1,2$ holds only when $\alpha_1 = \alpha_2 = 0$.

### Pf.

$\Longrightarrow$:

We know $0 + 0 = 0$, and according to the uniqueness of direct sum decomposition, we get $\alpha_1 = \alpha_2 = 0$.

$\Longleftarrow$:

suppose  $\alpha \in V_1 + V_2$, and it has two decompositions.
$$
\alpha = \alpha_1 + \alpha_2 = \beta_1 + \beta_2, \quad \alpha_i,\beta_i \in V_i, \quad i = 1,2.
$$
Subtracting them, we get a decomposition of the zero vector.
$$
(\alpha_1 - \beta_1) + (\alpha_2 - \beta_2) = 0.
$$
The term $\alpha_i - \beta_i$ are still in $V_i$.

Then we should have
$$
\alpha_i - \beta_i = 0, \quad \alpha_i = \beta_i, \quad i=1,2.
$$
Therefore, the decomposition of $\alpha$ is unique.

Furthermore, this theorem has an essential corollary that connects the direct sum to the intersection of subspaces.

> This corollary states:

## Co.1

The sum of two subspaces $V_1$ and $V_2$ is a direct sum if and only if their intersection $V_1 \cap V_2$ contains only the zero vector  $\{ 0 \}$.
$$
V_1 + V_2 = V_1 \bigoplus V_2 \Longleftrightarrow V_1 \cap V_2 = \{ 0 \}
$$

### Pf.

$\Longrightarrow$ :

Suppose $V_1 + V_2$ is a direct sum, and we need to prove $V_1 \cap V_2 = \{ 0 \}$.

Take any vector $\alpha$ from the intersection.

Since $\alpha$ is in both $V_1$ and $V_2$, we can write the $0$ as $\alpha + (-\alpha)$.

But we know $0$ also has the decomposition $0 = 0 + 0$, and the decomposition of the zero vector must be unique.

So we conclude that $\alpha = 0$.

This proves that the only vector in the intersection is the zero vector.

$\Longleftarrow$ :

Assume $V_1 \cap V_2 = \{ 0 \}$, and we need to prove the sum is a direct sum.

According to Theorem 8, we just need to prove that the decomposition of the zero vector is unique.

Suppose
$$
\alpha_1 + \alpha_2 = 0,\quad \alpha_i \in V_i, \quad i = 1,2.
$$
Then rearranging gives
$$
\alpha_1 = -\alpha_2 \in V_1 \cap V_2.
$$
This means $\alpha_1$ must be in their intersection $V_1 \cap V_2$. 

But we assumed this intersection is $\{0\}$.

Which means $\alpha_1 = 0$, and therefore $\alpha_2 = 0$.

So $V_1 + V_2$ is a direct sum.

> Theorem 9 reveals the relationship between a direct sum and dimensions.

## Th.9

Let $V_1,V_2$ be subspaces of $V$, and let $W = V_1 + V_2$.

Then the sum is a direct sum $W = V_1 \bigoplus V_2$ if and only if: $dim(W) = dim(V_1) + dim(V_2)$.
$$
W = V_1 \bigoplus V_2 \Longleftrightarrow dim(W) = dim(V_1) + dim(V_2)
$$
$\Longrightarrow$:

On the one hand, if $W = V_1 \bigoplus V_2$, then according to Theorem 8, $V_1 \cap V_2 = \{0\}$.

So $dim(V_1 \cap V_2) = 0$.

Then, according to the dimension formula, we know.
$$
dim(W) = dim(V_1) + dim(V_2)
$$
$\Longleftarrow$:

On the other hand, if $dim(W) = dim(V_1) + dim(V_2)$, then $dim(V_1 \cap V_2) = 0$.

Since the dimension of the intersection is 0, the intersection can only be $\{0\}$.

According to Theorem 8, this guarantees the sum is a direct sum.

> Thus, we now have three equivalent tools to identify a direct sum:
>
> 1. Unique decomposition.
> 2. Zero intersection.
> 3. Additive dimensions.

> Now, there is a question: If we are given only one subspace $U$ of linear space $V$, can we always find another subspace $W$, such that $V = U \bigoplus V$.
>
> Theorem 10 tells us that the answer is yes.

## Th.10

Let $U$ be a subspace of a vector space $V$. Then there must exist a subspace $W$ of $V$ such that $V = W \bigoplus U$.

### Pf.

Take a basis $\{\alpha_1,\cdots,\alpha_s \}$ for $U$, and extend it to form a basis $\{\alpha_1, \cdots, \alpha_s,\beta_1,\cdots, \beta_m \}$ for $V$.

Let $W = L(\beta_1,\cdots, \beta_m)$ .

The subspaces $U$ and $W$ satisfy the requirements.

> We are now very familiar with the direct sum of two subspaces. 
> Now, we naturally want to generalize this concept to the case of $s$ subspaces.

## Def.10

Let $V_1,\cdots, V_s$ all be subspaces of a linear space $V$.

If the decomposition 
$$
\alpha = \alpha_1 + \alpha_2 + \cdots + \alpha_s,\quad \alpha_i \in V_i, \quad i = 1,2,\cdots,s
$$
for every vector $\alpha$ in the sum $V_1 + \cdots + V_s$ is unique, then this sum is called a direct sum, denoted by
$$
V_1 \bigoplus V_2 \bigoplus \cdots \bigoplus V_s.
$$

> Just as we did for two subspaces, we need a set of equivalent, more easily verifiable conditions. This is where the value of Theorem 11 lies.

## Th.11

Let $V_1,V_2,\cdots, V_s$ be subspaces of $V$. The following conditions are equivalent:

1. The sum $W = \sum^s_{i=1}V_i$ is a direct sum;
2. The representation of the zero vector is unique: 
   $0 = \alpha_1 + \cdots + \alpha_s, \quad \alpha_i \in V_i$, holds only when $\alpha_i = 0$ for all $i = 1,2,\cdots,s$;
3. $V_i \cap \sum_{j \neq i}V_j = \{0\}$
4. $dim(W) = \sum^s_{i=1}dim(V_i)$
