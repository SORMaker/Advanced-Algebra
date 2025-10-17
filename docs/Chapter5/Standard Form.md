# Standard Form

## Theorem 1

Any quadratic form over a field P can be transformed into a sum of squares $d_1x_1^2 + d_2x_2^2 + \cdots + d_nx_n^2$ by a non-degenerate linear substitution.

### Proof

The proof that follows is the method of completing the square. We will proceed by induction on the number of variables n.

For the case $n=1$, the theorem is trivially true.

Now, we assume that the theorem holds for any quadratic form in $n-1$ variables.

So we have
$$
f(x_1, x_2, \cdots, x_n) = \sum^n_{i=1}\sum^n_{j=1}a_{ij}x_ix_j, \ a_{ij}=a_{ji}.
$$
There are three cases:

1. $\exist a_{ii} \neq 0$
   suppose $a_{11} \neq 0$, then we have
   $$
   \begin{split}
   f(x_1, x_2, \cdots , x_n) &= a_{11}x_1^2 + 2a_{12}x_1x_2 + \cdots + 2a_{1n}x_1x_n +  a_{22}x_2^2 + \cdots + 2a_{2n}x_2x_n + a_{nn}x_n^2 \\
   &=a_{11}(x_1^2 + 2\frac{a_{12}}{a_{11}}x_1x_2 + \cdots + 2\frac{a_{1n}}{a_{11}}x_1x_n) + a_{22}x_2^2 + \cdots + a_{nn}x_n^2 \\
   &=a_{11}(x_1^2 + 2x_1(\frac{a_{12}}{a_{11}}x_2 + \cdots + \frac{a_{1n}}{a_{11}}x_n) + (\frac{a_{12}}{a_{11}}x_2 + \cdots + \frac{a_{1n}}{a_{11}}x_n)^2) \\
   &- (\frac{a_{12}}{a_{11}}x_2 + \cdots + \frac{a_{1n}}{a_{11}}x_n)^2 + a_{22}x_2^2 + \cdots + a_{nn}x_n^2 \\
   &= a_{11}(x_1 + \frac{a_{12}}{a_{11}}x_2 + \cdots + \frac{a_{1n}}{a_{11}})^2 + b_{22}x_2^2 + \cdots + b_{nn}x_n^2
   \end{split}
   $$
   we use non-degenerate linear substitution 
   $$
   \begin{cases}
   x_1 = y_1 - \frac{a_{12}}{a_{11}}y_2 - \cdots - \frac{a_{1n}}{a_{11}}y_n \\
   x_2 = y_2 \\
   \quad \ \vdots\\
   x_n = y_n
   \end{cases}
   $$
   Then we get
   $$
   f(x_1, x_2, \cdots , x_n) = a_{11}x_1^2 + b_{22}x_2^2 + 2b_{23}y_2y_3 + \cdots + b_{nn}y_n^2
   $$
   According to the induction hypothesis, there exists a non-degenerate linear substitution to change $b_{22}x_2^2 + 2b_{23}y_2y_3 + \cdots + b_{nn}y_n^2$ into $d_2z_2^2 + d_3z_3^2 + \cdots + d_nz_n^2$.

   Let $y_1 = z_1$, we finally get:
   $$
   f(x_1, x_2, \cdots , x_n) = a_{11}z_1^2 + d_2z_2^2 + d_3z_3^2 + \cdots + d_nz_n^2
   $$

2. $\forall a_{ii}=0, \exist a_{1j} \neq 0$
   Suppose $a_{12} \neq 0 $, we have a non-degenerate linear substitution:
   $$
   \begin{cases}
   x_1 = y_1 + y_2\\
   x_2 = y_1 - y_2\\
   x_3 = y_3
   \quad \ \vdots\\
   x_n = y_n
   \end{cases}
   $$
   Then we get:
   $$
   \begin{split}
   f(x_1, x_2, \cdots , x_n) &= 2a_{12}x_1x_2 + \cdots \\ 
   &= 2a_{12}(z_1 + z_2)(z_1 - z_2) + \cdots \\
   &= 2a_{12}z_1^2 - 2a_{12}z_2^2 + \cdots
   \end{split}
   $$
   Thus, we have reduced the second case to the first, for which the theorem holds.

3. $a_{11} = a_{12} = \cdots = a_{1n} = 0$
   If $a_{11} = a_{12} = \cdots = a_{1n} = 0$, according to the symmetric, we know that $a_{11} = a_{21} = \cdots = a_{n1} = 0$.
   This is a quadratic form in $n-1$ variables, and by the induction hypothesis, it can be transformed into a sum of squares using a non-degenerate linear substitution.

## Theorem 2

Over a field P, every symmetric matrix is congruent to a diagonal matrix.
$$
A\text{为对称矩阵}\\
\Rightarrow f(x_1, x_2, \cdots , x_n) = X^TAX \text{为二次型}.\\
\Rightarrow \text{存在非退化线性替换} X=CZ, \text{将}X^TAX\text{化为}\\
Z^TBZ=d_1z_1^2 + d_2z_2^2 + \cdots + d_nz_n^2.\\
\Rightarrow A\text{与对角矩阵}B=C^TAC\text{是合同的}.
$$
$d_1x_1^2 + d_2x_2^2 + \cdots + d_nx_n^2$ is called the standard form.