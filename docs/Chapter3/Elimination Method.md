# Elimination method

Let me introduce some basic concepts.

Here is a general system of linear equations:

$$
\left\{  \begin{array}{}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n = b_1,\\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = b_2, \\
\cdots \\
a_{s1}x_1 + a_{s2}x_2 + \cdots + a_{sn}x_n = b_s
  \end{array} \right.\tag{1}
$$

In these linear equations, we have s equations in n unknowns.

We call $a_{ij}（i=1,2,\cdots,s,j=1,2,\cdots,n）$the coefficient of the equation and call $b_{j}(j=1,2,\cdots,s)$ the constant term.

If we have n numbers $k_1,k_2,\cdots,k_n$, we substitute $x_i$ with $k_i$. Then every equation becomes an identity, which  $k_i$ is called a solution of linear equations.

The set of all solutions to a system of linear equations is called its solution set.

If two systems of linear equations have the same solution set, they are called the same solution.

We often use a matrix to represent a linear equations system.

$$
\left[ \begin{array}{}
a_{11} & a_{12} & \cdots & a_{1n} & b_1\\
a_{21} & a_{22} & \cdots & a_{2n} & b_2\\
\vdots & \vdots & & \vdots & \vdots\\
a_{s1} & a_{s2} & \cdots & a_{sn} & b_s
 \end{array} \right]
$$

This is called the augmented matrix of the linear equation system $(1)$.

I will use an example to introduce the elimination method.

Here is a linear equation system with three equations in three unknowns.

$$
\left\{ \begin{array}{}  
2x_1 -x_2 + 3x_3 = 1,\\
4x_1 + 2x_2 + 5x_3 = 4,\\
2x_1 + x_2 + 2x_3 = 5.
\end{array}
\right.
$$

First, we use equation 2 minus 2 times equation 1. Then we use equation 3 minus equation 1. We got:

$$
\left\{ \begin{aligned}{} 
2x_1 - x_2 + 3x_3 = 1,\\
4x_2-x_3=2,\\
2x_2 - x_3 = 4.

\end{aligned} \right.
$$

Finally, we swap equation 2 minus 2 times equation 3. We got a system of linear equations that can be easily solved.

$$
\left\{ \begin{aligned}{} 
2x_1 - x_2 + 3x_3 = 1,\\
2x_2 - x_3 = 4,\\
x_3 = -6

\end{aligned} \right.
$$

So the solution of these linear equations is $(9,-1,-6)$.

## Definition 1

According to the above process, it is not difficult to know that the elimination method comprises three fundamental transformations.

1. Use a non-zero number times an equation.
2. Add multiples of an equation to another.
3. Swap the positions of two equations.

Actually, these three transformations are called the elementary transformations of linear equations.

We know these three basic transformations don’t change the solution of the system of linear equations.

But why?

Let’s give some proofs.

### Proof:

1. Use a non-zero number times an equation.

For a system of linear equations:

$$
\left\{  \begin{array}{}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n = b_1,\\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = b_2, \\
\cdots \\
a_{s1}x_1 + a_{s2}x_2 + \cdots + a_{sn}x_n = b_s
  \end{array} \right.\tag{1}
$$

For convenience, we use k times equation 1 and get a new linear equations system:

$$
\left\{  \begin{array}{}
ka_{11}x_1 + ka_{12}x_2 + \cdots + ka_{1n}x_n = kb_1,\\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = b_2, \\
\cdots \\
a_{s1}x_1 + a_{s2}x_2 + \cdots + a_{sn}x_n = b_s
  \end{array} \right.\tag{2}
$$

Suppose that $(c_1,c_2,\cdots,c_n)$ is a solution of the linear equations system 1. 

The solution satisfies the last $s-1$ equations of $(1)$ and  $(2)$.

Because $(c_1, c_2, \cdots, c_n)$ is a solution of $(1)$.

So we know:

$$
a_{11}c_1 + a_{12}c_2 + \cdots + a_{1n}c_n = b_1.
$$

Then we multiply k on both sides of the equation:

$$
ka_{11}c_1 + ka_{12}c_2 + \cdots + ka_{1n}c_n = kb_1.
$$

This equation tells us that $(c_1, c_2, \cdots, c_n)$ also satisfies the first equation of $(2)$, so $(c_1, c_2, \cdots, c_n)$ is also the solution of $(2)$.

 Similarly, it can be proved that any solution of $(2)$ is also a solution of $(1)$.

1. Add multiples of an equation to another.

The proof of the second elementary transformation is similar to the above.

We also have a linear equations system just like $(1).$

And we might add k times equation 2 to equation 1:

$$
\left\{  \begin{array}{}
(a_{11} + ka_{21})x_1 + (a_{12} + ka_{22})x_2 + \cdots + (a_{1n} + ka_{2n})x_n = b_1+kb_2,\\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = b_2, \\
\cdots \\
a_{s1}x_1 + a_{s2}x_2 + \cdots + a_{sn}x_n = b_s
  \end{array} \right.\tag{3}
$$

$(c_1, c_2, \cdots, c_n)$ is also a solution of $(1)$ and satisfies the last $(s-1)$ equations of $(1)$ and $(3)$.

According to $(1)$, we know:

$$
a_{11}c_1 + a_{12}c_2 + \cdots + a_{1n}c_n=b_1,\\
a_{21}c_1 + a_{22}c_2 + \cdots + a_{2n}c_n=b_2.
$$

Multiply both sides of the second equation by k and add it to the first equation to get:

$$
(a_{11} + ka_{21})x_1 + (a_{12} + ka_{22})x_2 + \cdots + (a_{1n} + ka_{2n})x_n = b_1+kb_2.
$$

So $(c_1, c_2, \cdots, c_n)$ satisfies the first equation of $(3)$.

Similarly, it can be proved that any solution of $(3)$ is also a solution of $(1)$.

So $(1)$ and $(3)$ have the same solution.

As for the third elementary transformation, it is obviously established.

Does every system of linear equations have a solution?

It is obviously not.

So, let’s consider the situation of a linear equation system.

When doing elimination, we use the $x_1$ from the first equation to eliminate the other $x_1$.

Then we use the $x_2$ from the second equation to eliminate the last $x_2$.

Finally, we will get an echelon linear equations system:

$$
\left\{ \begin{array}{}
c_{11}x_1 + c_{12}x_2 + \cdots c_{1r}x_r + \cdots + c_{1n}x_n = d_1,\\
c_{22}x_2 + \cdots + c_{2r}x_r + \cdots + c_{2n}x_n = d_2,\\
\cdots\\
c_{rr}x_r + \cdots + c_{rn}x_n=d_r,\\
0=d_{r+1},\\
0=0,\\
\cdots\\
0=0.
 \end{array} \right.
$$

1. If $d_{r+1}$ is not equal to zero.
    
    The linear equations system has no solution.
    
2. If $d_{r+1}$ is equal to zero. There are two situations.
    1. $r=n$
        
        $$
        \left\{ \begin{array}{}
        c_{11}x_1 + c_{12}x_2 + \cdots c_{1r}x_r + \cdots + c_{1n}x_n = d_1,\\
        c_{22}x_2 + \cdots + c_{2r}x_r + \cdots + c_{2n}x_n = d_2,\\
        \cdots\\
        c_{nn}x_n=d_n,\\
         \end{array} \right., \quad c_{ij} \neq 0(i=1,2,\cdots,n )
        $$
        
        According to the last equation, the $x_n$ can be uniquely determined. Then we can use $x_n$ to solve $x_{n-1}$. Finally, we get the unique solution to the system of linear equations.
        
    2. $r < n$
        
        $$
        \begin{cases}c_{11}x_{1}+c_{12}x_{2}+\cdots+c_{1r}x_{r}+c_{1,r+1}x_{r+1}+\cdots+c_{1n}x_{n}=d_{1},\\c_{22}x_{2}+\cdots+c_{2r}x_{r}+c_{2,r+1}x_{r+1}+\cdots+c_{2n}x_{n}=d_{2},\\\cdots\cdots\cdots\cdots\cdots\\c_{rr}x_{r}+c_{r,r+1}x_{r+1}+\cdots+c_{rn}x_{n}=d_{r},&\end{cases},\quad c_{ij} \neq 0(i=1,2,\cdots,n )
        $$
        
        We can rewrite the equations:
        
        $$
        \left\{ \begin{aligned}&c_{11}x_{1}+c_{12}x_{2}+\cdots+c_{1r}x_{,}=d_{1}-c_{1.r+1}x_{r+1}-\cdots-c_{1n}x_{n},\\&c_{22}x_{2}+\cdots+c_{2r}x_{,}=d_{2}-c_{2.r+1}x_{r+1}-\cdots-c_{2n}x_{n},\\&\cdots\cdots\cdots\cdots\cdots\\&c_{rr}x_{,}=d_{r}-c_{r,r+1}x_{r+1}-\cdots-c_{rn}x_{n}.\end{aligned} \right.
        $$
        
        It can be seen that for any given set of $x_{r+1},\cdots,x_n$, the value of $x_1,x_2,\cdots,x_r$ can be uniquely determined. So this system of linear equations has infinite solutions.
        
        We can express $x_1,x_2,\cdots,x_r$ through $x_{r+1},x_{r+2},\cdots,x_n$. Such a set of expressions is called the general solution of a linear equations system, and $x_{r+1}, \cdots, x_n$ are called free unknowns.
        

Before introducing Theorem 1, I need to declare two concepts.

The linear equations system $(1)$  is called an inhomogeneous system. When the constant terms equal zero, we call the linear equations system a homogeneous system.

## Theorem 1

In a homogeneous linear equations system:

$$
\left\{ \begin{array}{}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n = 0,\\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = 0,\\
\cdots\\
a_{s1}x_1 + a_{s2}x_2 + \cdots + a_{sn}x_n = 0
 \end{array} \right.
$$

If $s < n$, then it must have non-zero solutions.

### Proof:

It is evident that when we use the elimination method to transform the equations into an echelon form, the number of equations in the original form will not increase.

So $r \leq s < n$. From above, we know that if $r < n$, the number of its solutions will not equal one. 

Therefore, there must be a non-zero solution.