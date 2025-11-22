# Calculation of Linear Transformation

> We know what linear transformations are. It's natural to discuss what operations can be performed on these transformations themselves.
>
> First, let's define the product of a linear transformation.

## Def.1.1

Let $\mathscr{A},\mathscr{B}$ be two linear transformations of a linear space $V$, the product of $\mathscr{A},\mathscr{B}$ is defined as:
$$
\mathscr{AB}(\alpha) = \mathscr{A}(\mathscr{B}(\alpha)), \quad \alpha \in V.
$$

## Pt.1.1

It is easy to know that the product of two linear transformations is still a linear transformation.

### Pf.

$$
\begin{aligned}
(\mathscr{AB})(\alpha + \beta) &= \mathscr{A}(\mathscr{B}(\alpha + \beta))\\ 
&= \mathscr{A}(\mathscr{B}(\alpha) + \mathscr{B}(\beta))\\ 
&= \mathscr{A}(\mathscr{B}(\alpha)) + \mathscr{A}(\mathscr{B}(\beta))\\
&= (\mathscr{AB})(\alpha) + (\mathscr{AB})(\beta)\\
(\mathscr{AB})(k\alpha) &= \mathscr{A}(\mathscr{B}(k\alpha)) \\
&= \mathscr{A}(k\mathscr{B}(\alpha))\\
&= k\mathscr{A}(\mathscr{B}(\alpha))\\
&= k(\mathscr{AB})(\alpha)
\end{aligned}
$$

Furthermore, this multiplication satisfies the Associative Law: $(\mathscr{AB})\mathscr{C} = \mathscr{A}(\mathscr{BC})$.

However, it does not satisfy the Commutative Law, $\mathscr{AB}$ is generally not equal to $\mathscr{BA}$.

> Besides multiplication, we can also add them.

## Def.1.2

Let $\mathscr{A,B}$ be two linear transformations of a linear space $V$, the sum of them is defined as:
$$
(\mathscr{A + B})(\alpha) = \mathscr{A}(\alpha) + \mathscr{B}(\alpha), \quad \alpha \in V.
$$

## Pt.

Likewise, the sum of two linear transformations is still a linear transformation.

### Pf.

$$
\begin{aligned}
(\mathscr{A} + \mathscr{B})(\alpha + \beta) &= \mathscr{A}(\alpha + \beta) + \mathscr{B}(\alpha + \beta)\\
&= (\mathscr{A}(\alpha) + \mathscr{A}(\beta)) + (\mathscr{B}(\alpha) + \mathscr{B}(\beta))\\
&= (\mathscr{A}(\alpha) + \mathscr{B}(\alpha)) + (\mathscr{A}(\beta) + \mathscr{B}(\beta))\\
&= (\mathscr{A} + \mathscr{B})(\alpha) + (\mathscr{A} + \mathscr{B})(\beta)\\
(\mathscr{A} + \mathscr{B})(k\alpha) &= \mathscr{A}(k\alpha) + \mathscr{B}(k\alpha)\\
&= k\mathscr{A}(\alpha) + k\mathscr{B}(\alpha)\\
&= k(\mathscr{A}(\alpha) + \mathscr{B}(\alpha))\\
&= k(\mathscr{A} + \mathscr{B})(\alpha)
\end{aligned}
$$

> Finally, let's look at scalar multiplication.

Using the multiplication of the linear transformation, we can define the scalar multiplication of a number in the field $P$ and the linear transformation.
$$
k\mathscr{A} = \mathscr{KA}.
$$
Which means:
$$
(k\mathscr{A})(\alpha) = \mathscr{K}(\mathscr{A}(\alpha)) = \mathscr{KA}(\alpha).
$$

> We have just defined addition and scalar multiplication for linear transformations. 

Then, according to their properties, we know all linear transformations on the linear space $V$ also constitute a linear space on the field $P$.

> We have defined multiplication, so naturally, we think about 'division', which is the inverse transformation.

## Def.1.3

Let $\mathscr{A}$ be a linear transformation from $V$ to $V'$. If $\mathscr{A}$ is a bijection, then its inverse mapping $\mathscr{A}^{-1}$ exists, and $\mathscr{A}^{-1}$ is also a linear transformation. 

$\mathscr{A}^{-1}$ is called the inverse transformation of $\mathscr{A}$.

It satisfies $\mathscr{A}\mathscr{A}^{-1} = \mathscr{A}^{-1}\mathscr{A} = \mathscr{E}$.

## Pt.

Furthermore, if a linear transformation $\mathscr{A}$ is invertible, then its inverse mapping $\mathscr{A}^{-1}$ is also a linear transformation.

## Pf.

$$
\begin{aligned}
\mathscr{A}^{-1}(\alpha + \beta) &= \mathscr{A}^{-1}[(\mathscr{A}\mathscr{A}^{-1})(\alpha) + (\mathscr{A}\mathscr{A}^{-1})(\beta)]\\
&= \mathscr{A}^{-1}[\mathscr{A}(\mathscr{A}^{-1}(\alpha)) + \mathscr{A}(\mathscr{A}^{-1}(\beta))]\\
&= \mathscr{A}^{-1}[\mathscr{A}(\mathscr{A}^{-1}(\alpha) + \mathscr{A}^{-1}(\beta))]\\
&= (\mathscr{A}^{-1}\mathscr{A})(\mathscr{A}^{-1}(\alpha) + \mathscr{A}^{-1}(\beta))\\
&= \mathscr{A}^{-1}(\alpha) + \mathscr{A}^{-1}(\beta)\\
\mathscr{A}^{-1}(k\alpha) &= \mathscr{A}^{-1}(k(\mathscr{A}\mathscr{A}^{-1})(\alpha))\\
&= \mathscr{A}^{-1}(k(\mathscr{A}(\mathscr{A}^{-1}(\alpha))))\\
&= \mathscr{A}^{-1}(\mathscr{A}(k\mathscr{A}^{-1}(\alpha)))\\
&= (\mathscr{A}^{-1}\mathscr{A})(k\mathscr{A}^{-1}(\alpha))\\
&= k\mathscr{A}^{-1}(\alpha)
\end{aligned}
$$

> Finally, let's discuss the Powers of a linear transformation and the Polynomials of a linear transformation.

## Def.1.4

The k-th power $\mathscr{A}^{k}$ is just $\mathscr{A}$ applied $k$ times. Furthermore, we define $\mathscr{A}^0$ to be the identity transformation $\mathscr{E}$.

Once we have powers, we can define polynomials of a linear transformation.
$$
f(\mathscr{A}) = a_m\mathscr{A}^m + a_{m-1}\mathscr{A}^{m-1} + \cdots + a_0\mathscr{E}.
$$
It is not difficult to verify that if in the polynomial ring $P[x]$,
$$
h(x) = f(x) + g(x), \quad p(x) = f(x)g(x).
$$
Then for the linear transformations,
$$
h(\mathscr{A}) = f(\mathscr{A}) + g(\mathscr{A}), \quad h(\mathscr{A}) = f(\mathscr{A})g(\mathscr{A}).
$$
In particular,
$$
f(\mathscr{A})g(\mathscr{A}) = g(\mathscr{A})f(\mathscr{A})
$$
