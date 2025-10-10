# Chapter3-7

## Lemma

Suppose

$$
\begin{aligned}
f(x)=a_0x^{n} + a_1x^{n-1} + \cdots + a_n \quad (1)\\
g(x)=b_0x^{m} + b_1x^{m-1} + \cdots + b_m \quad (2)
\end{aligned}
$$

$a_0$ and $b_0$ are not all zero.

$f(x)$ and $g(x)$ have a non-constant common divisor if and only if there exist non-zero polynomials $v(x)$  and $u(x)$ such that:

1. $deg(v) < n$
2. $deg(u) < m$
3. $u(x)f(x) = v(x)g(x)$

### Proof

$\Longrightarrow$

If $f(x)$ and $g(x)$ have a non-constant common divisor $d(x)$, then we know 

$$
\begin{aligned}
f(x) = d(x)f_1(x)\\
g(x)=d(x)g_1(x)
\end{aligned}
$$

And the $deg(f_1(x)) < n,\ deg(g_1(x))<m$.

So we can make $u(x) = g_1(x),\ v(x) = f_1(x)$.

Obviously, we have $u(x)f(x)=d(x)f_1(x)g_1(x)=v(x)g(x).$

$\Longleftarrow$

$a_0$ and $b_0$ are not all zero, so suppose $a_0 \neq 0$. There exist non-zero polynomials $u(x)$ with $deg(u)<m$ and $v(x)$ with $deg(v) < n,$ such that $u(x)f(x) = v(x)g(x)$. Prove that $f(x)$ and $g(x)$ have a common divisor of degree greater than 0.

Let $d(x)$ be the greatest common divisor of $f(x)$ and $v(x)$, i.e., $d(x)=(f(x), v(x))$. This means we can write $f(x)=d(x)f_1(x)$ and $v(x)=d(x)v_1(x)$, where $(f_1(x), v_1(x))=1.$ Substituting these into the original equation gives $u(x)d(x)f_1(x)=d(x)v_1(x)g(x)$, which simplifies to $u(x)f_1(x)=g(x)v_1(x)$.

Since $d(x)$ is a divisor of $v(x)$ and we are given $deg(v) < n$, it follows that $deg(d) < n$. From the equation $f(x) = d(x)f_1(x)$, we have $deg(f_1)=deg(f)-deg(d) = n-deg(d)$. Because $deg(d)$ < n, the degree of $f_1(x)$  must be greater than 0.

From the equation $u(x)f_1(x)=g(x)v_1(x)$, it is clear that $f_1(x)$ divides the product $g(x)v_1(x)$. Since we know that $f_1(x)$ and $v_1(x)$ are coprime.(i.e., $(f_1(x),v_1(x))=1$) So, we can conclude that $f_1(x)$ must divide $g(x)$.

Thus, $f_1(x)$ is a common divisor of $f(x)$  and $g(x)$. Since we have already shown that $deg(f_1) > 0$, $f_1(x)$ is a common divisor of $f(x)$ and $g(x)$ with a degree greater than 0.

We use the method of undetermined coefficients to define the general forms of the polynomials:

$$
\begin{aligned}
u(x)=\sum^{m-1}_{i=0}u_ix^{m-1-i},\\
v(x)=\sum^{n-1}_{i=0}v_ix^{n-1-i}.
\end{aligned}
$$

Substituting these into the equation $u(x)f(x)=v(x)g(x)$, we get:

$$
\begin{cases}{} 
a_0u_0 = b_0v_0\\
a_1u_0 + a_0u_1 = b_1v_0 + b_0v_1\\
a_2u_0 + a_1u_1 + a_0u_2 = b_2v_0 + b_1v_1 + b_0v_2\\
\cdots\\
a_nu_{m-2} + a_{n-1}u_{m-1} = b_mv_{n-2} + b_{m-1}v_{n-1}\\
a_nu_{m-1} = b_mv_{n-1}
\end{cases}
$$

This is:

The required polynomials $u(x)$  and $v(x)$ exist 

$\Longleftrightarrow$

The system of linear equations shown above for the variables $u_0,\cdots,u_{m-1},v_0,\cdots,v_{n-1}$ has a non-trivial solution.

$\Longleftrightarrow$

The determinant of the coefficient matrix of this system is zero.

By transposing the coefficient matrix(swapping rows and columns), the value of the determinant remains unchanged, which is:

$$
\left| \begin{array}{}
a_0 & a_1 & a_2 & \cdots & \cdots & \cdots& a_n\\
& a_0 & a_1 & \cdots & \cdots & \cdots & a_{n-1} & a_n\\
& & & & \cdots & \cdots \\
& & & &  \cdots & a_0 & a_1 & \cdots & a_n\\

-b_0 & -b_1 & -b_2 & \cdots & \cdots & \cdots& -b_m\\
& -b_0 & -b_1 & \cdots & \cdots & \cdots & -b_{m-1} & -b_m\\
& & & & \cdots & \cdots \\
& & & &  \cdots & -b_0 & -b_1 & \cdots & -b_m\\
 \end{array} \right|
$$

The elements in this determinant are all coefficients of $f(x)$ and $g(x)$. we can multiply $(-1)^n$ and the determinant. This multiplication does not affect whether the determinant is zero or not.

So, we hereby define this new determinant to be the resultant of $f(x)$ and $g(x)$.

