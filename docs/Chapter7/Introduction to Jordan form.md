# Introduction to Jordan form

First, let's introduce the Jordan form.

Before we begin, I would like to note that the following discussion is limited to the complex field of mathematics.

## Def.9

Jordan block is 
$$
J(\lambda_0, k) = 
\begin{bmatrix}
\lambda_0 & 0 & 0 & \cdots & 0 & 0 & 0\\
1 & \lambda_0 & 0 & \cdots & 0 & 0 & 0\\
\vdots & \vdots & \vdots & & \vdots & \vdots & \vdots\\
0 & 0 & 0 & \cdots & 1 & \lambda_0 & 0\\
0 & 0 & 0 & \cdots & 0 & 1 & \lambda_0
\end{bmatrix}
$$
which $\lambda_0$ is a complex number.

If the block diagonal matrix $A$ is composed of some Jordan block, then $A$ is called the Jordan canonical form.
$$
A = 
\begin{bmatrix} 

J(\lambda_1, k_1) & & &\\
& J(\lambda_2, k_2) & & \\
& & \ddots &\\
& & & J(\lambda_s, k_s)

\end{bmatrix}
$$

## Lemma

Let $\mathscr{B}$ be the linear transformation of an n-dimensional linear space $V$.

And we have $\mathscr{B}^k = \mathscr{0}$, $k \in \Z^+$. (positive integer)

Then $\mathscr{B}$ is called a nilpotent linear transformation.

For the nilpotent linear transformation $\mathscr{B}$, we have a set of bases $(\alpha_1, \mathscr{B}\alpha_1, \cdots, \mathscr{B}^{k_1 - 1}\alpha_1, \alpha_2, \cdots, \mathscr{B}^{k_2-1}\alpha_2, \cdots, \mathscr{B}^{k_s-1}\alpha_s)$, where $\mathscr{B}^{k_i}\alpha_i = \mathscr{0}$, such that the matrix of $\mathscr{B}$ under the basis is 
$$
B = \begin{pmatrix}
  % First Block (k_1)
  \underbrace{
    \begin{matrix}
      0 & & & \\
      1 & 0 & & \\
      & \ddots & \ddots & \\
      & & 1 & 0
    \end{matrix}
  }_{k_1}\\
  
  % Second Block (k_2) and the zero to its left
   & \underbrace{
    \begin{matrix}
      0 & & & \\
      1 & 0 & & \\
      & \ddots & \ddots & \\
      & & 1 & 0
    \end{matrix}
  }_{k_2} \\
  & & \ddots\\
  % Last Block (k_s) and the zero above it
   & & & \underbrace{
    \begin{matrix}
      0 & & & \\
      1 & 0 & & \\
      & \ddots & \ddots & \\
      & & 1 & 0
    \end{matrix}
  }_{k_s}
\end{pmatrix}
$$

### Pf.

We proceed by induction on the dimension n of the linear space $V$.

When $n=1$. 

Suppose $\alpha_1$ is a basis of $V$, $\mathscr{B}\alpha_1 = \lambda_1\alpha_1$.

$\mathscr{B}$ is a  nilpotent linear transformation, then we have $\mathscr{B}^{k}\alpha_1 = \lambda_1\alpha_1 = 0$, so $\lambda_1 = 0$.

So $\mathscr{B}\alpha = \lambda_1\alpha = 0$, the lemma is true.

Suppose the $dim(V) \lt n$, the lemma is true.

If $\mathscr{B}V = V$, then $dim(\mathscr{B}V) = n$. 

According to the lemma, $dim(\mathscr{B}^{k}V) = dim(\mathscr{B}^{k-1}(\mathscr{B}V)) = dim(\mathscr{B}^{k-1}(V)) = \cdots = dim(V) = 0$.

There is a contradiction.

So $dim(\mathscr{B}V) < n$.

By Theorem 11, the pre-image of the basis of $\mathscr{B}V$ plus the basis of the kernel of $\mathscr{B}$ is the basis of $V$.

