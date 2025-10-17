# Chapter2-8

## Definition 9

In an n-order determinant D, randomly select k rows and k columns. The $k^2$ elements at the intersection of these rows and columns, in the original order, form the k-order determinant M, which is called the k-order minor of the determinant D. When $k<n$, the (n-k)-order determinant M' formed by the remaining elements after crossing out these k rows and columns in D in the original order is called the co-minor of the k-order minor M.

## Definition 10

Suppose the row and column indices of the k-order minor M of D in D are $i_1,i_2,\dots,i_k,j_1,j_2,\dots,j_k$ , respectively. Then the co-minor M' of M with the symbol $(-1)^{(i_1 + i_2 + \dots + i_k) + (j_1 + j_2 + \dots + j_k)}$ in front of it is called the cofactor of M.

## Lemma

Every term in the product of any minor M of the determinant D and its cofactor A is a term in the expansion of the determinant D, and the signs are the same.

### Proof:

First, we consider **a special case** where the minor M is located in the upper left of the determinant D:

$$
D = \left| \begin{array}{cccc:ccc}
a_{11} & a_{12} & \dots & a_{1k} & a_{1,k+1} & \dots & a_{1n} \\ 
\vdots & \vdots & M & \vdots & \vdots & & \vdots \\
a_{k1} & a_{k2} & \cdots & a_{kk}  & a_{k,k+1} & \cdots & a_{kn}\\
\hdashline \\
a_{k+1,1} & a_{k+1,2} & \cdots & a_{k+1,k} & a_{k+1,k+1} & \cdots & a_{k+1,m} \\
\vdots & \vdots & & \vdots & \vdots & M' & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nk} & a_{n,k+1} & \cdots & a_{n,n}
\end{array} \right|
$$

So the cofactor of M is:

$$
A = (-1)^{ ( 1+2+\cdots + k ) + ( 1+2+\cdots+k )}M'=M'.
$$

Each term of M can be written as :

$$
a_{1\alpha_1}a_{2\alpha_2}\cdots a_{k\alpha_k}
$$

Where $\alpha_1 \alpha_2 \cdots \alpha_k$ is a permutation of 1,2,…,k. So the sign preceding this term is $(-1)^{\tau( \alpha_1\alpha_2\cdots\alpha_k )}$

Similarly, each term of M’ can be written as:

$$
a_{k+1,\beta_{k+1}}a_{k+2,\beta_{k+2}}\cdots a_{n\beta_n}
$$

where $\beta_{k+1}\beta_{k+2}\cdots \beta_{n}$is a permutation of k+1, k+2,…,n. And the sign preceding this term is $(-1)^{ \tau( ( \beta_{k+1}-k )( \beta_{k+2}-k )\cdots( \beta_{n}-k ) ) }$.

The product of these two terms is:

$$
a_{1\alpha_1}a_{2\alpha_2}\cdots a_{k\alpha_k}a_{k+1,\beta_{k+1}}a_{k+2,\beta_{k+2}}\cdots a_{n\beta_n},
$$

And the sign in front is:

$$
(-1)^{\tau( \alpha_1\alpha_2\cdots\alpha_k )+ \tau( ( \beta_{k+1}-k )( \beta_{k+2}-k )\cdots( \beta_{n}-k ) ) }.
$$

Because each $\beta$ is greater than $\alpha$, $\beta$ didn’t form an inverse order with $\alpha$ . Therefore, the above sign is equal to:

$$
(-1)^{ \tau( \alpha_1\alpha_2\cdots\alpha_k\beta_{k+1}\cdots\beta_n ) }
$$

So this product is a term in the determinant D and has the same sign.

Now, let’s consider **the general case**.

Assume we select $i_1,i_2,\cdots,i_k$rows and $j_1,j_2,\cdots,j_k$columns from determinant D, and $i_1 < i_2< \cdots < i_k,j_1<j_2<\cdots<j_k$.

Then we can make a series of interchanges to put the minor M in the upper left of the determinant D.

To do this, we can successively interchange $i_1$ row with $i_1-1,i_1-2,\cdots,2,1$rows. After $i_1-1$ interchanges, we put the $i_1$ row in the 1st row. Then we do the same for the remaining rows. We totally make  interchanges.

