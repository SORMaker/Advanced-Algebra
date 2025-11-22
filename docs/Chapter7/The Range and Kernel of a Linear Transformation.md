# The Range and Kernel of a Linear Transformation

In the previous section, we discussed matrix diagonalization; however, the conditions for this are pretty strict. So, if a matrix cannot be diagonalized, what do we do? The Jordan Normal Form, which we will cover in Section 8, is the general solution to this problem. However, before we proceed, we need to prepare two essential tools: invariant subspaces and the topic of this section, the Range and Kernel of a Linear Transformation.

First, definition six states:

## Def.6

Let $\mathscr{A}$ be a linear transformation on a linear space $V$. The set of all images under $\mathscr{A}$ is called the range of $\mathscr{A}$, denoted by $\mathscr{A}V$. The set of all vectors that are mapped to the zero vector by $\mathscr{A}$ is called the kernel of $\mathscr{A}$, denoted by $\mathscr{A}^{-1}(0)$.

Using set notation, they are defined as:
$$
\begin{aligned}
\mathscr{A}V &= \{ \mathscr{A}(\alpha) | \alpha \in V \}.\\
\mathscr{A}^{-1}(0) &= \{ \xi | \mathscr{A}\xi=0, \xi \in V \}
\end{aligned}
$$
It's easy to prove that the range and kernel of a linear transformation are the subspaces of $V$.

The dimension of $\mathscr{A}V$ is called the rank of $\mathscr{A}$.

The dimension of $\mathscr{A}^{-1}(0)$ is called the nullity of $\mathscr{A}$.

What is the relationship between the rank of a linear transformation and the rank of a matrix?

Theorem 10 states:

## Th.10

Let $\mathscr{A}$ be a linear transformation on an n-dimensional linear space $V$.  Let $\{ \epsilon_i \}, i = 1,2,\cdots,n$ be a basis for $V$, and let $A$ be the matrix of $\mathscr{A}$ relative to this basis. Then:

1. $\mathscr{A}V$ is the subspace spanned by the images of the basis vectors. That is:
	$$
	\mathscr{A}V = span(\mathscr{A}\epsilon_1, \mathscr{A}\epsilon_2, \cdots, \mathscr{A}\epsilon_n)
	$$

2. The rank of $\mathscr{A}$ is equal to the rank of the matrix $A$.

### Pf.

**Part 1**

$\Longrightarrow$
$$
\forall \xi \in V,\mathscr{A}\xi \in \mathscr{A}V\\
\mathscr{A}\xi = x_1\mathscr{A}\epsilon_1 + \cdots + x_n\mathscr{A}\epsilon_n\\
\mathscr{A}\xi \in span(\mathscr{A}\epsilon_1, \cdots, \mathscr{A}\epsilon_n)\\
\mathscr{A}V \sub span(\mathscr{A}\epsilon_1, \cdots, \mathscr{A}\epsilon_n)
$$
$\Longleftarrow$
$$
\forall \xi \in span(\mathscr{A}\epsilon_1, \cdots, \mathscr{A}\epsilon_n)\\
\xi = x_1'\mathscr{A}\epsilon_1 + \cdots + x_n'\mathscr{A}\epsilon_n = \mathscr{A}(x_1'\epsilon_1 + \cdots + x_n'\epsilon_n)\\
\xi \in \mathscr{A}V\\
span(\mathscr{A}\epsilon_1, \cdots, \mathscr{A}\epsilon_n) \in \mathscr{A}V
$$
So, $\mathscr{A}V = span(\mathscr{A}\epsilon_1, \mathscr{A}\epsilon_2, \cdots, \mathscr{A}\epsilon_n)$

**Part 2**

We know:
$$
(\mathscr{A}\epsilon_1, \mathscr{A}\epsilon_2, \cdots, \mathscr{A}\epsilon_n) = \mathscr{A}(\epsilon_1, \epsilon_2, \cdots, \epsilon_n) = (\epsilon_1, \epsilon_2, \cdots, \epsilon_n)A.
$$
Then,
$$
\mathscr{A}V = \text{span}\{ \sum_{i = 1}^{n}a_{i1}\epsilon_i, \sum_{i = 1}^{n}a_{i2}\epsilon_i, \cdots, \sum_{i = 1}^{n}a_{in}\epsilon_i \}
$$
The rank of the set of vectors $\{ \sum_{i = 1}^{n}a_{ij}\epsilon_i \}, j = 1,2,\cdots,n$ equals the column rank of $A$.

So,
$$
\text{rank}(\mathscr{A}) = \text{dim}(\mathscr{A}V) = \text{rank}(A)
$$
Theorem 10 shows that the correspondence between a linear transformation and its matrix representation preserves rank.

Now, let's introduce the most important theorem in this section.

## Th.11

Let $\mathscr{A}$ be a linear transformation for an n-dimensional linear space $V$.

Then we have
$$
\text{dim}(\mathscr{A}) + \text{dim}(\mathscr{A}^{-1}(0)) = n.
$$
Which means the pre-images of a basis for $\mathscr{A}V$, together with a basis for the kernel of $\mathscr{A}$, form a basis for $V$.

### Pf.

Let $\eta_1, \eta_2, \cdots, \eta_r$ be a basis for $\mathscr{A}V$. 

