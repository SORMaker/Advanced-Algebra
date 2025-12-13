# The Rational Canonical Form of Matrix

## Def.8

Let $p(x)$ be a monic polynomial (the coefficient of the highest power is 1) of degree $n$ over a field $\mathbb{F}$:



$$p(x) = x^n + a_{n-1}x^{n-1} + \dots + a_1x + a_0$$

The Companion Matrix associated with $p(x)$, denoted as $A$, is the $n \times n$ square matrix defined as:
$$
A = \begin{bmatrix}

0 & 0 & \dots & 0 & -a_0 \\

1 & 0 & \dots & 0 & -a_1 \\

0 & 1 & \dots & 0 & -a_2 \\

\vdots & \vdots & \ddots & \vdots & \vdots \\

0 & 0 & \dots & 1 & -a_{n-1}

\end{bmatrix} \tag1
$$
 

It's easy to prove that the invariant factors of $A$ are $1,1,\cdots, 1, d(\lambda)$.

## Def.9

We have a block diagonal matrix $A$.
$$
A = \begin{bmatrix}
A_1 & & & \\
& A_2 & & \\
& & \ddots &\\
& & & A_s
\end{bmatrix} \tag2
$$
Where $A_i$ are the Companion matrices of some polynormal $d_i(\lambda)$, and $d_1(\lambda) | d_2(\lambda) | \cdots | d_s(\lambda)$.

Then we say that the matrix $A$ is in Rational Canonical Form.

## Lemma

 The invariant factors of the matrix $A$ in (2) are $1, \cdots, 1, d_1(\lambda), d_2(\lambda), \cdots, d_s(\lambda)$, where the number of $1$s is equal to the sum of the degrees of $d_1(\lambda), d_2(\lambda), \cdots, d_s(\lambda)$ minus $s$.

### Pf.

Consider the characteristic matrix of $A$:
$$
\lambda I - A = \begin{bmatrix} \lambda I_1 - A_1 & & & \\ & \lambda I_2 - A_2 & & \\ & & \ddots & \\ & & & \lambda I_s - A_s \end{bmatrix}
$$
Since the invariant factors of each block $\lambda I_i - A_i$ are $1, \cdots, 1, d_i(\lambda)$, we can use elementary transformations to convert each block into the form:
$$
\begin{bmatrix} 1 & & & \\ & 1 & & \\ & & \ddots & \\ & & & d_i(\lambda) \end{bmatrix}
$$
Consequently, using elementary transformations, we can transform the entire matrix $\lambda I - A$ into:
$$
\begin{bmatrix} 1 & & & & & & & \\ & \ddots & & & & & & \\ & & d_1(\lambda) & & & & & \\ & & & 1 & & & & \\ & & & & \ddots & & & \\ & & & & & d_2(\lambda) & & \\ & & & & & & \ddots & \end{bmatrix} \tag3
$$


Then, using row or column interchanges on the $\lambda$-matrix (3), it can be transformed into:
$$
\begin{bmatrix} 1 & & & & & \\ & 1 & & & & \\ & & \ddots & & & \\ & & & d_1(\lambda) & & \\ & & & & \ddots & \\ & & & & & d_s(\lambda) \end{bmatrix}
$$
Since the condition $d_1(\lambda) \mid d_2(\lambda) \mid \cdots \mid d_s(\lambda)$ holds, this matrix represents the Smith Normal Form of $\lambda I - A$.

Therefore, the invariant factors of $A$ are $1, 1, \cdots, 1, d_1(\lambda), d_2(\lambda), \cdots, d_s(\lambda)$. 

## Th.14

An $n \times n$ square matrix $A$ over a number field $P$ is similar over $P$ to a unique Rational Canonical Form, which is called the Rational Canonical Form of $A$.

### Pf.

Let the invariant factors of $A$ (that is, of $\lambda I - A$) be $1, 1, \dots, 1, d_1(\lambda), d_2(\lambda), \dots, d_s(\lambda)$, where the degree of each $d_1(\lambda), d_2(\lambda), \dots, d_s(\lambda)$ is $\ge 1$, and the number of $1$s is equal to the sum of the degrees of $d_1(\lambda), \dots, d_s(\lambda)$ minus $s$.

Let $B_i$ be the companion matrix of $d_i(\lambda)$. 

Construct the matrix $B$:
$$
B = \begin{bmatrix}

B_1 & & & \\

& B_2 & & \\

& & \ddots & \\

& & & B_s

\end{bmatrix}.
$$
As stated in the Lemma, the invariant factors of $B$ are identical to the invariant factors of $A$; therefore, $B$ is similar to $A$, meaning $B$ is the Rational Canonical Form of $A$.

Furthermore, since $B$ is uniquely determined by the invariant factors of $A$, $B$ is uniquely determined by $A$. 

Reformulating the conclusion of Theorem 14 into the context of linear transformations yields:

## Th.15

Let $\mathscr{A}$ be a linear transformation of an $n$-dimensional linear space over a number field $P$. 

Then, there exists a basis in $V$ such that the matrix of $\mathscr{A}$ relative to this basis is in Rational Canonical Form. 

Furthermore, this Rational Canonical Form is uniquely determined by $\mathscr{A}$ and is called the Rational Canonical Form of $\mathscr{A}$.