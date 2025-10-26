# Definition of Linear Space and Its Properties 

## Def.1

Let $V$ be a non-empty set, and let $P$ be a number field.

There are two operations:

1. Addition: 
   $$
   \begin{aligned}
   \forall \alpha,\beta \in V, \quad \exist \gamma \in V\\
   s.t. \quad \gamma = \alpha + \beta.
   \end{aligned}
   $$

2. Scalar Multiplication:
   $$
   \begin{aligned}
   \forall k \in P, \forall \alpha \in V, \quad \exist \eta \in V\\
   s.t. \quad \eta = k \cdot \alpha
   \end{aligned}
   $$

If the two operations satisify the following eight axioms.

Then $V$ is called the linear space over field $P$.

- Axioms for addition
  - $\alpha + \beta = \beta + \alpha$
  - $(\alpha + \beta) + \gamma = \alpha + (\beta + \gamma)$
  - $\exist0 \in V, \  s.t. \  \forall \alpha \in V, \alpha + 0 = \alpha$
  - $\forall \alpha \in V, \exist \beta \in V,\ s.t. \ \alpha + \beta = 0$
- Axioms for scalar multiplication 
  - $1\alpha = \alpha$
  - $k(l\alpha) = (kl)\alpha$
  - $k(\alpha + \beta) = k\alpha + k\beta$
  - $(k + l)\alpha = k\alpha + l\alpha$

There are some properties of linear space.

1. Zero element is unique.
   Suppose we have two zero elements $0_1, 0_2$.

   Then, according to $0_1$ is zero element, we have $0_1 + 0_2 = 0_2$

   $0_2$ is also zero element, so, $0_1 + 0_2 = 0_1 = 0_2$.

   So, zero element is unique.

2. Negative element is unique.
   Suppose $\alpha$ have two negative elements $\beta,\gamma$.
   Then we have $\alpha + \beta = 0, \alpha + \gamma = 0$.
   $\beta = \beta + 0 = \beta + (\alpha + \gamma) = (\beta + \alpha) + \gamma = 0 + \gamma = \gamma$.

   So, negative element is unique.

3. $0\alpha = 0, \ k0=0,\  (-1)\alpha = -\alpha$

   - $0\alpha = 0$:
     $$
     \begin{aligned}
     &\alpha + 0\alpha =  1\alpha + 0\alpha = (1+0)\alpha = \alpha\\
     \text{Lefthand:}\quad &\alpha + 0\alpha + (-\alpha) = 0\alpha\\
     \text{Righthand:} \quad &\alpha + (-\alpha) = 0\\
     \text{So}\quad &0\alpha = 0.
     \end{aligned}
     $$

   - $k0 = 0$:
     $$
     \begin{aligned}
     0 + 0 &= 0\\
     k(0 + 0) &= k0\\
     k0 + k0 &= k0\\
     k0 + k0 + (-k0) &= k0 + (-k0)\\
     k0 + (k-k)0 &= (k-k)0\\
     k0 &= 0
     \end{aligned}
     $$

   - $(-1)\alpha = -\alpha$:
     $$
     \begin{aligned}
     \alpha + (-1)\alpha &= 1\alpha + (-1)\alpha = (1-1)\alpha = 0\\
     \text{add}\  &-\alpha\  \text{on both sides}.\\
     (-1)\alpha &= -\alpha
     \end{aligned}
     $$

4. If $k \alpha = 0$, then $k = 0$ or $\alpha = 0$

   If $k \neq 0$, then we have $k^{-1}k\alpha = k^{-1}(k\alpha) = k^{-1}0 = 0$.

   We also have $k^{-1}k\alpha = (k^{-1}k)\alpha = 1\alpha = \alpha$.

   So, $\alpha = 0$.



