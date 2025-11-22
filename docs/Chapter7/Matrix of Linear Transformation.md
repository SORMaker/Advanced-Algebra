# Matrix of Linear Transformation

> Now, let's establish the relationship between the matrix and the linear transformation.

Let $V$ be an n-dimensional linear space, and $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ is a basis for $V$.

Then any vector $\xi$ can be linearly represented by $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$:
$$
\xi = x_1\epsilon_1 + x_2\epsilon_2 + \cdots + x_n\epsilon_n.
$$
The linear transformation maintains the linear relationship, so between the image of $\xi$, $\mathscr{A}\xi$, and the basis of the image $\mathscr{A}\epsilon_1, \mathscr{A}\epsilon_2, \cdots, \mathscr{A}\epsilon_n$ must have the same relationship:
$$
\begin{aligned}
\mathscr{A}\xi &= \mathscr{A}(x_1\epsilon_1 + x_2\epsilon_2 + \cdots + x_n\epsilon_n)\\ 
&= x_1\mathscr{A}\epsilon_1 + x_2\mathscr{A}\epsilon_2 + \cdots + x_n\mathscr{A}\epsilon_n.
\end{aligned}
$$
The above equation shows that if we know the images of the basis vectors $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$, then we know the image of any vector in the linear space.

In other words,

## Pt.0.1

Let $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ be a basis of a linear space $V$. 

If the linear transformation $\mathscr{A}$ and $\mathscr{B}$ have the same effect on this basis,

### Pf

The meaning of $\mathscr{A}$ being equal to $\mathscr{B}$ is that they have the same action on each vector.

So we want to prove that for any vector $\xi$, the equality $\mathscr{A}\xi = \mathscr{B}\xi$ holds.

We know:
$$
\begin{aligned}
\mathscr{A}\xi &= x_1\mathscr{A}\epsilon_1 + x_2\mathscr{A}\epsilon_2 + \cdots + x_n\mathscr{A}\epsilon_n \\
&= x_1\mathscr{B}\epsilon_1 + x_2\mathscr{B}\epsilon_2 + \cdots + x_n\mathscr{B}\epsilon_n\\
&= \mathscr{B}\xi.
\end{aligned}
$$
The meaning of property 0.1 is that a linear transformation is entirely determined by its images on a basis.

Furthermore, we point out that the images of the basis vectors are random.

## Pt.0.2

Let $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ is a basis of a linear space $V$, for any set of vectors $\alpha_1, \alpha_2, \cdots, \alpha_n$, we have a linear transformation $\mathscr{A}$, such that:
$$
\mathscr{A}\epsilon_i = \alpha_i, \quad i = 1,2,\cdots,n.
$$

### Pf.

Let
$$
\xi = \sum_{i=1}^nx_i\epsilon_i.
$$
is any vector of a linear space $V$, then we define the linear transformation of $V$ is $\mathscr{A}$:
$$
\mathscr{A}\xi = \sum_{i=1}^nx_i\alpha_i.
$$
Now, let's prove the transformation $\mathscr{A}$ is linear.

Take any two vectors in $V$:
$$
\beta = \sum_{i=1}^nb_i\epsilon_i, \quad \gamma = \sum_{i=1}^nc_i\epsilon_i.
$$
then, 
$$
\beta + \gamma = \sum_{i=1}^n(b_i + c_i)\epsilon_i, \quad k\beta = \sum_{i=1}^nkb_i\epsilon_i, \quad k \in P.
$$
Applying the linear transformation $\mathscr{A}$ to both sides of the equation, we get:
$$
\begin{aligned}
\mathscr{A}(\beta + \gamma) &= \sum_{i=1}^n(b_i + c_i)\alpha_i\\
&= \sum_{i=1}^nb_i\alpha_i + \sum_{i=1}^nc_i\alpha_i\\
&= \mathscr{A}\beta + \mathscr{A}\gamma,\\
\mathscr{A}(k\beta) &= \sum_{i=1}^n(kb_i\alpha_i)\\
&= k\sum_{i=1}^n(b_i\alpha_i)\\
&= k\mathscr{A}\beta.
\end{aligned}
$$
So, $\mathscr{A}$ is a linear transformation.
$$
\epsilon_i = 0\epsilon_1 + \cdots + 1\epsilon_i + 0\epsilon_{i+1} + \cdots + 0\epsilon_n, \quad i = 1,2,\cdots,n.
$$
So, we know:
$$
\mathscr{A}\epsilon_i = 0\alpha_1 + \cdots + 1\alpha_i + 0\alpha_{i+1} + \cdots + 0\alpha_n, \quad i = 1,2,\cdots,n.
$$
Q.E.D.

