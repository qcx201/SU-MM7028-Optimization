

Let $K := S^n_+$ denote the set of positive semi-definite matrices in $R^{n \times n}$.

Then for all matrices $\mathbf M \in K$, by definition of being semi-positive
$$
\begin{align}
    \forall \mathbf x \in \mathbb R^n,
    \quad
    \mathbf x' \mathbf M \mathbf x \ge 0.
\end{align}
$$


**(i) Proof that $K$ is a cone.**

Let $\lambda \ge 0$. To show that $K$ is a cone, we will show that for any $\mathbf M \in K, \; \lambda \mathbf M \in K$, i.e. $\lambda \mathbf M$ is still semi-positive.

Let $\mathbf M$ be any semi-positive matrix in $K$ and let $\mathbf x$ be any vector in $\mathbb R^n$. Then since $\mathbf M$ is semi-positive, we have that
$$
\begin{align}
    \exists \alpha \ge 0,
    \quad
    \mathbf{x' M x} = \alpha.
\end{align}
$$

Then since $\lambda \ge 0$ and $\alpha \ge 0$, we have that
$$
\begin{align}
    \mathbf x' (\lambda \mathbf M) \mathbf x
    =
    \lambda (\mathbf x' \mathbf M \mathbf x)
    =
    \lambda \alpha
    \ge
    0,
\end{align}
$$
then $\lambda \mathbf M$ is semi-definite and $\lambda \mathbf M \in K$.


**(ii) Proof that $K$ is a convex.**

To show that $K$ is convex, we want to show that
$$
\begin{align}
    \forall \mathbf M_1, \mathbf M_2 \in K,
    \quad
    \forall \lambda \in [0, 1],
    \quad
    \lambda \mathbf M_1 + (1-\lambda) \mathbf M_2 \in K.
\end{align}
$$

Let $\lambda \in [0, 1]$. Then we have that $1 - \lambda \in [0, 1]$ and so both $\lambda \ge 0$ and $(1-\lambda) \ge 0$. Then with the same argument from **(i)**, both $\lambda \mathbf M_1$ and $(1-\lambda) \mathbf M_2$ are semi-positive. Then for any $\mathbf x \in \mathbb R$, we have that

$$
\begin{align}
    \mathbf x' \lambda \mathbf M_1 \mathbf x = \alpha_1 \ge 0,
    \quad
    \mathbf x' (1-\lambda) \mathbf M_1 \mathbf x = \alpha_2 \ge 0,
\end{align}
$$

and since matrix multiplication is distributive,
$$
\begin{align}
    \mathbf x' [\lambda \mathbf M_1 + (1-\lambda) \mathbf M_2] \mathbf x
    &=
    \mathbf x' \lambda \mathbf M_1 \mathbf x
    +
    \mathbf x' (1-\lambda) \mathbf M_2 \mathbf x
    \\
    &=
    \alpha_1 + \alpha_2
    \ge 0.
\end{align}
$$

Thus $\lambda \mathbf M_1 + (1-\lambda) \mathbf M_2$ is also positive semi-definite and in $K$, meaning $K$ is convex.


**(iii) Proof that $K$ is closed.**

To show that $K$ is closed, we want to show that
$$
\begin{align}
    
\end{align}
$$


<!-- 
$$
\begin{align}
    
\end{align}
$$
-->
