# Linear Dependence

## Definition 9

The vector $\alpha$  is called a linear combination of the set of vectors $\beta_1, \beta_2, \cdots, \beta_s$, If there are $k_1,k_2,\cdots,k_s$ in the number field P that satisfy:

$$
\alpha=\beta_1+\beta_2+\cdots+\beta_s.
$$

For any n-dimension vector $\alpha=(a_1,a_2,\cdots,a_n)$ is a linear combination of the set of vectors:

$$
\left\{ \begin{array}{} 
\varepsilon_1=(1,0,\cdots,0),\\
\varepsilon_2=(0,1,\cdots,0),\\
\cdots\\
\varepsilon_n=(0,0,\cdots,1)
\end{array} \right.
$$

Because $\alpha=a_1\varepsilon_1+a_2\varepsilon_2+\cdots+a_n\varepsilon_n.$

The vectors $\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n$ are called n-dimensional unit vectors.

## Definition 10

If any vector $\alpha_i(i=1,2,\cdots,t)$ in a set of vectors $\alpha_1,\alpha_2,\cdots,\alpha_t$ can be linearly represented by a set of vectors $\beta_1,\beta_2,\cdots,\beta_s$, then the set of vectors $\alpha_1,\alpha_2,\cdots,\alpha_t$ is said to be linearly representable by the set of vectors $\beta_1,\beta_2,\cdots,\beta_s$. If two sets of vectors can be linearly represented with each other, then they are called equivalent.

So we can get three properties according to the equivalent of the set of vectors:

- Reflexivity： each set of vectors is equivalent to itself.
- Symmetry: If the set of vectors $\alpha_i$ is equivalent to $\beta_i$, then the set of vectors $\beta_i$ is equivalent to $\alpha_i$, either.     
- Transitivity: If the set of vectors $\alpha_i$  is equivalent to $\beta_i$ and $\beta_i$ is equivalent to $\gamma_i$, then $\alpha_i$ is equivalent to $\gamma_i$.

Let’s give a quick proof about transitivity:

$$
\begin{aligned}
\alpha_i = \sum_{j=1}^{s}k_{ij}\beta_{j}, \quad i=1,2,\cdots,t.\\
\beta_i = \sum_{m=1}^{p}l_{jm}\gamma_{m}, \quad j=1,2,\cdots,s.
\end{aligned}
$$

So:

$$
\alpha_i=\sum_{j=1}^{s}k_{ij}\sum_{m=1}^{p}l_{jm}\gamma_{m}=\sum_{m=1}^{p}(\sum_{j=1}^{s}k_{ij}l_{jm})\gamma_m,i=1,2,\cdots,t.
$$

It’s true for another case.

## Definition 11

If there is a vector in the set of vectors $\alpha_1, \alpha_2,\cdots,\alpha_s(s\geq2)$ that the rest of the vectors can linearly represent, then the set of vectors $\alpha_1, \alpha_2,\cdots,\alpha_s(s\geq2)$ is called linearly dependent.

 

## Definition 11’

A set of vectors is called linearly dependent if there are numbers $k_1,k_2,\cdots,k_s$ which are not all zero in the field P, such that:

$$
k_1\alpha_1+k_2\alpha_2+\cdots+k_s\alpha_s=0
$$

Now, let’s prove the two definitions above are equivalent.

$\Longrightarrow:$

When $s\geq2$, according to Definition 11, we know:

$$
\alpha_s=k_1\alpha_1+k_2\alpha_2+\cdots+k_{s-1}\alpha_{s-1}.
$$

Rewrite the formula:

$$
k_1\alpha_1+k_2\alpha_2+\cdots+k_{s-1}\alpha_{s-1} + (-1)\alpha_s=0.
$$

Because $k_1, k_2,\cdots,k_{s-1},-1$ are not all zero, at least $(-1)\neq 0$.

So, according to definition 11’, this set of vectors is linearly dependent.

$\Longleftarrow:$

According to definition 11’, we have:

$$
k_1\alpha_1 + k_2\alpha_2 + \cdots + k_s\alpha_s=0.
$$

$k_1,k_2,\cdots,k_s$ are not all zero.

Assume that $k_s \neq 0$. So, we can rewrite the above formula:

$$
\alpha_s=-\frac{k_1}{k_s}\alpha_1 - \frac{k_2}{k_s}\alpha_2 - \cdots - \frac{k_{s-1}}{k_s}\alpha_{s-1}.
$$

According to definition 11, this set of vectors is linearly dependent. 

## Definition 12

If we can infer $k_1=k_2=\cdots=k_s=0$ from $k_1\alpha_1 + k_2\alpha_2 + \cdots + k_s\alpha_s=0$, then we say that set of vectors $\alpha_1,\alpha_2,\cdots,\alpha_s$ is linearly independent.

Now, we have introduced a lot of definitions. But we still don’t know how to judge whether a set of vectors is linearly dependent.

So, how?

According to definition 11’, if the set of vectors is linearly dependent, we need to find a series of k that are not all zero.

We need to see whether equation $x_1\alpha_1 + x_2\alpha_2 + \cdots + x_s\alpha_s=0$ has a non-zero solution.

$$
\left\{ \begin{array}{} 
a_{11}x_1 + a_{21}x_2 + \cdots + a_{s1}x_s = 0,\\
a_{12}x_1 + a_{22}x_2 + \cdots + a_{s2}x_s = 0,\\
\cdots\\
a_{1n}x_1 + a_{2n}x_2 + \cdots + a_{sn}x_s = 0.\\

\end{array} \right.\tag{1}
$$

So, the necessary and sufficient condition for the set of vectors $\alpha_1,\alpha_2,\cdots,\alpha_s$ to be linearly independent is that the homogeneous linear equation system has only non-zero solutions.

We can also use this form to draw the other conclusion. 

If we have a linearly independent n-dimensional set of vectors $\beta_i=(b_{i1}, b_{i2}, \cdots, b_{in}),i=1,2,\cdots,s$, then adding a component to each vector to get the n+1-dimensional set of vectors $\beta_i=(b_{i1}, b_{i2}, \cdots, b_{in},b_{i,n+1}),i=1,2,\cdots,s$ is linearly independent.

According to the n+1-dimensional set of vectors, we have n+1 equations:

$$
\left\{ \begin{array}{} 
a_{11}x_1 + a_{21}x_2 + \cdots + a_{s1}x_s = 0,\\
a_{12}x_1 + a_{22}x_2 + \cdots + a_{s2}x_s = 0,\\
\cdots\\
a_{1n}x_1 + a_{2n}x_2 + \cdots + a_{sn}x_s = 0,\\
a_{1,n+1}x_1 + a_{2,n+1}x_2 + \cdots + a_{s,n+1}x_s=0.
\end{array} \right.\tag{2}
$$

Obviously, if the linear equations system $(1)$ only has a zero solution, then the linear equations system  $(2)$﻿  only has a zero solution.

## Theorem 2

We have two sets of vectors $\alpha_i$ and $\beta_i$.

If:

- Set of vectors $\alpha_i$ can be linearly represented by $\beta_i$.
- $r > s$

Then the set of vectors $\alpha_i$ must be linearly dependent.

## Corollary 1

If the set of vectors $\alpha_i$ can be linearly represented by $\beta_i$, and set of vectors $\alpha_i$ is linearly independent, then $r \leq s$.

## Corollary 2

Any n+1 n-dimensional vectors are linearly dependent.

## Corollary 3

Two linearly independent and equivalent sets of vectors must contain the same number of vectors.

## Definition 13

A subset of a set of vectors is called a maximal linearly independent set if the subset itself is linearly independent and if any vector is added to the subset, the resulting subset is linearly dependent.

### Basic property:

Any maximal linearly independent set is equivalent to the set of vectors itself.

## Theorem 3

All maximal linearly independent subsets of a set of vectors have the same number of vectors.

## Definition 14

The rank of a set of vectors is defined as the number of vectors in any maximal linearly independent subsets.

Since a linearly independent set of vectors is its own maximal linearly independent subset, it follows that a set of vectors is linearly independent if and only if its rank is equal to the number of vectors it contains.
