# Conditions for Matrix Similarity

## Lemma 1

If we have two $n \times n$ numerical  matrices $P_0$ and $Q_0$, s.t.
$$
\lambda E - A = P_0(\lambda E - B)Q_0
$$
Then $A$ is similar to $B$.

### Pf.

$$
\begin{aligned}
\lambda E - A &= P_0(\lambda E - B)Q_0\\
&= \lambda P_0 Q_0 - P_0 B Q_0
\end{aligned}
$$

Comparing both sides of the equation, we obtain $P_0Q_0 = E, P_0BQ_0 = A$.

So $P_0^{-1} = Q_0$, $A = P_0^{-1}BP_0$.

$A$ is similar to $B$.

## Lemma 2

For any non-zero $n \times n$ numerical matrix $A$ and two $\lambda$-matrices $U(\lambda),V(\lambda)$, there exist two $\lambda$-matrices $Q(\lambda), R(\lambda)$ and two matrices $U_0, R_0$, s.t.
$$
\begin{aligned}
U(\lambda) = (\lambda E - A)Q(\lambda) + U_0,\\
V(\lambda) = R(\lambda)(\lambda E - A) + V_0.
\end{aligned}
$$

### Pf.

Rewrite $U(\lambda)$,
$$
U(\lambda) = D_0 \lambda^m + D_1 \lambda^{m-1} + \dots + D_{m-1} \lambda + D_m,
$$
where $D_0, D_1, \cdots, D_m$ are all $n \times n$ numerical matrices, and $D_0 \neq O$.

If $m = 0$, let $Q(\lambda) = O$ and $U_0 = D_0$. 

These clearly satisfy the requirements of Lemma 2.

Assume $m > 0$. Let
$$
Q(\lambda) = Q_0 \lambda^{m-1} + Q_1 \lambda^{m-2} + \dots + Q_{m-2} \lambda + Q_{m-1},
$$
where $Q_0, Q_1, \cdots, Q_{m-1}$ are numerical matrices to be determined.

Then,
$$
\begin{aligned}
&(\lambda E - A)Q(\lambda)\\
=&Q_0 \lambda^m + (Q_1 - AQ_0)\lambda^{m-1} + \cdots + (Q_k - AQ_{k-1})\lambda^{m-k} + \cdots + (Q_{m-1} - AQ_{m-2})\lambda - AQ_{m-1}.
\end{aligned}
$$
To satisfy equation (2), it suffices to choose:
$$
\begin{aligned}
&Q_0 = D_0, \\
&Q_1 = D_1 + A Q_0, \\
&Q_2 = D_2 + A Q_1, \\
&\qquad\dots\dots\dots \\
&Q_k = D_k + A Q_{k-1}, \\
&\qquad\dots\dots\dots \\
&Q_{m-1} = D_{m-1} + A Q_{m-2},
\end{aligned}
$$
and 
$$
U_0 = D_m + AQ_{m-1}.
$$
Using the same method, we can obtain $R(\lambda)$ and $V_0$.

The proof of the lemma is complete.

## Th.7

Let $A$ and $B$ be two $n \times n$ numerical matrices over the field $P$.

$A$ is similar to $B$ if and only if their characteristic matrices $\lambda E - A$ and $\lambda E - B$ are equivalent.

### Pf.

From the corollary of Theorem 6, we know that $\lambda E - A$ and $\lambda E - B$ are equivalent if and only if there exist invertible $\lambda$-matrices $U(\lambda)$ and $V(\lambda)$ such that:
$$
\lambda E - A = U(\lambda)(\lambda E - B)V(\lambda). \tag1
$$
First, we prove necessity. 

Suppose $A$ and $B$ are similar, meaning there exists an invertible matrix $T$ such that 
$$
A = T^{-1}BT.
$$
Then,
$$
\lambda E - A = \lambda E - T^{-1}BT = T^{-1}(\lambda E - B)T,
$$
which implies that $\lambda E - A$ and $\lambda E - B$ are equivalent.

Next, we prove sufficiency. 

Suppose $\lambda E - A$ and $\lambda E - B$ are equivalent, meaning there exist invertible $\lambda$-matrices $U(\lambda), V(\lambda)$ such that (1) holds.

Using Lemma 2, there exist $\lambda$-matrices $Q(\lambda)$ and $R(\lambda)$, as well as numerical matrices $U_0$ and $V_0$, such that:
$$
\begin{aligned} U(\lambda) &= (\lambda E - A)Q(\lambda) + U_0, \quad &(2) \\ V(\lambda) &= R(\lambda)(\lambda E - A) + V_0. \quad &(3) \end{aligned}
$$
Rewrite (1) as:
$$
U(\lambda)^{-1}(\lambda E - A) = (\lambda E - B)V(\lambda),
$$
Substitute $V(\lambda)$ from (3) into this equation, and then rearrange the terms to obtain:
$$
[U(\lambda)^{-1} - (\lambda E - B)R(\lambda)](\lambda E - A) = (\lambda E - B)V_0.
$$
The degree of the right-hand side is 1 or $V_0 = O$.

Therefore, $U(\lambda)^{-1} - (\lambda E - B)R(\lambda)$ is a numerical matrix. 

Let us denote it by $T$, i.e.,
$$
T = U(\lambda)^{-1} - (\lambda E - B)R(\lambda),\\
T(\lambda E - A) = (\lambda E - B)V_0. \tag4
$$
Now we proceed to prove that $T$ is invertible. From the first equation of (4), we have:
$$
\begin{aligned} E &= U(\lambda)T + U(\lambda)(\lambda E - B)R(\lambda) \\ &= U(\lambda)T + (\lambda E - A)V(\lambda)^{-1}R(\lambda) \\ &= [(\lambda E - A)Q(\lambda) + U_0]T + (\lambda E - A)V(\lambda)^{-1}R(\lambda) \\ &= U_0 T + (\lambda E - A)[Q(\lambda)T + V(\lambda)^{-1}R(\lambda)]. \end{aligned}
$$
The second term on the right side of the equation must be zero; otherwise, its degree would be at least 1. 

Since $E$ and $U_0 T$ are both numerical matrices, the equation would not hold. 

Thus,
$$
E = U_0 T,
$$
which means that $T$ is invertible. 

From the second equation of (4), we obtain:
$$
\lambda E - A = T^{-1}(\lambda E - B)V_0.
$$
Applying Lemma 1 again, $A$ and $B$ are similar.

## Co.

$A$ is similar to $B$ if and only if they have the same invariant factors.