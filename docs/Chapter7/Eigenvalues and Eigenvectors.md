# Eigenvalues and Eigenvectors

Now, we know that the matrices corresponding to a linear transformation under different bases are similar. 

Then, is it possible to appropriately choose a set of bases such that the matrix of a linear transformation takes the simplest form, and what does this simplest form look like?

Let's look at definition 4.

## Def.4

Let $\mathscr{A}$ be a linear transformation of a linear space $V$ over the field $P$.

If for a number $\lambda_0$ in $P$, there exists a non-zero vector $\xi$, such that
$$
\mathscr{A}\xi = \lambda_0\xi.
$$
Then $\lambda_0$ is called an eigenvalue of $\mathscr{A}$, and $\xi$ is called an eigenvector of $\mathscr{A}$ corresponding to the eigenvalue $\lambda_0$.

We already know what eigenvalues and eigenvectors are, but how do we find them?

Let $V$ be an n-order linear space over a field $P$, $\{\epsilon_i\},\ i = 1,2,\cdots,n$ is a basis for $V$, the matrix of the linear transformation $\mathscr{A}$ with respect to this basis is $A$.

Suppose $\lambda_0$ is an eigenvalue, and the coordinates of its eigenvector $\xi$ under the basis $\{ \epsilon_i \}$ are $x_{01}, x_{02}, \cdots, x_{0n}$.

Then the coordinates of $\mathscr{A}\xi$ is 
$$
A\begin{bmatrix}x_{01}\\x_{02}\\\vdots \\x_{0n} \end{bmatrix}.
$$
The coordinates of $\lambda_0\xi$ is 
$$
\lambda_0\begin{bmatrix}x_{01}\\x_{02}\\ \vdots \\x_{0n} \end{bmatrix}.
$$
According to definition 4, we know $\mathscr{A}\xi = \lambda_0\xi$, so their coordinates equal.
$$
A\begin{bmatrix}x_{01}\\x_{02}\\\vdots \\x_{0n} \end{bmatrix} = \lambda_0\begin{bmatrix}x_{01}\\x_{02}\\ \vdots \\x_{0n} \end{bmatrix}
$$
Rewriten this equation,
$$
(\lambda_0E - A)\begin{bmatrix} x_{01}\\x_{02}\\ \vdots \\x_{0n} \end{bmatrix} = 0.
$$
If we convert this matrix back into a system of linear equations, we get
$$
\begin{cases}
(\lambda_0 - a_{11})x_1 - a_{12}x_2 - \cdots - a_{1n}x_n = 0,\\
-a_{21}x_1 + (\lambda_0 - a_{22})x_2 - \cdots - a_{2n}x_n = 0,\\
\cdots\\
-a_{n1}x_1 - a_{n2}x_2 - \cdots + (\lambda_0 - a_{nn})x_n = 0.
\end{cases}
$$
We know that $\xi$ is not equal to zero vector, its coordinates is not all zero, which means this linear system has non-trivial solution.

We know that a homogeneous system of linear equations has a non-trivial solution if and only if the determinant of its coefficient matrix is zero, this is to say
$$
|\lambda_0 E-A|=\left| \begin{array}{}
\lambda_0-a_{11} & -a_{12} & \cdots & -a_{1n}\\
-a_{21} & \lambda_0-a_{22} & \cdots & -a_{2n}\\
\vdots & \vdots & & \vdots\\
-a_{n1} & -a_{n2} & \cdots & \lambda_0-a_{nn}
\end{array} \right|=0.
$$


Now, let's introduce definition 5.

## Def.5

Let $A$ be an n-order matrix over the field $P$, and let $\lambda$ be an indeterminate.

The determinant of the matrix $\lambda E - A$ is called the characteristic polynomial of $A$, which is a polynomial of degree $n$ over the number field $P$.
$$
|\lambda E-A|=\left| \begin{array}{}
\lambda-a_{11} & -a_{12} & \cdots & -a_{1n}\\
-a_{21} & \lambda-a_{22} & \cdots & -a_{2n}\\
\vdots & \vdots & & \vdots\\
-a_{n1} & -a_{n2} & \cdots & \lambda-a_{nn}
\end{array} \right|
$$
The analysis above shows that if $\lambda_0$ is an eigenvalue of linear transformation $\mathscr{A}$, then $\lambda_0$ is a root of the characteristic polynomial of $A$.

We just defined the characteristic polynomial. The primary use of this polynomial is to find the eigenvalues of $A$, which are simply its roots.

