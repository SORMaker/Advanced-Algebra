# Elementary Divisors

## Def.7

Decompose every invariant factor of a matrix $A$ (or linear transformation $\mathscr{A}$) with degree greater than zero into a product of distinct powers of monic linear factors. All these powers of linear factors (counting multiplicities) are called the elementary divisors of the matrix $A$ (or linear transformation $\mathscr{A}$).

## Th.8

Two complex matrices of the same order are similar if and only if they have the same elementary divisors.

Before we explain how to calculate the elementary divisors.

Let me first introduce a property of polynomial GCDs.

## Pt.

If polynomials $f_1(\lambda),f_2(\lambda)$ are both coprime to $g_1(\lambda), g_2(\lambda)$, then:
$$
(f_1(\lambda)g_1(\lambda), f_2(\lambda)g_2(\lambda)) = (f_1(\lambda),f_2(\lambda)) \cdot (g_1(\lambda),g_2(\lambda)).
$$

### Pf.

Let 
$$
(f_1(\lambda)g_1(\lambda), f_2(\lambda)g_2(\lambda)) = d(\lambda),\\
(f_1(\lambda),f_2(\lambda)) = d_1(\lambda), \qquad (g_1(\lambda), g_2(\lambda)) = d_2(\lambda).
$$
Clearly, $d_1(\lambda) \mid d(\lambda)$ and $d_2(\lambda) \mid d(\lambda)$. 

Since $(f_1(\lambda), g_1(\lambda)) = 1$, it follows that $(d_1(\lambda), d_2(\lambda)) = 1$, and thus $d_1(\lambda)d_2(\lambda) \mid d(\lambda)$. 

On the other hand, since $d(\lambda) \mid f_1(\lambda)g_1(\lambda)$, we can let $d(\lambda) = f(\lambda)g(\lambda)$, where $f(\lambda) \mid f_1(\lambda)$ and $g(\lambda) \mid g_1(\lambda)$. 

Since $(f_1(\lambda), g_2(\lambda)) = 1$, we have $(f(\lambda), g_2(\lambda)) = 1$. 

From $f(\lambda) \mid f_2(\lambda)g_2(\lambda)$, we obtain $f(\lambda) \mid f_2(\lambda)$, and consequently $f(\lambda) \mid d_1(\lambda)$. 

Similarly, $g(\lambda) \mid d_2(\lambda)$. Therefore $d(\lambda) \mid d_1(\lambda)d_2(\lambda)$. Thus, $d(\lambda) = d_1(\lambda)d_2(\lambda)$

## Lemma

Let
$$
A(\lambda) = \begin{pmatrix} f_1(\lambda)g_1(\lambda) & 0 \\ 0 & f_2(\lambda)g_2(\lambda) \end{pmatrix},\\
B(\lambda) = \begin{pmatrix} f_2(\lambda)g_1(\lambda) & 0 \\ 0 & f_1(\lambda)g_2(\lambda) \end{pmatrix}.
$$
If the polynomials $f_1(\lambda)$ and $f_2(\lambda)$ are both coprime to $g_1(\lambda)$ and $g_2(\lambda)$, then $A(\lambda)$ and $B(\lambda)$ are equivalent.

### Pf.

Clearly, $A(\lambda)$ and $B(\lambda)$ share the same determinantal divisor of order 2. The determinantal divisors of order 1 for $A(\lambda)$ and $B(\lambda)$ are , respectively:
$$
d(\lambda) = (f_1(\lambda)g_1(\lambda), f_2(\lambda)g_2(\lambda))
$$
and 
$$
d'(\lambda) = (f_2(\lambda)g_1(\lambda), f_1(\lambda)g_2(\lambda)).
$$
From the preceding discussion, we know that $d(\lambda)$ and $d'(\lambda)$ are equal.

Consequently, $A(\lambda)$ and $B(\lambda)$ also possess the same determinantal divisor of order 1.

Therefore, $A(\lambda)$ and $B(\lambda)$ are equivalent.

## Th.9

If elementary transformations are used to diagonalize the characteristic matrix $\lambda E - A$, and the diagonal elements are factored into products of products of powers of distinct linear factors, then these powers of linear factors constitute all the elementary divisors of $A$.

