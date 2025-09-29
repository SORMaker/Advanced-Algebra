# Chapter3-5

Suppose the linear system is 

$$
\left\{ \begin{array}{}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n=b_1,\\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n=b_2,\\
\cdots\\
a_{s1}x_1 + a_{s2}x_2 + \cdots + a_{sn}x_n=b_s.\\
 \end{array} \right.(1)
$$

We can rewrite it in the form of a vector equation.

$$
x_1\alpha_1+x_2\alpha_2+\cdots + x_n\alpha_n=\beta,\\
\alpha_i=\left[ \begin{array}{} 
a_{1i}\\
a_{2i}\\
\vdots\\
a_{si}
\end{array} \right],\beta=\left[ \begin{array}{} 
b_{1}\\
b_{2}\\
\vdots\\
b_{s}
\end{array} \right].
$$

Obviously, the linear system has solutions if and only if $\beta$ can be linearly represented by the set of vectors $\alpha_i$.

## Theorem 7

The linear system $(1)$ has solutions if and only if its coefficient matrix and its augmented matrix have the same rank.

### Proof

$\Rightarrow$

The linear system has solutions, which means $\beta$ can be linearly represented by $\alpha_i$. So from this, we can immediately deduce that the set of vectors $\alpha_i$ and $\alpha_i,\beta$ are equivalent. So matrix $A$  and $\overline{A}(A|B)$ have the same rank.

$\Leftarrow$

If matrix $A$  and $\overline{A}$ have the same rank, and the rank of $A$  = r, which means that their column vectors $\set{\alpha_i(i=1,\cdots,n)}$ and $\set{\alpha_i,\beta}$ have the same rank. 

We can assume that their maximal linearly independent vectors are $\alpha_j(j=1,\cdots,r)$. Obviously, $\alpha_j$  is also a maximal linearly independent vector of $\set{\alpha_i,\beta}$(because if $\beta$  can’t be linearly represented by $\alpha_j$, then the maximal linearly independent vectors of $\set{\alpha_i,\beta}$ are $\set{\alpha_j,\beta}$, the rank of it is $r+1\neq r$), so $\beta$ can be linearly represented by $\alpha_j$.

So $\beta$ can be linearly represented by $\alpha_i$. The linear system has solutions.