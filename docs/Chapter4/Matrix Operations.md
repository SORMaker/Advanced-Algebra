# Matrix Operations

This section is about the calculation of matrices.

Therefore, we will not introduce the basic matrix operations, such as $A + B.$

We will focus on just a few properties.

## Property 1

$R(A+B) \leq R(A)+R(B)$

### Proof

Let 

$$
A=\left[ \begin{array}{}
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{m1} & a_{m2} & \cdots & a_{mn}
 \end{array} \right],
B=\left[ \begin{array}{}
b_{11} & b_{12} & \cdots & b_{1n}\\
b_{21} & b_{22} & \cdots & b_{2n}\\
\vdots & \vdots & & \vdots\\
b_{m1} & b_{m2} & \cdots & b_{mn}
 \end{array} \right]
$$

So, $A+B$ is

$$
A+B=\left[ \begin{array}{}
a_{11}+b_{11} & a_{12}+b_{12} & \cdots & a_{1n}+b_{1n}\\
a_{21}+b_{21} & a_{22}+b_{22} & \cdots & a_{2n}+b_{2n}\\
\vdots & \vdots & & \vdots\\
a_{m1}+b_{m1} & a_{m2}+b_{m2} & \cdots & a_{mn}+b_{mn}\\
 \end{array} \right]
$$

Suppose the set of row vectors A is $\set{\alpha_1, \alpha_2, \cdots, \alpha_s}$; the set of row vectors B is $\set{\beta_1, \beta_2,\cdots,\beta_s}$

So, we have

$$
A+B=\left[ \begin{array}{} 
\alpha_1\\
\alpha_2\\
\vdots\\
\alpha_s
\end{array} \right]+\left[ \begin{array}{}
\beta_1\\
\beta_2\\
\vdots\\
\beta_s
 \end{array} \right]=\left[ \begin{array}{}
\alpha_1 + \beta_1\\
\alpha_2 + \beta_2\\
\vdots\\
\alpha_s + \beta_s
 \end{array} \right]
$$

Hence, the set of row vectors of A+B is {α₁ + β₁， α₂ + β₂，..., αₛ + βₛ}. This set of row vectors can be linearly expressed by the union of a maximal linearly independent set of {αᵢ} and a maximal linearly independent set of {βᵢ}. Therefore, its rank does not exceed rank(A) + rank(B).

We already known the determinant has transpose, the matrix also has transpose.

- $(A^T)^T=A$
- $(A + B)^T = A^T + B^T$
- $(AB)^T = B^TA^T$
- $(kA)^T = kA^T$