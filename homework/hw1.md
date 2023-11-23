

Let $K := S^n_+$ denote the set of symmetric positive semi-definite matrices in $R^{n \times n}$.

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

for some $\alpha_1, \alpha_2$. And since matrix multiplication is distributive, we have that
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

Then $\lambda \mathbf M_1 + (1-\lambda) \mathbf M_2$ is also positive semi-definite and therefore in $K$, meaning $K$ is convex.


**(iii) Proof that $K$ is closed.**

To show that $K$ is closed, we want to show that
$$
\begin{align}
    K = cl K = \{\mathbf M \in S_n : K \cap N_\varepsilon(\mathbf M) \ne \varnothing, \varepsilon > 0\},
\end{align}
$$
where the $\varepsilon$-neighborhood for $\varepsilon > 0$ is defined as
$$
\begin{align}
    N_\varepsilon(\mathbf M) =
    \{
        \mathbf A \in S_n : d(\mathbf A, \mathbf M) =  \sqrt{\text{Tr}\mathbf{[(A-M)(A-M)]}} < \varepsilon
    \}.
\end{align}
$$

Note these standard properties of trace for any matrices $\mathbf X, \mathbf Y \in S^n$:
$$
\begin{align}
    \text{Tr}(\mathbf X + \mathbf Y)
    &=
    \text{Tr}\mathbf X + \text{Tr}\mathbf Y
    ,
    \\
    \text{Tr}\mathbf{XY}
    &=
    \text{Tr}\mathbf{YX}
    .
\end{align}
$$

Let $\epsilon > 0$ and let $\mathbf A \in N_\varepsilon(\mathbf M)$. Then we have that
$$
\begin{align}
    \varepsilon^2 >
    \text{Tr}[\mathbf{(A-M)(A-M)}]
    &=
    \text{Tr}[\mathbf{(AA - AM - MA + MM)}]
    \\
    &=
    \text{Tr}\mathbf{AA}
    - \text{Tr}\mathbf{AM}
    - \text{Tr}\mathbf{MA}
    + \text{Tr}\mathbf{MM}
    \\
    &=
    \text{Tr}\mathbf{AA}
    - 2\text{Tr}\mathbf{AM}
    + \text{Tr}\mathbf{MM}
\end{align}
$$


<!-- 
$$
\begin{align}
    
\end{align}
$$
-->