$$
R(f,g)=\left| \begin{array}{}
a_0 & a_1 & a_2 & \cdots & \cdots & \cdots& a_n\\
& a_0 & a_1 & \cdots & \cdots & \cdots & a_{n-1} & a_n\\
& & & & \cdots & \cdots \\
& & & &  \cdots & a_0 & a_1 & \cdots & a_n\\

b_0 & b_1 & b_2 & \cdots & \cdots & \cdots& b_m\\
& b_0 & b_1 & \cdots & \cdots & \cdots & b_{m-1} & b_m\\
& & & & \cdots & \cdots \\
& & & &  \cdots & b_0 & b_1 & \cdots & b_m\\
 \end{array} \right|
$$

## Theorem 10

Let $f(x)=\sum^{n}_{i=0}a_ix^{n-i}$ and $g(x)= \sum^m_{i=0}b_ix^{m-i}$ be two polynomials over a field $P$, with $m,n > 0$. Then, the resultant $R(f,g)=0$ if and only if either:

1. $f(x)$ and $g(x)$ have a common divisor of degree greater than 0 in P[x], or
2. $a_0$ and $b_0$ are both zero.

### Proof

$\Longrightarrow$

Assume $R(f,g) = 0$. If at least one of $f(x)$ or $g(x)$ is the zero polynomial, the conclusion holds. If neither is the zero polynomial, and if $a_0 = b_0 = 0$, the conclusion holds by the theorem’s statement.

Otherwise, $a_0$ and $b_0$ are not both zero.From $R(f,g)=0$, we know that the corresponding homogeneous system of linear equations has a non-trivial solution. This means there exist polynomials $u(x)$ and $v(x)$, not both zero, satisfying the equation $u(x)f(x)=v(x)g(x)$.

Since we are in the case where $f(x)$ and $g(x)$ are non-zero, it follows that both $u(x)$ and $v(x)$ must also be non-zero. Furthermore, by the construction of the system, we have $deg(u)<m$ and $deg(v)<n$.

According to the previous lemma, it follows that $f(x)$ and $g(x)$ have a common divisor of degree greater than 0.

$\Longleftarrow$

If $a_0=b_0=0$,then the first column of the resultant matrix $R(f,g)$ consists entirely of zeros. Therefore, it is natural that $R(f,g)=0$.

If $a_0$ and $b_0$ are not all zero, but at least one of $f(x)$ or $g(x)$ is the zero polynomial, then there will be entire rows of zeros in the resultant $R(f,g)$. Naturally, $R(f,g)=0$.

If $a_0$ and $b_0$ are not all zero, neither $f(x)$ nor $g(x)$ is the zero polynomial, and they have a common divisor of degree greater than 0, then by the lemma, we know there exist non-zero polynomials $u(x)$ and $v(x)$ satisfying $u(x)f(x)=v(x)g(x)$, with $deg(u)<m$ and $deg(v)<n$.

This implies that the corresponding homogeneous system of linear equations has a non-trivial solution, and therefore the determinant of its coefficient matrix must be zero. Since the resultant $R(f, g)$ is simply this determinant multiplied by a factor (e.g., $(-1)^n$), the resultant is also zero.

Another form of Theorem 10 is: The resultant $R(f, g)$ = 0 if and only if $f(x)$ and $g(x)$ have a common root in the complex field, or their leading coefficients are both zero.

One of the applications of the resultant is to solve systems of higher-degree bivariate equations of the form:

$$
\begin{cases} 
f(x,y)=0\\
g(x,y)=0
\end{cases}
$$

We arrange the bivariate polynomials in the system by treating them as polynomials in the variable x, where the coefficients are polynomials in y:

$$
\begin{cases} 
f(x,y)= a_0(y)x^n + a_1(y)x^{n-1} + \cdots + a_n(y)\\
g(x,y)= b_0(y)x^m + b_1(y)x^{m-1} + \cdots + b_m(y)\\
\end{cases}
$$

Here, the coefficients $a_i(y)$ and $b_j(y)$ are polynomials in y. By viewing f(x,y) and g(x,y) as polynomials in x, we can define their resultant with respect to x, denoted $R_x(f,g)$, as the following determinant:

$$
R_x(f,g)=\left| \begin{array}{} 
a_0(y) & a_1(y) & a_2(y) & \cdots & \cdots & \cdots& a_n(y)\\
& a_0(y) & a_1(y) & \cdots & \cdots & \cdots & a_{n-1}(y) & a_n(y)\\
& & & & \cdots & \cdots \\
& & & &  \cdots & a_0(y) & a_1(y) & \cdots & a_n(y)\\

b_0(y) & b_1(y) & b_2(y) & \cdots & \cdots & \cdots& b_m(y)\\
& b_0(y) & b_1(y) & \cdots & \cdots & \cdots & b_{m-1}(y) & b_m(y)\\
& & & & \cdots & \cdots \\
& & & &  \cdots & b_0(y) & b_1(y) & \cdots & b_m(y)\\

\end{array} \right|
$$

## Theorem 11

1. If $(x_0, y_0)$ is a solution to the system of bivariate equations, then $y_0$ is a root of the resultant $R_x(f,g)$.
2. Conversely, if $y_0$ is a root of the resultant $R_x(f,g)$, then either the $a_0(y)$ and $b_0(y)$ are both zero, or there exists a complex number $x_0$ such that $(x_0,y_0)$ is a solution to the system.

### Proof

The theorem can be proven by treating the coefficients $a_i(y)$ and $b_i(y)$ as constants and directly applying Theorem 10.