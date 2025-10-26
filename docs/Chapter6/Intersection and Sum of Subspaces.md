# Intersection and Sum of Subspaces

## Th.5

If $V_1,V_2$ are two subspaces of a linear space $V$, then their intersection is also a subspaces of a linear space $V$.

### Pf.

First, we need to prove $V_1 \cap V_2$ is non-empty.

$0 \in V_1,\ 0 \in V_2$, so $0 \in V_1 \cap V_2$.

$V_1 \cap V_2$ is non-empty.

Then, we need to prove $V_1 \cap V_2$ closed under addition and scalar multiplication.

Suppose we have $\alpha,\beta \in V_1 \cap V_2$.

Then $\alpha,\beta \in V_1$, $\alpha,\beta \in V_2$.

So $\alpha + \beta \in V_1$, $\alpha + \beta \in V_2$.

So $\alpha + \beta \in V_1 \cap V_2$.

Suppose we have $\alpha \in V_1 \cap V_2$ and $k \in P$.

Then $k\alpha \in V_1$ and $k\alpha \in V_2$.

So $k\alpha \in V_1 \cap V_2$.

There are calculation laws about the intersection of subspaces.

- $V_1 \cap V_2 = V_2 \cap V_1$
- $(V_1 \cap V_2) \cap V_3 = V_1 \cap (V_2 \cap V_3)$
- $V_1 \cap V_2 \cap \cdots \cap V_s = \bigcap^s_{i=1}V_i$

## Def.8

Let $V_1,V_2$ be the subspaces of a linear space $V$. Then the sum of $V_1$ and $V_2$ refers to the set composed of all sums of a vector in $V_1$ and a vector in $V_2$.
$$
V_1 + V_2 = \{ \alpha_1 + \alpha_2| \alpha_1 \in V_1, \alpha_2 \in V_2 \}
$$

## Th.6

If $V_1,V_2$ are the subspaces of a linear space $V$, then their sum $V_1 + V_2$ is also the subspaces of $V$.

### Pf.

$V_1 + V_2$ is obviously non-empty.

If $\alpha,\beta \in V_1 + V_2$, that is 
$$
\begin{aligned}
\alpha = \alpha_1 + \alpha_2, \quad \alpha_1 \in V_1, \alpha_2 \in V_2\\
\beta = \beta_1 + \beta_2, \quad \beta_1 \in V_1, \beta_2 \in V_2
\end{aligned}
$$
Then
$$
\alpha + \beta = (\alpha_1 + \beta_1) + (\alpha_2 + \beta_2)
$$
$V_1,V_2$ are subspaces, so
$$
\alpha_1 + \beta_1 \in V_1,\quad \alpha_2 + \beta_2 \in V_2.
$$
Then
$$
\alpha + \beta \in V_1 + V_2
$$
Similarly, 
$$
k\alpha = k\alpha_1 + k\alpha_2 \in V_1 + V_2
$$
So, $V_1 + V_2$ is the subspace of $V$.

There are calculation laws about the sum of subspaces.

- $V_1 + V_2 = V_2 + V_1$
- $(V_1 + V_2) + V_3 = V_1 + (V_2 + V_3)$
- $V_1 + V_2 + \cdots + V_s = \sum^s_{i=1}V_i$

## Pt.

1. Let $V_1,V_2,W$ be the subspaces of $V$, then:
   1. $W \subset V_1, W \subset V_2 \Rightarrow W \subset V_1 \cap V_2$
   2. $V_1 \subset W, V_2 \subset W \Rightarrow V_1 + V_2 \subset W$
2. $V_1 \subset V_2 \Leftrightarrow V_1 \cap V_2 = V_1 \Leftrightarrow V_1 + V_2 = V_2$
3. $L(\alpha_1, \alpha_2,\cdots,\alpha_s) + L(\beta_1,\beta_2,\cdots,\beta_t) = L(\alpha_1, \alpha_2,\cdots,\alpha_s,\beta_1,\beta_2,\cdots,\beta_t)$

### Pf.

