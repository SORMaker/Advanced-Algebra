# Uniqueness

If A is congruent to B, then they have the same rank.

A matrix in standard form is a diagonal matrix, and the rank of a diagonal matrix is equal to the number of its non-zero elements on the main diagonal.

Therefore, in the standard form of a quadratic form, the number of square terms with non-zero coefficients is uniquely determined and is independent of the non-degenerate linear substitution used. 

This uniquely determined number is defined as the rank of the quadratic form, which is equal to the rank of its associated matrix.

Over a general field, the standard form of a quadratic form is not unique; it depends on the specific non-degenerate linear substitution that is made.

## Theorem 3

Any complex quadratic form can be reduced to a canonical form by a suitable non-degenerate linear substitution, and the canonical form is unique.

### Proof

Let $f(x_1, x_2, \cdots, x_n)$ be a complex quadratic form.

After a non-degenerate linear substitution, we can transform it to the standard form.

Assuming that its standard form is 
$$
d_1y_1^2 + d_2y_2^2 + \cdots + d_ry_r^2, \quad d_i \neq 0, \quad i=1,2,\cdots,r. \tag{1}
$$
$r$ is the rank of the matrix of $f(x_1, x_2, \cdots, x_n)$.

Since $f(x_1, x_2, \cdots, x_n)$ is a complex quadratic form, then we can make a non-degenerate linear substitution:
$$
\begin{cases}   
y_1 = \frac{1}{\sqrt{d_1}}z_1,\\
\cdots\\
y_r = \frac{1}{\sqrt{d_r}}z_r,\\
y_{r+1} = z_{r+1},\\
\cdots\\
y_n = z_n.
\end{cases}
$$
Then $(1)$ becomes
$$
z_1^2 + z_2^2 + \cdots + z_r^2. \tag{2}
$$
$(3)$ is called the Canonical form.

Any complex sysmmetric matrix is congruent to a diagonal matrix $A$.
$$
A = \begin{bmatrix} 
1 & & & & &\\
& \ddots & & & &\\
& & 1 & & &\\
& & & 0 & &\\
& & & & \ddots &\\
& & & & & 0
\end{bmatrix}
$$
Two complex symmetric matrices are congruent if and only if their ranks are equal.

## Theorem 4(Sylvester's Law of Inertia)

Any real quadratic form can be reduced to a canonical form by a suitable non-degenerate linear substitution, and the canonical form is unique.

### Proof

Part1: how to become a canonical form.

Let $f(x_1, x_2, \cdots, x_n)$ be a real quadratic form.

After a non-degenerate linear substitution, we can get a standard form of $f(x_1, x_2, \cdots, x_n)$.

Suppose that its standard form is 
$$
d_1y_1^2 + \cdots + d_py_p^2 - d_{p+1}y_{p+1}^2 - \cdots - d_ry_r^2, \quad d_i > 0(i=1,2,\cdots,r). \tag{3}
$$
$r$ is the rank of the matrix of $f(x_1, x_2, \cdots, x_n)$.

Then we make a non-degenerated linear substitution as follows 
$$
\begin{cases} 
y_1 = \frac{1}{\sqrt{d_1}}z_1,\\
\cdots\\
y_r = \frac{1}{\sqrt{d_r}}z_r,\\
y_{r+1} = z_{r+1},\\
\cdots\\
y_n = z_n.
\end{cases}
$$
Then $(3)$ becomes 
$$
z_1^2 + \cdots + z_p^2 - z_{p+1}^2 - \cdots - z_r^2. \tag{4}
$$
$(4)$ is called the Canonical form.

Part2: uniqueness

Suppose we have two canonical forms.
$$
X=BY \Rightarrow
f(x_1, x_2, \cdots, x_n) = y_1^2 + \cdots + y_p^2 - y_{p+1}^2 - \cdots - y_r^2,\\
X=CZ \Rightarrow
f(x_1, x_2, \cdots, x_n) = z_1^2 + \cdots + z_q^2 - z_{q+1}^2 - \cdots - z_r^2.
$$
Now we need to prove $p = q$.

We will use the proof by contradiction, suppose $ p > q $.

