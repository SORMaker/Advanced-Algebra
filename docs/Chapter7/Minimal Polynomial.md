# Minimal Polynomial

## Def.

Let $A$ be an $n \times n$ matrix over a field $P$. If $f(x)$ is a monic polynomial of the least positive degree for which $f(A)=O$, then the polynomial $f(x)$ is called a minimal polynomial of $A$.

## Lemma 1

The minimal polynomial $f(x)$ of $A$ is unique.

### Pf.

Suppose $g_1(x)$ and $g_2(x)$ are all the minimal polynomials of $A$, according to the Euclidean division, 
$$
g_1(x) = q(x)g_2(x) + r(x)
$$
Where $r(x) = 0$ or $\partial(r(x)) < \partial(g_2(x))$, so we have
$$
g_1(A) = q(A)g_2(A) + r(A) = O.
$$
We know $g_1(A) = O$ and $g_2(A) = O$, so $r(A) = O$.

According to the definition of minimal polynomial, $r(x) = 0$, which means $g_2(x)|g_1(x)$.

Similarly, $g_1(x)|g_2(x)$.

$g_1(x)$ and $g_2(x)$ differ only by a non-zero constant factor, and $g_1(x)$, $g_2(x)$ are monic polynomials, so $g_1(x) = g_2(x)$.

## Lemma 2

Let $g(x)$ be a minimal polynomial of $A$, then $A$ is the root of $f(x)$ if and only if $g(x)$ divides $f(x)$.

### Pf.

$\Longrightarrow$

Suppose $f(x) = q(x)g(x) + r(x)$. 

$f(A) = q(A)g(A) + r(A)$, so $r(A) = O$.

Since $deg(r(x)) < deg(g(x))$, $r(x) = 0$.

So $g(x) | f(x)$.

$\Longleftarrow$

If $g(x) | f(x)$, then there exists $h(x)$, such that $f(x)=g(x)h(x)$, so $f(A)=g(A)h(A)=O$.

## Lemma 3

Let $A$ be a diagonal block matrix.
$$
A = \begin{bmatrix} A_1 & & &\\ & A_2 & &\\ & & \ddots &\\ & & & A_s \end{bmatrix}.
$$
Let the minimal polynomial of $A_i$ be $g_i(x)$.

Then the minimal polynomial of $A$ is $[g_1(x),\cdots,g_s(x)]$ (the least common multiple of $g_1(x)$ to $g_s(x)$).

### Pf.

Let $g(x) = [g_1(x), g_2(x), \cdots, g_s(x)]$, then we know $g_i(x)|g(x)$, so $g(A_i) = O$, 
$$
g(A) = 
\begin{bmatrix}
g(A_1) & & & \\
& g(A_2) & &\\
& & \ddots &\\
& & & g(A_s)
\end{bmatrix} = O
$$
The minimal polynomial of $A$ derives $g(x)$.

On the other hand, if $h(A) = 0$, then $h(A_i) = 0$, $g_i(x)|h(x)$.

So $g(x)|h(x)$, which means $deg(g(x))$ is the lowest, so $g(x)$ is the minimal polynomial of $A$.

## Lemma 4

The minimal polynomial of a k-th order Jordan block is $(x-a)^k$.
$$
J = 
\begin{bmatrix} 

a & & &\\
1 & \ddots & & \\
& \ddots & a & \\
& & 1 & a

\end{bmatrix}
$$


### Pf.

The characteristic polynomial of $J$ is $(x-a)^k$.

We know 
$$
J-aE = 
\begin{bmatrix} 
0 & & & \\
1 & \ddots & &\\
& \ddots & 0 &\\
& & 1 & 0
\end{bmatrix}
$$
Then
$$
(J-aE)^{k-1} = 
\begin{bmatrix} 
0\\
\vdots & & O\\
0\\
1 & 0 & \cdots & 0
\end{bmatrix} \neq O,
$$
So the minimal polynomial of $J$ is $(x-a)^k$.

## Th.15

Let $A$ be an $n \times n$ matrix over a field $P$. 

Then $A$ is similar to a diagonal matrix if and only if the minimal polynomial of $A$ is $g(x) = \prod_{i = 1}^l(x-a_i)$.

### Pf.

$\Longrightarrow$

Let $A$ be similar to a diagonal matrix $\text{diag}(a_1, a_2, \cdots, a_n)$. Then the minimal polynomial of each diagonal element $A_i = a_i$ is $(x-a_i)$.

Therefore, the minimal polynomial of $A$ is the product of the distinct coprime factors from the set $\{ (x-a_i) \}_{i=1}^n$.

$\Longleftarrow$

Let $g(x) = \prod_{i=1}^l(x-a_i)$ be the minimal polynomial of $A$.

Since $g(\mathscr{A})V = \{0\}$, according to Theorem 12, we know that:
$$
V = V^{a_1} \oplus \cdots \oplus V^{a_l}
$$
where $V^{a_i}$ is the kernel of $(\mathscr{A} - a_i\mathscr{E})$.

So the union of the bases of $V^{a_i}$ forms a basis for $V$.

These basis vectors are all eigenvectors of $\mathscr{A}$ within each subspace $V^{a_i}$.

Thus, $\mathscr{A}$ has n linearly independent eigenvectors.

By Theorem 7, $A$ is similar to a diagonal matrix.

## Co.

A complex matrix $A$ is similar to a diagonal matrix if and only if its minimal polynomial has distinct roots.