Let their pre-images be $\epsilon_1, \epsilon_2, \cdots, \epsilon_r$, such that $\mathscr{A}\epsilon_i = \eta_i(i = 1,2,\cdots,r)$.

Also, let $\epsilon_{r+1}, \epsilon_{r+2}, \cdots, \epsilon_{s}$ be a basis for $\mathscr{A}^{-1}(0)$.

We now prove that $\epsilon_1, \epsilon_2, \cdots, \epsilon_s$ is a basis for $V$.

First, we need to prove they are linearly independent.

Suppose we have:
$$
l_1\epsilon_1 + \cdots + l_r\epsilon_r + l_{r+1}\epsilon_{r+1} + \cdots + l_s\epsilon_s = 0. \tag1
$$
Apply the $\mathscr{A}$ to the vectors on both sides of $(1)$:
$$
l_1\mathscr{A}\epsilon_1 + \cdots + l_r\mathscr{A}\epsilon_r + \cdots + l_s\mathscr{A}\epsilon_s = \mathscr{A}0 = 0. \tag2 
$$
Since $\epsilon_{r+1}, \cdots, \epsilon_s$ belong to the kernel of $\mathscr{A}$, we have $\mathscr{A}\epsilon_{r+1} = \cdots = \mathscr{A}\epsilon_s = 0$.

Also, $\mathscr{A}\epsilon_i = \eta_i(i = 1,2,\cdots,r)$.

Thus, from $(2)$, we obtain:
$$
l_1\eta_1 + \cdots + l_r\eta_r = 0.
$$
Because $\eta_1, \eta_2, \cdots, \eta_r$ are linearly independent, we have $l_1 = l_2 = \cdots = l_r$.

Substituting this back into equation $(1)$:
$$
l_{r+1}\epsilon_{r+1} + \cdots + l_s\epsilon_s = 0.
$$
Since $\epsilon_{r+1}, \cdots, \epsilon_s$ is a basis for $\mathscr{A}^{-1}(0)$, they are linearly independent, so $l_{r+1} = \cdots = l_s = 0$.

This proves that the set of $\epsilon_1, \cdots, \epsilon_s$ is linearly independent.

Next, we prove that any vector $\alpha$ in $V$ can be linearly represented by $\epsilon_1,\cdots,\epsilon_s$.

Since $\eta_i = \mathscr{A}\epsilon_i$, and $\mathscr{A}\alpha$ is in $\mathscr{A}V$, there exists a set of scalars $l_1, \cdots, l_r$ such that:
$$
\mathscr{A}\alpha = l_1\mathscr{A}\epsilon_1 + \cdots + l_r\mathscr{A}\epsilon_r.
$$
Therefore:
$$
\mathscr{A}(\alpha - l_1\epsilon_1 - \cdots - l_r\epsilon_r) = 0
$$
Which means:
$$
\alpha - l_1\epsilon_1 - \cdots - l_r\epsilon_r \in \mathscr{A}^{-1}(0)
$$
Since $\epsilon_{r+1}, \cdots, \epsilon_s$ is a basis for $\mathscr{A}^{-1}(0)$, there exists a set a scalars $l_{r+1}, \cdots, l_s$ such that:
$$
\alpha - l_1\epsilon_1 - \cdots - l_r\epsilon_r = l_{r+1}\epsilon_{r+1} + \cdots + l_s\epsilon_s.
$$
Thus:
$$
\alpha = l_1\epsilon_1 + \cdots + l_r\epsilon_r + l_{r+1}\epsilon_{r+1} + \cdots + l_s\epsilon_s.
$$
This implies that $\alpha$ is a linear combination of $\epsilon_1, \cdots, \epsilon_s$.

So, $\epsilon_1, \cdots, \epsilon_s$ is a basis for $V$.

Since the dimension of $V$ is $n$, so $s = n$.

And $r$ is the dimension of $\mathscr{A}V$, $s-r = n-r$ is the dimension of $\mathscr{A}^{-1}(0)$.

Finally, we conclude:
$$
\text{dim}(\mathscr{A}) + \text{dim}(\mathscr{A}^{-1}(0)) = n.
$$

According to the theorem, we can easily get a corollary:

## Co.

For a linear transformation on a finite-dimensional linear space, it is injective if and only if it's surjective.

### Pf.

$\Longrightarrow$

Assume $\mathscr{A}$ is injective, which means that only the zero vector will be mapped to zero.

That is, the kernel of $\mathscr{A}$ contains only the zero vector.
$$
\text{dim}(\mathscr{A}^{-1}(0)) = 0.
$$
According to Theorem 11, we get
$$
\text{dim}(\mathscr{A}V) = n - \text{dim}(\mathscr{A}^{-1}(0)) = n - 0 = n = \text{dim}(V).
$$
So,
$$
\mathscr{A}V = V.
$$
Thus, $\mathscr{A}$ is surjective.

$\Longleftarrow$

Suppose $\mathscr{A}$ is surjective. 

Then $\text{dim}(\mathscr{A}V) = n$.

So, the nullity of $\mathscr{A}$ is $\text{dim}(\mathscr{A}^{-1}(0)) = n - \text{dim}(\mathscr{A}V) = 0$.

Since the dimension of the kernel is 0, the kernel contains only the zero vector.

Thus, $\mathscr{A}$ is injective.