Since $dim(\mathscr{B}V) < n$, then there exists a set of basis of $\mathscr{B}V$.
$$
\epsilon_1, \mathscr{B}\epsilon_1, \cdots, \mathscr{B}^{k_1 - 1}\epsilon_1, \cdots, \mathscr{B}\epsilon_t, \cdots, \mathscr{B}^{k_t - 1}\epsilon_t.
$$
Their inverse image is
$$
\alpha_1, \mathscr{B}\alpha_1, \cdots, \mathscr{B}^{k_1 - 1}\alpha_1, \cdots, \mathscr{B}\alpha_t, \cdots, \mathscr{B}^{k_t - 1}\alpha_t.
$$
We know $\mathscr{B}\alpha_i = \epsilon_i$, $\mathscr{B}^{k_i}\epsilon_i = 0$.

So $\mathscr{B}^{k_i}(\mathscr{B}\alpha_i) = \mathscr{0} \Rightarrow \mathscr{B}(\mathscr{B}^{k_i}\alpha_i) = \mathscr{0}$.

So $\mathscr{B}^{k_i}\alpha_i \in \mathscr{B}^{-1}(0)$.

We know $\mathscr{B}^{k_i - 1}\epsilon_i$ are linearly independent.

So $\mathscr{B}^{k_i}\alpha_i$ are linearly independent.

Thus, $\mathscr{B}^{k_i}\alpha_i$ can be extended to a basis for $\mathscr{B}^{-1}(0)$.

Then we have $\mathscr{B}^{k_1}\alpha_1, \cdots \mathscr{B}^{k_t}\alpha_t, \alpha_{t+1}, \cdots, \alpha_s$.

So 
$$
\alpha_1, \mathscr{B}\alpha_1, \cdots, \mathscr{B}^{k_1 - 1}\alpha_1, \cdots, \mathscr{B}\alpha_t, \cdots, \mathscr{B}^{k_t - 1}\alpha_t,\mathscr{B}^{k_1}\alpha_1, \cdots \mathscr{B}^{k_t}\alpha_t, \alpha_{t+1}, \cdots, \alpha_s.
$$
is a basis for $V$.

The lemma is true.

## Th.13

Let $\mathscr{A}$ be a linear transformation of an n-dimensional linear space $V$ over the complex field.

Then there exists a set of bases in $V$ such that the matrix of $\mathscr{A}$ under the basis is a Jordan matrix, and we call it the Jordan normal form of $\mathscr{A}$.

### Pf.

Let the characteristic polynomial of $\mathscr{A}$ is $f(\lambda) = (\lambda - \lambda_1)^{r_1}(\lambda - \lambda_2)^{r_2}\cdots(\lambda - \lambda_s)^{r_s}$.

According to Theorem 12, we know that $V$ can be decomposed into the direct sum of $\mathscr{A}$-subspaces.
$$
V = \sum_{i=1}^{s}\oplus V^{\lambda_i},\quad V^{\lambda_i} = \{ \xi \in V | (\mathscr{A} - \lambda_i \mathscr{E})^{r_i}\xi = 0 \}.
$$
Let $\mathscr{B} = (\mathscr{A} - \lambda_i\mathscr{E})|V_i$, then $\mathscr{B}^{r_i} = \mathscr{0}$.

According to Lemma, we know that there exists a set of bases over $V^{\lambda_i}$, such that the matrix of $\mathscr{B}$ is 
$$
\begin{bmatrix} 
J(0,r_{i_1}) & & &\\
& J(0,r_{i_2}) & & \\
& & \ddots &\\
& & & J(0,r_{i_{s_i}})
\end{bmatrix}
$$
Then the matrix of $\mathscr{A}|V^{\lambda_i} = \mathscr{B} + \lambda_i\mathscr{E}|V^{\lambda_i}$ is
$$
\begin{bmatrix}
J(\lambda_i, r_{i_1}) & & & \\
& J(\lambda_i, r_{i_2}) & & \\
& & \ddots &\\
& & & J(\lambda_i, r_{i_{s_i}})
\end{bmatrix}
$$
We combined the bases from each $V^{\lambda_i}$.

Then they form a basis for the linear space $V$, and the matrix of $\mathscr{A}$ under this basis is the Jordan Canonical Form.