1. Let $V_1,V_2,W$ be the subspaces of $V$.

   1. $\alpha \in W \Rightarrow \alpha \in V_1, \alpha \in V_2 \Rightarrow \alpha \in V_1 \cap V_2$
   2. $\alpha \in V_1, \beta \in V_2, \alpha,\beta \in W$, $W$ is a subspace, then $\alpha + \beta \in W \Rightarrow V_1 + V_2 \subset W$

2. $V_1 \subset V_2 \Leftrightarrow V_1 \cap V_2 = V_1$ obviously holds.

   Now we need to prove $V_1 \subset V_2 \Leftrightarrow V_1 + V_2 = V_2$

   1. $V_1 \subset V_2 \Rightarrow V_1 + V_2 = V_2$

      1. $V_1 + V_2 \subset V_2$
         Suppose we have $\alpha \in V_1, \beta \in V_2$, because $V_1 \subset V_2$, then $\alpha \in V_2$.

         So $\alpha + \beta \in V_2$, which means $V_1 + V_2 \subset V_2$.

      2. $V_2 \subset V_1 + V_2$
         Suppose we have $\alpha \in V_2$, then $\alpha = \alpha + 0, \alpha \in V_2, 0 \in V_1$.
         So $\alpha \in V_1 + V_2$, which means $V_2 \subset V_1 + V_2$

      So $V_1 \subset V_2 \Rightarrow V_1 + V_2 = V_2$

   2. $V_1 + V_2 = V_2 \Rightarrow V_1 \subset V_2$
      If $V_1 + V_2 = V_2$, and $V_1 \not\subset V_2$.
      Then $\alpha \in V_1, \alpha \not\in V_2$.
      But we have $\alpha \in V_1$ and $0 \in V_2$, then $\alpha = \alpha + 0 \in V_2$, there is a contradiction.
      So $V_1 \subset V_2$. 

3. Let $V_1 = L(\alpha_1, \alpha_2,\cdots,\alpha_s), V_2 = L(\beta_1,\beta_2,\cdots,\beta_t)$.
   Let $W = L(\alpha_1, \alpha_2,\cdots,\alpha_s,\beta_1,\beta_2,\cdots,\beta_t)$
   Now we need to prove $V_1 + V_2 = W$

   1. $V_1 + V_2 \subset W$

      Any $\alpha \in V_1$, we have $\alpha = k_1\alpha_1 + k_2\alpha_2 + \cdots + k_s\alpha_s$.
      Any $\beta \in V_2$, we have $\beta = l_1\beta_1 + l_2\beta_2 + \cdots + l_s\beta_s$.
      So $\alpha + \beta = k_1\alpha_1 + k_2\alpha_2 + \cdots + k_s\alpha_s + l_1\beta_1 + l_2\beta_2 + \cdots + l_s\beta_s$.
      So $V_1 + V_2 \subset W$

   2. $V_1 + V_2 \supset W$
      Any $\alpha \in W$, we have $\alpha = k_1\alpha_1 + \cdots + k_s\alpha_s + l_1\beta_1 + \cdots + l_s\beta_s$.
      $k_1\alpha_1 + \cdots + k_s\alpha_s \in V_1$, $l_1\beta_1 + \cdots + l_s\beta_s \in V_2$.
      So $V_1 + V_2 \supset W$.

   So $V_1 + V_2 = W$.

## Th.7

If $V_1, V_2$ are two subspaces in linear space $V$, then:
$$
Dim(V_1) + Dim(V_2) = Dim(V_1 + V_2) + Dim(V_1 \cap V_2)
$$

### Pf.

Suppose $Dim(V_1)=n_1, Dim(V_2)=n_2, Dim(V_1 \cap V_2)=m$.

Taking a basis for $V_1 \cap V_2$: $\alpha_1, \alpha_2,\cdots, \alpha_m$.