Similarly, we can make $(j_1-1)+(j_2-2)+\cdots+(j_k-k)=( j_1+j_2+\cdots+j_k )-(1+2+\cdots+k)$ column interchanges to transform the columns of M to the 1st, 2nd,…,k-th columns.

We use $D_1$ to represent the new determinant after transforming. So 

$$
D_1=(-1)^{( i_1+i_2+\cdots+i_k )-(1 + 2 + \cdots + k)+( j_1 + j_2 + \cdots + j_k )-( 1 + 2 + \cdots + k )}D=( -1 )^{i_1 + i_2 + \cdots + i_k + j_1 + j_2 + \cdots + j_k}D
$$

From this, we can see the terms in the expansions of $D_1$ and $D$  are the same; The only difference is that each term has a different sign $(-1)^{i_1 + \cdots + i_k + j_1 + \cdots + j_k}$.

Now, M is located in the upper left corner of $D_1$, the minor of $D_1$ and the cofactor of $D_1$ are $M'$, so each term in $MM'$ is a term in $D_1$ and has the same sign. 

But 

$$
MA=(-1)^{i_1 + \cdots + i_k + j_1 + \cdots + j_k}MM'
$$

So, each term in MA equals each term in D, and they have the same sign.

## Theorem 6(Laplace‘s theorem)

Suppose we randomly select $k(1 \leq k \leq n-1)$ rows in determinant D. The sum of the products of all k-order minors composed of the elements of these k rows and their cofactors equals determinant D.

$$
D=M_1A_1 + M_2 A_2 + \cdots + M_t A_t
$$

### Proof:

After selecting  $k$ rows in a determinant $D$, we get the minors $M_1,M_2,\cdots,M_t$, and their cofactors are $A_1,A_2,\cdots,A_t$.

According to Lemma, each term in $M_i A_i$ is a term in $D$, and they have the same sign. Moreover, $M_iA_i$ and $M_jA_j$ don’t contain common terms.

Therefore, to prove the theorem, we must only confirm that the number of terms on both sides of the equation is equal.

Obviously, there are $n!$ terms on the left side of the equation. To calculate the number of terms on the right side, we must get $t$.

$$
t=C_{n}^{k}=\frac{n!}{k! (n-k)!}.
$$

Because there are $k!$ terms in $M_i$, $(n-k)!$ terms in $A_i$. So there are 

$$
tk!(n-k)!=n!
$$

terms on the right side.

## Theorem 7

We have two n-th order determinants,

$$
D_1=\left| \begin{array}{}a_{11} & a_{12} & \cdots & a_{1n} \\ 
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{array} \right|,D_2=\left| \begin{array}{} 
b_{11} & b_{12} & \cdots & b_{1n} \\
b_{21} & b_{22} & \cdots & b_{2n} \\
\vdots & \vdots & & \vdots \\
b_{n1} & b_{n2} & \cdots & b_{nn}

 \end{array} \right|.
$$

The product of them equals an n-th order determinant,

$$
C=\left| \begin{array}{} c_{11} & c_{12} & \cdots & c_{1n}\\
c_{21} & c_{22} & \cdots & c_{2n}\\
\vdots & \vdots & & \vdots \\
c_{n1} & c_{n2} & \cdots & c_{nn}
\end{array} \right|,
$$

where $c_{ ij }$ is the sum of the product of the i-th row in $D_1$ and the j-th column in $D_2$: 

$$
c_{ij} = a_{i1}b_{1j} + a_{i2}b_{2j} + \cdots + a_{in}b_{nj}
$$

### Proof:

We can create a determinant of 2n-th order:

$$
D=\left| \begin{array}{}
a_{11} & a_{12} & \cdots & a_{1n} & 0 & 0 & \cdots & 0 \\
a_{21} & a_{22} & \cdots & a_{2n} & 0 & 0& \cdots & 0\\
\vdots & \vdots & & \vdots & \vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn} & 0 & 0 & & 0\\
-1 & 0 & \cdots & 0 & b_{11} & b_{12} & \cdots & b_{1n}\\
0 & -1 & \cdots & 0 & b_{21} & b_{22} & \cdots & b_{2n}\\
\vdots & \vdots & & \vdots & \vdots & \vdots & & \vdots\\
0 & 0 & \cdots & -1 & b_{n1} & b_{n2} & \cdots & b_{nn}

 \end{array} \right|.