According to the property 0.1 and 0.2, we get the Theorem 1.

## Th.1

Let $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ be a basis for a linear space $V$, $\alpha_1, \alpha_2, \cdots, \alpha_n$ are any $n$ vectors in $V$. 

Then there exists the unique linear transformation $\mathscr{A}$, such that:
$$
\mathscr{A}\epsilon_i = \alpha_i, \quad i = 1,2,\cdots,n.
$$

## Def.2

Let $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ be a basis for an n-dimensional linear space $V$ over the field $P$, $\mathscr{A}$ is a linear transformation in $V$.

Then the image of a basis for $V$ can be linearly represented by the basis.
$$
\begin{cases}
\mathscr{A}\epsilon_1 = a_{11}\epsilon_1 + a_{21}\epsilon_2 + \cdots + a_{n1}\epsilon_n,\\
\mathscr{A}\epsilon_1 = a_{11}\epsilon_1 + a_{21}\epsilon_2 + \cdots + a_{n1}\epsilon_n,\\
\cdots\\
\mathscr{A}\epsilon_1 = a_{11}\epsilon_1 + a_{21}\epsilon_2 + \cdots + a_{n1}\epsilon_n,\\
\end{cases}
$$
In matrix form, this is:
$$
\mathscr{A}(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n) = (\mathscr{A}\epsilon_1, \mathscr{A}\epsilon_2, \cdots, \mathscr{A}\epsilon_n)=(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)A
$$
Where,
$$
A = \begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn}\\
\end{bmatrix}
$$
The matrix $A$ is called the matrix of the linear transformation $\mathscr{A}$ respect to the basis $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$.

After establishing the one-to-one correspondence between the linear transformation and the matrix.

Next, we will study the relationship between the operations of linear transformations and the operations of their matrices.

## Th.2

Let $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ be a basis for an n-dimensional linear space $V$ over the field $P$.

Under the basis, each linear transformation corresponds to an $n \times n$ matrix. 

This correspond has the following properties:

1. The sum of the linear transformations corresponding to the sum of the matrices.
2. The product of the linear transformations corresponding to the product of the matrices.
3. The scalar multiplication of the linear transformation corresponding to the scalar multiplication of the matrices.
4. An invertible linear transformation corresponds to the invertible matrix, and the inverse transformation corresponds to the inverse matrix.

### Pf.

Let $\mathscr{A},\mathscr{B}$ be two linear transformations, and let their matrices with respect to the basis $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ be $A$ and $B$.

That is:
$$
\begin{aligned}
\mathscr{A}(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n) = (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)A\\
\mathscr{B}(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n) = (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)B
\end{aligned}
$$

1. $$
   \begin{aligned}
   (\mathscr{A} + \mathscr{B})(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n) &= \mathscr{A}(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n) + \mathscr{B}(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)\\
   &= (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)A + (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)B\\
   &= (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)(A+B)\\
   \end{aligned}
   $$

2. Similarly,
   $$
   \begin{aligned}
   (\mathscr{AB})(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n) &= \mathscr{A}(\mathscr{B}(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n))\\ 
   &= \mathscr{A}((\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)B)\\
   &= (\mathscr{A}(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n))B\\
   &= (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)AB
   \end{aligned}
   $$
   Therefore, with respect to the basis $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$, the matrix of the linear transformation $\mathscr{AB}$ is the matrix product $AB$.

3. $$
   \begin{aligned}
   (k\mathscr{A})(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n) &= k(\mathscr{A}(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n))\\
   &= k(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)A\\
   &= (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)kA
   \end{aligned}
   $$

4. The identity transformation corresponds to the identity matrix, therefore:
   $$
   \mathscr{AB} = \mathscr{BA} = \mathscr{E}
   $$
   is corresponding to:
   $$
   AB = BA = E
   $$
   So, an invertible linear transformation corresponds to the invertible matrix, and the inverse transformation corresponds to the inverse matrix.

Using the matrix of linear transformation, we can directly calculate an image of a vector.

> Theorem 3 states:

## Th.3

Let $\mathscr{A}$ be a linear transformation, and let its matrix with respect to the basis $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ be $A$.