By the assumption above, we have 
$$
y_1^2 + \cdots + y_p^2 - y_{p+1}^2 - \cdots - y_r^2 = z_1^2 + \cdots + z_q^2 - z_{q+1}^2 - \cdots - z_r^2.
$$
So if we can prove that the left hand is not equal to the right hand, we will get a contradiction, then we can prove $p=q$.

Now the our goal is that we want to find a serise of y, which $y_{p+1}, \cdots, y_n = 0$ and $y_1, \cdots, y_p$ are not all zero, such that $z_1, \cdots, z_q = 0$.

Which means the left hand 
$$
\begin{split}
f(x_1, x_2, \cdots, x_n) 
&= y_1^2 + \cdots + y_p^2 - y_{p+1}^2 - \cdots - y_r^2 \\
&= y_1^2 + \cdots + y_p^2\\
&> 0 
\end{split}
$$
And the right hand
$$
\begin{split}
f(x_1, x_2, \cdots, x_n) 
&= z_1^2 + \cdots + z_q^2 - z_{q+1}^2 - \cdots - z_r^2 \\
&= - z_{q+1}^2 - \cdots - z_r^2 \\
&\leq 0
\end{split}
$$
Since $X=BY, \quad X=CZ$, then we have $Z = C^{-1}BY$.

Suppose $C^{-1}B = G = (g_{ij})$.

We have 
$$
\begin{cases} 
z_1 = g_{11}y_1 + g_{12}y_2 + \cdots + g_{1n}y_n\\
z_2 = g_{21}y_1 + g_{22}y_2 + \cdots + g_{2n}y_n\\
\cdots\\
z_n = g_{n1}y_1 + g_{n2}y_2 + \cdots + g_{nn}y_n
\end{cases}
$$
Let $y_{p+1} = \cdots = y_n = 0$.

Then we have the homogeneous linear system
$$
\begin{cases}
g_{11}y_1 + g_{12}y_2 + \cdots + g_{1p}y_p = 0\\
g_{21}y_1 + g_{22}y_2 + \cdots + g_{2p}y_p = 0\\
\cdots\\
g_{q1}y_1 + g_{q2}y_2 + \cdots + g_{qp}y_p = 0
\end{cases} \tag{1}
$$
If $(1)$ has a nontrivial solution, which means that we find a series of $y$, which $y_1,\cdots,y_p$ are not all zero and $y_{p+1} = \cdots = y_n = 0$, such that $z_1 = \cdots = z_q = 0$.

$(1)$ has $p$ unknowns and $q$ equations, and $ p > q $.

According to the theorem 1 of Chapter3, we have a nontrivial solution.

$ p > q $ does not hold, so $p \leq q$.

Similarly, we can prove $p \geq q$.

So $p = q$.

## Definition 3

In the canonical form of a real quadratic form, the number $p$ of positive square terms is called the positive index of inertia of $f(x_1, x_2, \cdots, x_n)$; the number $r-p$ of negative square terms is called the negative index of inertia of $f(x_1, x_2, \cdots, x_n)$; their difference is called the signature of $f(x_1, x_2, \cdots, x_n)$.



## Theorem 5

1. Any complex matrix of quadratic form is congruent to a diagonal matrix $A$, the number of 1s on the diagonal is r and it is equal to the rank of $A$.  
   $$
   A = \begin{bmatrix} 
   1 & & & & & & & \\
   & 1 & & & & & & \\
   & & \ddots & & & &\\
   & & & 1 & & &\\
   & & & & 0 & &\\
   & & & & & \ddots &\\
   & & & & & & 0
   \end{bmatrix}
   $$

2. Any real matrix of quadratic form is congruent to a diagonal matrix $B$, the number of 1s on the diagonal is p and the number of -1s on the diagonal is $r-p$, and $r$ is the rank of B. $r$ is called the positive index of inertia and $r-p$ is called the negative index of inertia, their difference is called the signature of $B$.
   $$
   B = \begin{bmatrix} 
   1 & & & & & & & \\
   & \ddots & & & & & & \\
   & & 1 & & & &\\
   & & & -1 & & & & & & & \\
   & & & & \ddots & & & & & & \\
   & & & & & -1 & & & &\\
   & & & & & & & 0 & &\\
   & & & & & & & & \ddots &\\
   & & & & & & & & & 0
   \end{bmatrix}
   $$
   



