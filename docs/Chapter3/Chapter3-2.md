# Chapter3-2

# n-dimensional vector space

## Definition 2

The n-dimensional vector on the number field P is an ordered array composed of n numbers in the number field P.

$$
(a_1, a_2, \cdots, a_n) \qquad \qquad (1)
$$

$a_{i}$ is called the components of Vector$(1)$.

 

## Definition 3

There are two n-dimensional vectors:

$$
\alpha=(a_1, a_2, \cdots, a_n),\ \beta=(b_1, b_2, \cdots, b_n)
$$

Their corresponding components are equal:

$$
a_i=b_i,\quad i=1,2,\cdots,n.
$$

Then we said the two n-dimensional vectors are equal and are written as $\alpha = \beta$.

 

## Definition 4

The sum of two n-dimensional vectors is written as $\gamma = \alpha + \beta$, which 

$$
\alpha=(a_1, a_2, \cdots, a_n),\ \beta=(b_1, b_2, \cdots, b_n)
$$

$$
\gamma=(a_1+b_1, a_2+b_2, \cdots, a_n+b_n)
$$

Immediately following the definition, we can get

Commutative property：$\alpha+\beta=\beta+\alpha.$

Associative property：$\alpha+(\beta+\gamma)=(\alpha+\beta)+\gamma.$

## Definition 5

A vector with zero components is called a zero vector and is written as $\mathbf{0}$.

$(-a_i, -a_2, \cdots, -a_n )$ is called a negative vector of $\alpha,$ which is written as $-\alpha.$

Obviously, for all vectors $\alpha$, we have:

$$
\alpha+\mathbf{0}=\alpha,\\
\alpha + (-\alpha)=\mathbf{0}.
$$

## Definition 6

$$
\alpha-\beta=\alpha+(-\beta)
$$

## Definition 7

Definition 7 says that k is a number in the number field, and we multiply $\alpha$ by k, then we get:

$$
k\alpha=(ka_1, ka_2, \cdots, ka_n)
$$

This is called the scalar product and is written as $k\alpha.$

From the definition, we can quickly get:

$$
k(\alpha+\beta)=k\alpha+k\beta,\\
(k+l)\alpha = k\alpha+k\beta,\\
k(l\alpha)=(kl)\alpha,\\
1\alpha=\alpha.
$$

These are basic calculation rules.

According to them, we can deduce:

$$
0\alpha=\mathbf{0},\\
(-1)\alpha=-\alpha,\\
k\mathbf{0}=\mathbf{0}.
$$

If $k \neq 0, \alpha \neq \mathbf{0}$, then $k\alpha \neq \mathbf{0}.$

## Definition 8

The set of all n-dimensional vectors whose components are numbers in the number field P, taking into account the addition and scalar multiplication defined on them, is called an n-dimensional linear space over the number field P.

$\alpha=(a_1, a_2, \cdots, a_n)$ is called a row vector, and $\alpha=\left( \begin{array}{}
a_1\\
a_2\\
\vdots\\
a_n
 \end{array} \right)$ is called a column vector.