According to Theorem 4, it can be extended to a basis for $V_1$.
$$
\alpha_1, \alpha_2,\cdots, \alpha_m, \beta_1, \cdots, \beta_{n_1-m}.
$$
And it can also be extended to a basis for $V_2$.
$$
\alpha_1, \alpha_2,\cdots, \alpha_m, \gamma_1, \cdots, \gamma_{n_2-m}.
$$
Now we need to prove that $\alpha_1, \alpha_2,\cdots, \alpha_m, \beta_1, \cdots, \beta_{n_1-m},\gamma_1, \cdots, \gamma_{n_2-m}$ is a basis for $V_1 + V_2$, then $Dim(V_1 + V_2) = n_1 + n_2 - m$.

Because
$$
V_1 = L(\alpha_1, \alpha_2,\cdots, \alpha_m, \beta_1, \cdots, \beta_{n_1-m}), \quad V_2 = L(\alpha_1, \alpha_2,\cdots, \alpha_m, \gamma_1, \cdots, \gamma_{n_2-m}).
$$
Then
$$
V_1 + V_2 = L(\alpha_1, \alpha_2,\cdots, \alpha_m, \beta_1, \cdots, \beta_{n_1-m},\gamma_1, \cdots, \gamma_{n_2-m}).
$$
Now let's prove $\alpha_1, \alpha_2,\cdots, \alpha_m, \beta_1, \cdots, \beta_{n_1-m},\gamma_1, \cdots, \gamma_{n_2-m}$ are linearly independent.

Suppose we have
$$
k_1\alpha_1 + \cdots + k_m\alpha_m + p_1\beta_1 + \cdots + p_{n_1-m}\beta_{n_1-m}+q_1\gamma_1+ \cdots+ q_{n_2-m}\gamma_{n_2-m}=0
$$
Let
$$
\alpha = k_1\alpha_1 + \cdots + k_m\alpha_m + p_1\beta_1 + \cdots + p_{n_1-m}\beta_{n_1-m} = -q_1\gamma_1- \cdots- q_{n_2-m}\gamma_{n_2-m}
$$
According to the first equation, we know $\alpha \in V_1$. According to the second equation, we know $\alpha \in V_2$.

So $\alpha \in V_1 \cap V_2$, then $\alpha$ can be linearly represented by $\alpha_1, \alpha_2,\cdots, \alpha_m$.

Let $\alpha = l_1\alpha_1+ l_2\alpha_2+ \cdots+ l_m\alpha_m$, then
$$
l_1\alpha_1+ l_2\alpha_2+ \cdots+ l_m\alpha_m +q_1\gamma_1+ \cdots+ q_{n_2-m}\gamma_{n_2-m} = 0
$$
$\alpha_1, \alpha_2,\cdots, \alpha_m, \gamma_1, \cdots, \gamma_{n_2-m}$ are linearly independent, so $l_1 = l_2 = \cdots = l_m = q_1 = \cdots = q_{n_2-m} = 0$.

So $\alpha = 0$.

So $k_1\alpha_1 + \cdots + k_m\alpha_m + p_1\beta_1 + \cdots + p_{n_1-m}\beta_{n_1-m} = 0$.

Because $\alpha_1, \alpha_2,\cdots, \alpha_m, \beta_1, \cdots, \beta_{n_1-m}$ are linearly independent, so $k_1 = \cdots = k_m = p_1 = \cdots = p_{n_1-m} = 0$.

So $\alpha_1, \cdots, \alpha_m, \beta_1, \cdots, \beta_{n_1-m},\gamma_1, \cdots, \gamma_{n_2-m}$ are linearly independent.

So $Dim(V_1) + Dim(V_2) = Dim(V_1 + V_2) + Dim(V_1 \cap V_2)$.

## Co.

If $V_1,V_2$ are the subspaces of $V$, and the dimension of $V$ is $n$. The sum of the dimensions of $V_1$ and $V_2$ is grater than $n$.

Then $V_1$ and $V_2$ have non-zero common vector.

### Pf.

$$
Dim(V_1 + V_2) + Dim(V_1 \cap V_2) = Dim(V_1) + Dim(V_2) > n.
$$

$V_1 + V_2$ is the subspace of $V$, then we have $Dim(V_1 + V_2) \leq n$,

so, $Dim(V_1 \cap V_2) > 0$.

Which means $V_1 \cap V_2$ have non-zero vectors.