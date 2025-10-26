# Basis Transformation and Coordinates Transformation

Let $V$ be an n-dimensional linear space.

We have two bases $\epsilon_1, \epsilon_2, \cdots, \epsilon_n$ and $\epsilon_1', \epsilon_2', \cdots, \epsilon_n'$ for $V$.

Their relationship is 
$$
\begin{bmatrix}\epsilon_1', \epsilon_2', \cdots, \epsilon_n' \end{bmatrix} = \begin{bmatrix}\epsilon_1, \epsilon_2, \cdots, \epsilon_n \end{bmatrix}
\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn}\\
\end{bmatrix}\\
=\begin{bmatrix}\epsilon_1, \epsilon_2, \cdots, \epsilon_n \end{bmatrix}A
$$
The matrix $A$ is called the transition matrix from $\begin{bmatrix}\epsilon_1, \epsilon_2, \cdots, \epsilon_n \end{bmatrix}$ to $\begin{bmatrix}\epsilon_1', \epsilon_2', \cdots, \epsilon_n' \end{bmatrix}$.

$A$ is invertible.

This is the basis transformation.

Let the coordinates of the vector $\alpha$ relative to these two bases be $x_1,x_2,\cdots,x_n$ and $x_1',x_2',\cdots, x_n'$.

Then, 
$$
\begin{aligned}
\alpha &= x_1\epsilon_1 + x_2\epsilon_2 + \cdots + x_n\epsilon_n = \begin{bmatrix}\epsilon_1, \epsilon_2, \cdots, \epsilon_n  \end{bmatrix} \begin{bmatrix}x_1\\x_2\\\vdots\\x_n \end{bmatrix}\\
&= x_1'\epsilon_1' + x_2\epsilon_2' + \cdots + x_n'\epsilon_n'=\begin{bmatrix}\epsilon_1', \epsilon_2', \cdots, \epsilon_n'  \end{bmatrix} \begin{bmatrix}x_1'\\x_2'\\\vdots\\x_n' \end{bmatrix}\\
\end{aligned}
$$
We know $\begin{bmatrix}\epsilon_1', \epsilon_2', \cdots, \epsilon_n' \end{bmatrix} = \begin{bmatrix}\epsilon_1, \epsilon_2, \cdots, \epsilon_n \end{bmatrix}A$.

So
$$
\alpha 
=\begin{bmatrix}\epsilon_1', \epsilon_2', \cdots, \epsilon_n'  \end{bmatrix} \begin{bmatrix}x_1'\\x_2'\\\vdots\\x_n' \end{bmatrix}
=\begin{bmatrix}\epsilon_1, \epsilon_2, \cdots, \epsilon_n \end{bmatrix}A\begin{bmatrix}x_1'\\x_2'\\\vdots\\x_n' \end{bmatrix}
=\begin{bmatrix}\epsilon_1, \epsilon_2, \cdots, \epsilon_n  \end{bmatrix} \begin{bmatrix}x_1\\x_2\\\vdots\\x_n \end{bmatrix}.
$$
So 
$$
\begin{aligned}
\begin{bmatrix}x_1\\x_2\\\vdots\\x_n \end{bmatrix}&=A\begin{bmatrix}x_1'\\x_2'\\\vdots\\x_n' \end{bmatrix}\\
\begin{bmatrix}x_1'\\x_2'\\\vdots\\x_n' \end{bmatrix} &= A^{-1}\begin{bmatrix}x_1\\x_2\\\vdots\\x_n \end{bmatrix}
\end{aligned}
$$
