# Chapter3-6

If we have $Ax=0.$ 

Then we also have 

1. $A(k+l)=Ak+Al=0+0=0$
2.  $A(ck)=c\cdot A(k)=c \cdot 0=0$

## Definition 18

A set of solutions to a homogeneous system of linear equations is called a fundamental system of solutions if it satisfies two conditions:

1. The solutions in the set are linearly independent.
2. Any solution to the system can be expressed as a linear combination of the solutions in the set.

## Theorem 8

A homogeneous linear system with n variables and a coefficient matrix of rank r has a fundamental system of solutions consisting of $n-r$ vectors.

### Proof

We have a homogeneous system of linear equations.

$$
\left\{ \begin{array}{}
a_{11}x_1 + \cdots + a_{1r}x_r = -a_{1,r+1}x_{r+1} - \cdots - a_{1n}x_n,\\
a_{21}x_1 + \cdots + a_{2r}x_r = -a_{2,r+1}x_{r+1} - \cdots - a_{2n}x_n,\\
\cdots\\
a_{r1}x_1 + \cdots + a_{rr}x_r = -a_{r,r+1}x_{r+1} - \cdots - a_{rn}x_n,\\
 \end{array} \right.
$$

If $r=n$, then the linear system doesn’t have free unknowns, which means it only has a trivial solution.

So suppose $r<n$.

We know that if any two solutions of a homogeneous linear system have the same free variables, then the two solutions are the same.

Therefore, by substituting $n-r$ sets of values $(1,0,\cdots,0),(0,1,\cdots,0),\cdots,(0,0,\cdots,1)$ for the free variables, we can obtain $n-r$ solutions to the homogeneous system.

$$
\left\{ \begin{array}{}
\eta_1 = (c_{11}, \cdots, c_{1r}, 1, 0, \cdots, 0),\\
\eta_2 = (c_{21}, \cdots, c_{2r}, 0, 1, \cdots, 0),\\
\cdots\\
\eta_{n-r} = (c_{n-r,1}, \cdots, c_{n-r,r}, 0, 0, \cdots, 1),\\
 \end{array} \right.
$$

1. First prove $\eta_i(1=1, \cdots, n-r)$ are linearly independent
    
    $$
    k_1\eta_1 + k_2\eta_2 + \cdots + k_{n-r}\eta_{n-r}=0,\\
    k_1\eta_1 + k_2\eta_2 + \cdots + k_{n-r}\eta_{n-r} = ( *, \cdots, *, k_1, k_2, \cdots, k_{n-r} ) \\
    = ( 0, \cdots, 0, 0, 0, \cdots, 0 ),\\
    so\ k_1 = k_2 = \cdots = k_{n-r} = 0.
    $$
    
    So $\set{\eta_i}$ are linearly independent.
    
2. Secondly, prove that any $\eta$ can be linearly represented by $\set{\eta_1, \cdots, \eta_{n-r}}$
    
    Suppose we have a solution $\eta = (c_1, \cdots, c_r, c_{r+1}, c_{r+2}, \cdots, c_n)$, and the linear combination $c_{r+1}\eta_1 + c_{r+2}\eta_2 + \cdots + c_{n}\eta_{n-r}$ is also a solution. Comparing the last $n-r$ components, we know that they have the same free variables, so 
    
    $$
    \eta = c_{r+1}\eta_1 + c_{r+2}\eta_2 + \cdots + c_{n}\eta_{n-r}
    $$
    

Next, let us consider the structure of solutions to the general system of linear equations.

$$
\left\{ \begin{array}{}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n = b_1,\\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = b_2,\\
\cdots\\
a_{s1}x_1 + a_{s2}x_2 + \cdots + a_{sn}x_n = b_s,\\
 \end{array} \right.(*)
$$

If we set all constant terms to zero, then we get a homogeneous linear system, and the homogeneous linear system is called the derived system of $(*)$.

1. The difference between two solutions of a system of linear equations is a solution to its derived system.
    
$$
\begin{aligned}
Ak=b,Al=b.\\
A(k-l)=0
\end{aligned}
$$
    
2. The sum of a solution to a system of linear equations and a solution to its derived system is still a solution to the same system of linear equations.
    
$$
\begin{aligned}
Ak=b,Al=0.\\
A(k+l)=b
\end{aligned}
$$
    

## Theorem 9

If $\gamma_0$ is a particular solution of $(*)$, then the solution set of the system is $\set{\gamma_0 + \eta|\text{where }\eta \text{ is a solution to the derived system}}$

### Proof

Let S be the solution set of $(*)$. We will now prove that $S = \set{\gamma_0 + \eta|\text{where }\eta \text{ is a solution to the derived system}}$.

For any $\gamma \in S$, we know $\gamma-\gamma_0$ is a solution to the derived system. Therefore, we can write $\gamma=\gamma_0 + (\gamma - \gamma_0)$, which means $\gamma \in \set{\gamma_0 + \eta|\text{where }\eta \text{ is a solution to the derived system}}$.

This shows that S is a subset of $\set{\gamma_0 + \eta|\text{where }\eta \text{ is a solution to the derived system}}$.

let $\eta_0$ be any solution to the derived system. We know that $\gamma_0 + \eta_0$ is a solution to the original system of equations. Therefore, $\gamma_0 + \eta_0 \in S$, which means that S contains the set $\set{\gamma_0 + \eta|\text{where }\eta \text{ is a solution to the derived system}}$

So, $S = \set{\gamma_0 + \eta|\text{where }\eta \text{ is a solution to the derived system}}$

This theorem tells us that any solution to $(*)$ can be expressed as a linear combination of $\gamma_0$ and a solution to the derived system.

Therefore, as $\eta$ ranges over the entire solution set of the derived system, the expression $\gamma_0 + \eta$ generates the entire solution set of $(*)$.

If $\set{\eta_1, \eta_2, \cdots, \eta_{n-r}}$ is a fundamental system of solutions for the derived system, and $\gamma_0$ is a particular solution of $(*)$, then the solution set S of the $(*)$ is given by:

$$
S = \set{\gamma_0 + \eta_1, \gamma_0 + \eta_2, \cdots, \gamma_0 + \eta_{n-r}}
$$


## Corollary

Under the condition that $(*)$ has solutions, it has a unique solution if and only if its derived system has only the trivial solution.

$\Longrightarrow$

$(*)$ has a unique solution $\Rightarrow$ S = $\set{\gamma_0}$ $\Rightarrow$ $k_i = 0 (i=1,2,\cdots,n-r)$ $\Rightarrow$ its derived system has only the trivial solution.

> If the derived system has a non-trivial solution, then we add the non-trivial solution to a solution of $(*)$, and then we get another solution of $(*)$, which means $(*)$ has many solutions. So, if $(*)$ has a unique solution, then its derived system’s solution only has a trivial solution.

$\Longleftarrow$

The derived system of $(*)$ has only the trivial solution $\Rightarrow$ $k_i = 0 (i=1,2,\cdots,n-r)$ $\Rightarrow$ S = $\set{\gamma_0}$ $\Rightarrow$ $(*)$ has a unique solution.

> If $(*)$ has two different solutions, then the subtraction of them is a non-trivial solution of its derived system. So, if the derived system only has a trivial solution, then $(*)$ has a unique solution.