The coordinates of the vector $\xi$ with respect to the basis $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ are $(x_1, x_2, \cdots, x_n)$.

Then the coordinates of the vector $\mathscr{A}\xi$ with respect to the basis $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ can be calculated according to the following formula:
$$
\begin{bmatrix} y_1\\ y_2\\ \vdots \\ y_n \end{bmatrix} = A\begin{bmatrix} x_1\\ x_2\\ \vdots \\ x_n \end{bmatrix}.
$$

### Pf.

We have:
$$
\xi = (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)\begin{bmatrix} x_1\\ x_2\\ \vdots \\ x_n \end{bmatrix}
$$
So,
$$
\begin{aligned}
\mathscr{A}\xi &= (\mathscr{A}\epsilon_1, \mathscr{A}\epsilon_2, \cdots, \mathscr{A}\epsilon_n)\begin{bmatrix} x_1\\ x_2\\ \vdots \\ x_n \end{bmatrix}\\
&= (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)A\begin{bmatrix} x_1\\ x_2\\ \vdots \\ x_n \end{bmatrix}\\
&= (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)\begin{bmatrix} y_1\\ y_2\\ \vdots \\ y_n \end{bmatrix}.
\end{aligned}
$$
$\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ are linearly independent, so we get:
$$
\begin{bmatrix} y_1\\ y_2\\ \vdots \\ y_n \end{bmatrix} = A\begin{bmatrix} x_1\\ x_2\\ \vdots \\ x_n \end{bmatrix}.
$$
The matrix of a linear transformation is linked to a basis in the space.

Generally speaking, as the basis changes, the same linear transformation will have different matrices.

Therefore, it is necessary for us to understand how the matrix of a linear transformation changes as the basis changes.

## Th.4

Let $\mathscr{A}$ be a linear transformation in linear space $V$, and let its matrices with respect to the basis $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ and $\eta_1, \eta_2, \cdots, \eta_n$ be $A$ and $B$.

The transition matrix from $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$ to $\eta_1, \eta_2, \cdots, \eta_n$ is $X$.

Then we have $B = X^{-1}AX$.

### Pf.

We know:
$$
\begin{aligned}
\mathscr{A}(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n) = (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)A\\
\mathscr{A}(\eta_1, \eta_2, \cdots, \eta_n) = (\eta_1, \eta_2, \cdots, \eta_n)A\\
(\eta_1, \eta_2, \cdots, \eta_n) = (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)X.
\end{aligned}
$$
So, we get:
$$
\begin{aligned}
\mathscr{A}(\eta_1, \eta_2, \cdots, \eta_n) &= \mathscr{A}((\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)X)\\
&= \mathscr{A}(\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)X\\
&= (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)AX\\
&= (\eta_1, \eta_2, \cdots, \eta_n)X^{-1}AX
\end{aligned}
$$
So, $B = X^{-1}AX$.

Theorem 4 tells us the relationship between the matrices of the same linear transformation $\mathscr{A}$ under different bases, and this fundamental relationship is very important.

Now, we will introduce the definition of similar matrices.

## Def.3

Let $A,B$ be two n-th order matrices over the field $P$.

If we can find an n-th order invertible matrix $X$, such that $B=X^{-1}AX$, then we say that $A$ is similar to $B$, denoted as $A \sim B$.

Now that we have the concept of matrix similarity, Theorem 4 can be restated as:

## Th.5

Matrices that represent the same linear transformation with respect to different bases are similar.

Conversely, if two matrices are similar, then they can be regarded as the matrices representing the same linear transformation with respect to two bases.

### Pf.

The first part is the conclusion of Theorem 4.

For the second part, suppose that the n-order matrices $A$ and $B$ are similar. Regard $A$ as the matrix of the linear transformation $\mathscr{A}$ in the n-dimensional linear space $V$ under the basis $\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n$.

Since $A$ and $B$ are similar, $B = X^{-1}AX$.

Let $(\eta_1, \eta_2, \cdots, \eta_n) = (\epsilon_1, \epsilon_2 ,\cdots, \epsilon_n)X$.

Then $\eta_1, \eta_2, \cdots, \eta_n$ is also a set of bases for $V$,  and $B$ is the matrix of $\mathscr{A}$ under this basis.

If $f(x)$ is a polynomial over the number field $P$, and $B = X^{-1}AX$

Then we have
$$
f(B) = X^{-1}f(A)X
$$
