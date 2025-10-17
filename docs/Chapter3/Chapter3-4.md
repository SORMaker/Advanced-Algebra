# Chapter3-4

## Definition 15

The row rank of matrices is called the rank of the row vectors in matrices, and the column rank of matrices is called the rank of the set of column vectors in matrices.

## Definition 16

In the $s\times n$  matrix A, randomly select k rows and k columns. The k-order determinant composed of the $k^2$ elements at the intersection of these selected rows and columns in the original order is called the k-order minor of A.

note: $k \leq min(s,n)$.

## Definition 17

The order of the highest non-zero minor in matrix A is called the rank of A. When A is a zero matrix, we say the rank of A is zero.

## Theorem 4

The rank of A = the column rank of A = the row rank of A.

### Proof:

We want to prove this theorem, and we need 

1. Prove the first r columns are linearly independent.
2. Prove that the first r columns can linearly represent any columns of A.

Firstly, assume that the rank of A is r. So there must be an r-th order minor of A that does not equal zero, and all (r+1)-th order minors equal zero.

We just proved that r = the column rank of A.

$$
A=\left[ \begin{array}{}
a_{11} & a_{12} & \cdots & a_{1r} & a_{1,r+1} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2r} & a_{2,r+1} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots & \vdots  & & \vdots\\
a_{r1} & a_{r2} & \cdots & a_{rr} & a_{r,r+1}& \cdots & a_{rn}\\
\vdots & \vdots & & \vdots &\vdots& & \vdots\\
a_{s1} & a_{s2} & \cdots & a_{sr} & a_{s,r+1} & \cdots & a_{sn}

 \end{array} \right]
$$

We can assume a minor r-th order in the first r columns that is not equal to zero.

 So we have

$$
d=\left| \begin{array}{}
a_{i_11} & a_{i_12} & \cdots & a_{i_1r}\\
a_{i_21} & a_{i_22} & \cdots & a_{i_2r}\\
\vdots & \vdots & & \vdots\\
a_{i_r1} & a_{i_r2} & \cdots & a_{i_rr}
 \end{array} \right| \neq 0.
$$

According to Cramer’s Rule, the system of linear equations 

$$
\left\{ \begin{array}{}
a_{i_11}x_1+a_{i_12}x_2+\cdots +a_{i_1r}x_r=0,\\
a_{i_21}x_1+a_{i_22}x_2+\cdots +a_{i_2r}x_r=0,\\
\cdots\\
a_{i_r1}x_1+a_{i_r2}x_2+\cdots +a_{i_rr}x_r=0.\\
 \end{array} \right.
$$

Only have zero solution because $d \neq 0$.

This means that the columns in d are linearly independent, and the first r columns in A are also linearly independent.

Because if a set of vectors is linearly independent, then the new set of vectors, formed by appending a component to each vector, is also linearly independent.

So the first r columns are linearly independent.

Then we need to prove that the first r columns can linearly represent any columns of A.

From A, we can choose the $i_1,i_2,\cdots,i_r,i$ rows and the $1,2,\cdots,r,j$columns, then we get an (r+1)-th order minor which should equal zero.

$$
\left| \begin{array}{}
a_{i_11} & a_{i_12} & \cdots & a_{i_1r} & a_{i_1j}\\
a_{i_21} & a_{i_22} & \cdots & a_{i_2r} & a_{i_2j}\\
\vdots & \vdots & & \vdots & \vdots\\
a_{i_r1} & a_{i_r2} & \cdots & a_{i_rr} & a_{i_rj}\\
a_{i1} & a_{i2} &  \cdots &a_{ir} & a_{ij}
 \end{array} \right|=0.
$$

We already know that the first r columns are linearly independent, so we must have 

$$
a_{i_kj}=l_1a_{i_k1} + l_2a_{i_k2} + \cdots + l_ra_{i_kr}, 1 \leq k \leq r.
$$

So, we can use $l_1$ times column 1 to subtract the last column, then use $l_2$ times column 2 to subtract the previous column, and repeat the same operations from $1 \cdots r$.

Then we get:

$$
\left| \begin{array}{}
a_{i_11} & a_{i_12} & \cdots & a_{i_1r} & 0\\
a_{i_21} & a_{i_22} & \cdots & a_{i_2r} & 0\\
\vdots & \vdots & & \vdots & \vdots\\
a_{i_r1} & a_{i_r2} & \cdots & a_{i_rr} & 0\\
a_{i1} & a_{i2} &  \cdots &a_{ir} & b
 \end{array} \right|=b\cdot d=0.
$$

d does not equal zero, so b must equal zero.

So the first r columns can linearly represent any columns of A.

## Corollary 1

The rank, column rank, and row rank of a matrix are preserved under elementary row and column operations.

$$
R(A)=R(col(A))=R(row(A))=R(B)=R(col(B))=R(row(B)).
$$

## Corollary 2

The rank of a matrix A is the number of non-zero rows in its row echelon form.

## Corollary 3

$$
B=\left[ \begin{array}{} 
0 & \cdots & 0 & b_{1i_1} & \cdots & b_{1i_2} & \cdots & b_{1i_r} & \cdots & b_{1n}\\
0 & \cdots & 0 & 0 & \cdots & b_{2i_2} & \cdots & b_{2i_r} & \cdots & b_{2n}\\
\vdots & & \vdots & \vdots & & \vdots & & \vdots & & \vdots\\
0 & \cdots & 0 & 0 & \cdots & 0 & \cdots & b_{ri_r} & \cdots & b_{rn}\\
0 & \cdots & 0 & 0 & \cdots & 0 & \cdots & 0 & \cdots & 0\\
0 & \cdots & 0 & 0 & \cdots & 0 & \cdots & 0 & \cdots & 0\\
\vdots & & \vdots & \vdots & & \vdots & & \vdots & & \vdots\\
0 & \cdots & 0 & 0 & \cdots & 0 & \cdots & 0 & \cdots & 0\\
\end{array} \right]
$$

Let B be a row echelon form of a matrix A. If the pivot columns of B are columns $i_1,i_2,\cdots,i_r$, then the corresponding columns $i_1,i_2,\cdots,i_r$ of the original matrix A form a basis for the column space of A.

## Corollary 4

Suppose 

$$
A=\left[ \begin{array}{}
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn}

 \end{array} \right]