$$

According to Laplace’s theorem, we expand the determinant D with the first n rows. 

Because, except for the n-order minor in the upper left corner, the remaining n-order minors in the first n rows of D are all equal to zero. 

So:

$$
D=\left| \begin{array}{}
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn}
 \end{array} \right| 
\cdot
\left| \begin{array}{}
b_{11} & b_{12} & \cdots & b_{1n}\\
b_{21} & b_{22} & \cdots & b_{2n}\\
\vdots & \vdots & & \vdots\\
b_{n1} & b_{n2} & \cdots & b_{nn}
 \end{array} \right|=D_1D_2.
$$

Now, let’s prove $D=C$.

We make elementary row transformations on D, and we add the $a_{11}$ times the n+1 row to the first row. Then we add the $a_{12}$ times the n+2 row to the first row. … Finally, we add the $a_{1n}$ times the 2n row to the first row. 

We can get:

$$
D=\left| \begin{array}{}
0 & 0 & \cdots & 0 & c_{11} & c_{12} & \cdots & c_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} & 0 & 0& \cdots & 0\\
\vdots & \vdots & & \vdots & \vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn} & 0 & 0 & & 0\\
-1 & 0 & \cdots & 0 & b_{11} & b_{12} & \cdots & b_{1n}\\
0 & -1 & \cdots & 0 & b_{21} & b_{22} & \cdots & b_{2n}\\
\vdots & \vdots & & \vdots & \vdots & \vdots & & \vdots\\
0 & 0 & \cdots & -1 & b_{n1} & b_{n2} & \cdots & b_{nn}

 \end{array} \right|.
$$

Then we repeat the same operation for the other columns. The D is:

$$
D=\left| \begin{array}{}
0 & 0 & \cdots & 0 & c_{11} & c_{12} & \cdots & c_{1n} \\
0 & 0 & \cdots & 0 & c_{21} & c_{22} & \cdots & c_{2n} \\
\vdots & \vdots & & \vdots & \vdots & \vdots & & \vdots\\
0 & 0 & \cdots & 0 & c_{n1} & c_{n2} & \cdots & c_{nn} \\
-1 & 0 & \cdots & 0 & b_{11} & b_{12} & \cdots & b_{1n}\\
0 & -1 & \cdots & 0 & b_{21} & b_{22} & \cdots & b_{2n}\\
\vdots & \vdots & & \vdots & \vdots & \vdots & & \vdots\\
0 & 0 & \cdots & -1 & b_{n1} & b_{n2} & \cdots & b_{nn}

 \end{array} \right|.
$$

Using Laplace’s theorem, we know:

$$
D= \\ \left| \begin{array}{}  
c_{11} & c_{12} & \cdots & c_{1n}\\
c_{21} & c_{22} & \cdots & c_{2n}\\
\vdots & \vdots & & \vdots\\
c_{n1} & c_{n2} & \cdots & c_{nn}
\end{array}  \right| \cdot (-1)^{(1 + 2 + \cdots + n) + (n+1 + n+2 + \cdots + 2n)} \left| \begin{array}{} 
-1 & 0 & \cdots & 0\\
0 & -1 & \cdots & 0\\
\vdots & \vdots & & \vdots\\
0 & 0 & \cdots & -1
  \end{array} \right|=\\
\left| \begin{array}{}  
c_{11} & c_{12} & \cdots & c_{1n}\\
c_{21} & c_{22} & \cdots & c_{2n}\\
\vdots & \vdots & & \vdots\\
c_{n1} & c_{n2} & \cdots & c_{nn}
\end{array}  \right| \cdot
(-1)^{1+2+\cdots+2n} \cdot (-1)^{n}=C \cdot (-1)^{2n(n+1)}=C
$$