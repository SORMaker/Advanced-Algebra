# Chapter4-5

Matrix partitioning

Let $A = (a_{ik})_{s \times n}, \ B = (b_{kj})_{n \times m}$ .

We can partition matrices A and B into blocks.
$$
\begin{gathered}n_{1}\quad n_{2}\quad\cdots\quad n_{l}\\\mathbf{A}=\begin{array}{c}s_{1}\\s_{2}\\\vdots\\s_{t}\end{array}\begin{bmatrix}\mathbf{A}_{11}&\mathbf{A}_{12}&\cdots&\mathbf{A}_{11}\\\mathbf{A}_{21}&\mathbf{A}_{22}&\cdots&\mathbf{A}_{2l}\\\vdots&\vdots&&\vdots\\\mathbf{A}_{t1}&\mathbf{A}_{t2}&\cdots&\mathbf{A}_{tl}\end{bmatrix},\end{gathered},\\
\begin{gathered}
\quad \quad \quad m_{1}\quad m_{2}\quad\cdots\quad m_{r
}\\
\mathbf{B}=\begin{array}{c}n_{1}\\n_{2}\\\vdots\\n_{l}\end{array}\begin{bmatrix}\mathbf{B}_{11}&\mathbf{B}_{12}&\cdots&\mathbf{B}_{1r}\\\mathbf{B}_{21}&\mathbf{B}_{22}&\cdots&\mathbf{B}_{2r}\\\vdots&\vdots&&\vdots\\\mathbf{B}_{l1}&\mathbf{B}_{l2}&\cdots&\mathbf{B}_{lr}\end{bmatrix},
\end{gathered}.
$$

$A_{ij}$ are $s_i \times n_j$ matrices and $B_{ij}$ are $n_i \times m_j$ matrices.

So we have $C$.
$$
\begin{gathered}
\quad \quad \quad\quad\quad\quad \quad m_{1} \quad m_{2}\quad\cdots\quad m_{r}\\
\mathbf{C}=\mathbf{AB}=\begin{array}{c}s_{1}\\s_{2}\\\vdots\\s_{t}\end{array}\begin{bmatrix}\mathbf{C}_{11}&\mathbf{C}_{12}&\cdots&\mathbf{C}_{1r}\\\mathbf{C}_{21}&\mathbf{C}_{22}&\cdots&\mathbf{C}_{2r}\\\vdots&\vdots&&\vdots\\\mathbf{C}_{t1}&\mathbf{C}_{t2}&\cdots&\mathbf{C}_{tr}\end{bmatrix},
\end{gathered}
$$
And $C_{pq} = \sum_{k=1}^l A_{pk}B_{kq}, \quad p = 1,2,\cdots,t;q=1,2,\cdots,r.$

There give us a different way to understand matrices multiplication.

We use the set of row vectors of $B$  to represent matrix $B$.
$$
B = \left[ \begin{array}{} 
B_1 \\
B_2 \\
\vdots \\
B_m
\end{array}   \right]
$$
So
$$
AB = \left[ \begin{array}{} 
a_{11} & a_{12} & \cdots & a_{1m}\\
a_{21} & a_{22} & \cdots & a_{2m}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nm}
\end{array}   \right]
\left[ \begin{array}{} 
B_1 \\
B_2 \\
\vdots \\
B_m
\end{array}   \right]
=
\left[ \begin{array}{} 
a_{11}B_1 + a_{12}B_2 + \cdots + a_{1m}B_m \\
a_{21}B_1 + a_{22}B_2 + \cdots + a_{2m}B_m \\
\cdots\cdots\cdots \\
a_{n1}B_1 + a_{n2}B_2 + \cdots + a_{nm}B_m
\end{array}   \right]
$$
Furthermore matrix $A$ ban be represented by the set of column vectors of $A$.
$$
A = \left[ \begin{array}{} A_1 & A_2 & \cdots & A_m \end{array}   \right]
$$
So
$$
AB = \left[ \begin{array}{} A_1 & A_2 & \cdots & A_m \end{array}   \right]
\left[ \begin{array}{} 
b_{11} & b_{12} & \cdots & b_{1s}\\
b_{21} & b_{22} & \cdots & b_{2s}\\
\vdots & \vdots & & \vdots\\
b_{m1} & b_{m2} & \cdots & b_{ms}
\end{array}   \right]
= \\
\left[ \begin{array}{} 
b_{11}A_1 + b_{21}A_2 + \cdots + b_{m1}A_m &
\cdots &
b_{1s}A_1 + b_{2s}A_2 + \cdots + b_{ms}A_s
\end{array}   \right]
$$

If we have a matrix of form like that
$$
A = \left[ \begin{array}{} 
A_1 & & & O\\
& A_2 & & \\
& & \ddots & \\
 O & & & A_l
\end{array} \right]
$$
And $A_i(i=1,2,\cdots,l)$ is $n_i \times n_i$ matrices, then we called A a block diagonal matrix.

Obviously,
$$
AB = \left[ \begin{array}{} 
A_1B_1 & & & O\\
& A_2B_2 & & \\
& & \ddots & \\
 O & & & A_lB_l
\end{array} \right],\\
A+B = \left[ \begin{array}{} 
A_1+B_1 & & & O\\
& A_2+B_2 & & \\
& & \ddots & \\
 O & & & A_l+B_l
\end{array} \right]
$$
Moreover, if $A_i$ are all invertible, then:
$$
\left[ \begin{array}{} 
A_1 & & & O\\
& A_2 & & \\
& & \ddots & \\
 O & & & A_l
\end{array} \right]^{-1} = \left[ \begin{array}{} 
A_1^{-1} & & & O\\
& A_2^{-1} & & \\
& & \ddots & \\
 O & & & A_l^{-1}
\end{array} \right]
$$