$$

So, the column vectors(or row vectors) of a square matrix A are linearly dependent if and only if  $|A|=0$;The column vectors(or row vectors) of a square matrix A are linearly independent if and only if $|A| \neq 0$.

### Proof

The order of the highest-order minor of matrix A is n. The column vectors of A are linearly dependent which means the rank of A is less than n. So $|A|=0.$

## Theorem 5

The homogeneous linear system

$$
\left\{ \begin{array}{}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n=0,\\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n=0,\\
\cdots\\
a_{n1}x_1 + a_{n2}x_2 + \cdots + a_{nn}x_n=0.\\
 \end{array} \right.
$$

has non-trivial solutions if and only if the determinant of the coefficient matrix

$$
A=\left[ \begin{array}{}
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn}\\
 \end{array} \right]
$$

equals zero$|A|=0$; The homogeneous linear system has zero solution if and only if $|A|\neq0.$

### Proof

The homogeneous linear system has non-trivial solutions, which means the column vectors of A are linearly dependent, so $|A|=0.$

## Theorem 6

The linear system

$$
\left\{ \begin{array}{}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n=b_1,\\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n=b_2,\\
\cdots\\
a_{n1}x_1 + a_{n2}x_2 + \cdots + a_{nn}x_n=b_n.\\
 \end{array} \right.(1)
$$

has a unique solution if and only if the determinant of its coefficient matrix $|A|\neq0$.

### Proof

$\Leftarrow \text{(Sufficiency)}$

According to the Cramer Rule, we know that $x_i=\frac{|A_i|}{|A|}$. So the linear system has a unique solution.

$\Rightarrow \text{(Necessity)}$

Assume that the linear system has a unique solution $(c_1,c_2,\cdots,c_n)$.

Considering its homogeneous linear system, if it has a non-trivial solution $(d_1,d_2,\cdots,d_n)$, then it is obvious that $(c_1+d_1, c_2+d_2,\cdots,c_n+d_n)$ is a solution of the linear system$(1)$ and doesn’t equal $(c_1,c_2,\cdots,c_n)$. 

This contradicts the fact that system $(5)$ has a unique solution; therefore, its homogeneous linear system has only the trivial solution, and consequently, $|A|\neq0.$