### Pf.

Assume that $\lambda E - A$ has been reduced by elementary transformations to the diagonal form:
$$
D(\lambda) = \begin{pmatrix} h_1(\lambda) & & & \\ & h_2(\lambda) & & \\ & & \ddots & \\ & & & h_n(\lambda) \end{pmatrix},
$$
where the leading coefficient of each $h_i(\lambda)$ is 1. Factor each $h_i(\lambda)$ into a product of powers of distinct linear factors:
$$
h_i(\lambda) = (\lambda - \lambda_1)^{k_{i1}}(\lambda - \lambda_2)^{k_{i2}}\dots(\lambda - \lambda_r)^{k_{ir}}, \quad i=1, 2, \dots, n.
$$
We must prove that for each distinct linear factor $(\lambda - \lambda_j)$, if we arrange its powers $(\lambda - \lambda_j)^{k_{1j}}, (\lambda - \lambda_j)^{k_{2j}}, \dots, (\lambda - \lambda_j)^{k_{nj}}(j=1, 2, \dots, r) $ in ascending order of degree along the main diagonal of $D(\lambda)$, the resulting new diagonal matrix $D'(\lambda)$ is equivalent to $D(\lambda)$. 

In this case, $D'(\lambda)$ is the Smith Normal Form of $\lambda E - A$, and all $(\lambda - \lambda_j)^{k_{ij}}$ not equal to 1 are the elementary divisors of $A$.

For convenience, we first discuss the powers of $\lambda - \lambda_1$. 

Let
$$
g_i(\lambda) = (\lambda - \lambda_2)^{k_{i2}}(\lambda - \lambda_3)^{k_{i3}}\dots(\lambda - \lambda_r)^{k_{ir}}, \quad i=1, 2, \dots, n.
$$
Thus,
$$
h_i(\lambda) = (\lambda - \lambda_1)^{k_{i1}}g_i(\lambda), \quad i=1, 2, \dots, n.
$$
Furthermore, each $(\lambda - \lambda_1)^{k_{i1}}$ is coprime to $g_j(\lambda)$ (for $j=1, 2, \dots, n$). If there exists an adjacent pair of exponents such that $k_{i,1} > k_{i+1, 1}$, we swap the positions of $(\lambda - \lambda_1)^{k_{i1}}$ and $(\lambda - \lambda_1)^{k_{i+1,1}}$ in $D(\lambda)$ while keeping the other factors unchanged.

According to the Lemma,
$$
\begin{pmatrix} (\lambda-\lambda_1)^{k_{i1}}g_i(\lambda) & 0 \\ 0 & (\lambda-\lambda_1)^{k_{i+1,1}}g_{i+1}(\lambda) \end{pmatrix}
$$
is equivalent to
$$
\begin{pmatrix} (\lambda-\lambda_1)^{k_{i+1,1}}g_i(\lambda) & 0 \\ 0 & (\lambda-\lambda_1)^{k_{i1}}g_{i+1}(\lambda) \end{pmatrix}.
$$
Consequently, $D(\lambda)$ is equivalent to the diagonal matrix
$$
D_1(\lambda) = \begin{pmatrix} (\lambda-\lambda_1)^{k_{11}}g_1(\lambda) & & & & \\ & \ddots & & & \\ & & (\lambda-\lambda_1)^{k_{i+1,1}}g_i(\lambda) & & \\ & & & (\lambda-\lambda_1)^{k_{i1}}g_{i+1}(\lambda) & \\ & & & & \ddots & \\ & & & & & (\lambda-\lambda_1)^{k_{n1}}g_n(\lambda) \end{pmatrix}.
$$
We then apply the same discussion to $D_1(\lambda)$. 

Continuing this process until the powers of $\lambda - \lambda_1$ contained in the diagonal elements are arranged in ascending order of degree. 

Treating $\lambda - \lambda_2, \dots, \lambda - \lambda_r$ in the same manner, we finally obtain a diagonal matrix $D'(\lambda)$ equivalent to $D(\lambda)$, in which the powers of every identical linear factor on the main diagonal are arranged in ascending order of degree.