Now, for each of these eigenvalues $\lambda$, we can look at the set of vectors $\alpha$ that satisfy $\mathscr{A}\alpha = \lambda \alpha$. This set, along with the zero vector, forms a crucial subspace called the eigenspace, denoted as
$$
V_{\lambda_0}=\{ \alpha|\mathscr{A}\alpha = \lambda_0\alpha, \alpha \in V \}.
$$
In addition to finding the eigenspaces, the eigenvalues ($\lambda_i$) of a matrix A reveal two of its most fundamental properties: its trace and its determinant.

1. First, the trace of A, denoted tr(A), which is the sum of the diagonal elements, is equal to the sum of all the eigenvalues.
   $$
   tr(A) = \sum_{i=1}^na_{ii} = \sum_{i=1}^n\lambda_i.
   $$
   
2. Second, the determinant of A, denoted det(A), is equal to the product of all the eigenvalues.
   $$
   det(A) = \prod_{i=1}^n\lambda_i.
   $$

According to definition 4, we know that eigenvalues are determined by the linear transformation. 

So, what is the relationship between the characteristic and the linear transformation.

Under different bases, the matrix of a linear transformation is generally different, but these matrices are similar.

Therefore, theorem 6 states:

## Th.6

Similar matrices have the same characteristic polynomial.

### Pf.

Suppose $A \sim B$.

Then we have $B = X^{-1}AX$.

So,
$$
|\lambda E - B| = |\lambda X^{-1}X - X^{-1}AX| = |X^{-1}(\lambda E - A)X| = |X^{-1}||\lambda E - A||X| = |\lambda E - A|.
$$
Theorem 6 implies that the characteristic polynomial of a linear transformation is independent of the basis, so we can rightfully speak of 'the characteristic polynomial of the linear transformation'.

Finally, let's see an important property of character polynomial.

## Hamilton-Cayley Theorem

Let $A$ be an $n \times n$ matrix over field $P$, and $f(\lambda) = |\lambda E - A|$ is the characteristic polynomial of $A$, then we have 
$$
f(A) = A^n - (a_{11} + a_{12} + \cdots + a_{nn})A^{n-1} + \cdots + (-1)^n|A|E = 0.
$$

### Pf.

Let $B(\lambda)$ be the adjugate matrix of $\lambda E - A$, then according to the property of determinant, we know 
$$
B(\lambda)(\lambda E - A) = |\lambda E - A|E = f(\lambda)E.
$$
Since the entries of $B(\lambda)$ are the cofactors of the matrix $(\lambda E - A)$, their degrees are at most $n-1$.

So,
$$
B(\lambda) = \lambda^{n-1}B_0 + \lambda^{n-2}B_1 + \cdots + B_{n-1}.
$$
$B_0,B_1,\cdots, B_{n-1}$ are $n \times n$ matrices.

Suppose $f(\lambda) = \lambda^n + a_1\lambda^{n-1} + \cdots + a_{n-1}\lambda + a_n$, then
$$
f(\lambda)E = \lambda^n E + a_1\lambda^{n-1}E + \cdots + a_nE.
$$
We know 
$$
\begin{aligned}
B(\lambda)(\lambda E - A) &= (\lambda^{n-1}B_0 + \lambda^{n-2}B_1 + \cdots + B_{n-1})(\lambda E - A)\\
&= \lambda^nB_0 + \lambda^{n-1}(B_1 - B_0A) + \lambda^{n-2}(B_2 - B_1A)\\
&\quad + \cdots + \lambda(B_{n-1} - B_{n-2}A) - B_{n-1}A\\
&= f(\lambda)E.
\end{aligned}
$$
So, we have
$$
\begin{cases}
B_0 = E,\\
B_1 - B_0A = a_1E,\\
B_2 - B_1A = a_2E,\\
\cdots\\
B_{n-1} - B_{n-2}A = a_{n-1}E,\\
-B_{n-1}A = a_nE.
\end{cases}
$$
We use $A^{n-i}$ multiply the $i + 1$ equation, we get
$$
\begin{cases}
B_0A^n = EA^n = A^n,\\
B_1A^{n-1} - B_0A^n = a_1EA^{n-1} = a_1A^{n-1},\\
B_2A^{n-2} - B_1A^{n-1} = a_2EA^{n-2} = a_2A^{n-2},\\
\cdots\\
B_{n-1}A - B_{n-2}A^2 = a_{n-1}EA = a_{n-2}A,\\
-B_{n-1}A = a_nE.
\end{cases}
$$
Adding these $n+1$ equations together, the left side becomes zero, and the right side is $f(A)$.

This prove is done.

Because the operations on transformations correspond to the operations on their matrices.

So we have a corollary

## Co.

Let $\mathscr{A}$ be a linear transformation of $V$, $f(\lambda)$ is the characteristic polynomial of $\mathscr{A}$, then $f(\mathscr{A}) = \mathscr{0}$.

