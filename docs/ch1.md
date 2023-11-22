
# Chapter 2: Convex Sets

## Section 2.1: Convex Hulls

### Definition 2.1.1 (Convexity).

<details>
<summary><b>Convex set</b></summary><br>

A set $S \subset \mathbb{R}^n$ is ***convex*** if the ***line segement*** joining any two points in the set is also in the set:
$$
    \forall \mathbf{x_1, x_2} \in S, \quad
    \forall \lambda \in [0, 1], \quad
    \lambda \mathbf{x_1} + (1-\lambda) \mathbf{x_2} \in S.  
$$
</details>

<details>
<summary><b>Convex, affine, and linear combinations</b></summary><br>

Weighted averages of the form
$$
    \sum_{j=1}^k \lambda_j \mathbf{x_j},
    \quad
    \sum_{j=1}^k \lambda_j = 1,
    \quad
    \lambda_j \ge 0,\; j = 1, ..., k,
$$
are called ***convex combinations*** of $\mathbf{x_1, ..., x_k} \in S$. Convex combinations are of course contained in $S$ if $S$ is **convex.**

If $\lambda_j$ can be negative, the combination is called an ***affine combination.***

If $\lambda_j \in \mathbb{R}$, the combination is simply called a ***linear combination.***

</details>


### Lemma 2.1.2 (Properties of convex sets).

<details>
<summary><b>Properties of convex sets</b></summary><br>

Let $S_1, S_2$ be convex sets in $R^n$. Then

1. $S_1 \cap S_2$ is convex.
2. $S_1 \oplus S_2 = \{x_1 + x_2 : x_1 \in S_1, x_2 \in S_2\}$ is convex.
3. $S_1 \ominus S_2 = \{x_1 - x_2 : x_1 \in S_1, x_2 \in S_2\}$ is convex.

**Proof.** Left as exercise.

</details>

### Definition 2.1.3 (Convex hulls).

<details>
<summary><b>Convex hulls</b></summary><br>

Let $S \subseteq \mathbb R^n$ (not necessarily convex). The ***convex hull*** of $S$, denoted $conv(S)$, is the collection of all **convex combinations** of $S$:
$$
    conv(S)
    =
    \left\{
        \sum_{j=1}^k \lambda_j \mathbf{x_j}
        \;
        \bigg|
        \;
        \lambda_1, ..., \lambda_k \in [0, 1], \; \sum_{j=1}^k \lambda_j = 1,
        \quad
        \mathbf{x_1, ..., x_k} \in S
    \right\}.
$$
<!-- or
$$
    \mathbf{x} \in conv(S)
    \iff
    \exists \lambda_1, ..., \lambda_k \in [0, 1], \; \sum_{j=1}^k \lambda_j = 1,
    \quad
    \exists \mathbf{x_1, ..., x_k} \in S,
    \quad
    \mathbf{x} = \sum_{j=1}^k \lambda_j \mathbf{x_j}.
$$ -->

</details>

### Lemma 2.1.4 (convex hull is minimal).

<details>
<summary><b>Conv(S) is the minimal convex set containing S</b></summary><br>

Let $S \subseteq R^n$ (not necessarily convex). Then $conv(S)$ is the intersecion of all convex sets containing $S$, i.e. the "smallest" convex set containing $S$.

**Proof.** Left as exercise.

</details>

### Definition 2.1.5 (polytope).

<details>
<summary><b>Polytope</b></summary><br>

The **convex hull** of a finite number of points $S = \{\mathbf x_1, ..., \mathbf x_{k+1}\} \subset \mathbb{R}^n$ is called a ***polytope***.

</details>

<details>
<summary><b>Affine independence and simplex</b></summary><br>

If $\mathbf x_1, ..., \mathbf x_{k+1}$ are ***affinely independent***, meaning
$$
    x_2 - x_1, \; x_3 - x_1, \; ..., \; x_{k+1} - x_1
$$
are linearly independent, then $conv(\mathbf x_1, ..., \mathbf x_{k+1})$ is called a ***simplex*** having vertices $\mathbf x_1, ..., \mathbf x_{k+1}$.

Since there are only $n$ linearly independent vectors in $R^n$, there can be no simplex in $R^n$ with more than $n+1$ vertices.

</details>

### Theorem 2.1.6 (Carathéodory).

<details>
<summary><b>Carathéodory theorem</b></summary><br>

Let $S \subseteq R^n$. If $\mathbf x \in conv(S)$, then $\mathbf x \in conv(\mathbf x_1, ..., \mathbf x_{n+1})$ where $\mathbf x_j \in S$ for $j = 1, ..., n+1$.

In other words, $\mathbf x$ can be represented as
$$
    \mathbf x = \sum_{j=1}^{n+1} \lambda_j \mathbf x_j,
    \quad
    \sum_{j=1}^{n+1} \lambda_j = 1,
    \quad
    \lambda_j \ge 0, \;
    \mathbf x_j \in S, \;
    j = 1, ..., n+1.
$$

Any point in a convex hull can be represented as a convex combination of a finite number of points in $S$ (an element of an polytope of points in $S$).

**Proof.** See page 44 of *Bazara et el.*

</details>


## Section 2.2: Closure and interior of a set

### Definition 2.2.1 (closure).

<details>
<summary><b>
Closure
</b></summary><br>

Let $S \subseteq R^n$. A point $\mathbf x$ is in the ***closure*** of $S$, denoted $cl S$, if for every $\varepsilon > 0$,
$$
    S \cap N_\varepsilon(\mathbf x) \ne \varnothing,
    \quad
    N_\epsilon(\mathbf x)
    =
    \{
        \mathbf y \in \mathbb R :
        || \mathbf y - \mathbf x || < \varepsilon
    \}.
$$

Here $N_\epsilon(\mathbf x)$ is the $\epsilon$-neighborhood or open ball of $\mathbf x$ with radius $\epsilon$.

In other words,
$$
    cl S
    =
    \{
        \mathbf x \in \mathbb R^n
        :
        S \cap N_\varepsilon (\mathbf x) \ne \varnothing,\; \varepsilon > 0
    \}.
$$

If $S = cl S$, then $S$ is called ***closed***.

</details>

<details>
<summary><b>
Interior, solid, open, and boundary
</b></summary><br>

A point $\mathbf x$ is in the ***interior*** of $S$, denoted $int S$, if $N_\varepsilon(x) \subset S$ for some $\varepsilon > 0$.
$$
    int S = \{\mathbf x \in \mathbb R^n : N_\varepsilon(\mathbf x) \subset S, \varepsilon > 0\}.
$$

A ***solid set*** $S \subseteq \mathbb R^n$ is one having an nonempty interior.

If $S = int S$, then $S$ is called ***open.***

If for every $\varepsilon > 0$, $N_\varepsilon(\mathbf x)$ contains one point in $S$ and one point not in $S$, then $\mathbf x$ is said to be in the ***boundary*** of $S$, denoted $\partial S$.

</details>


### Theorem 2.2.2 (Line segements between cl S and int S).

<details>
<summary><b>
Line segements between points in cl S and int S are interior
</b></summary><br>

Let $S \subseteq R^n$ be a convex set with an nonempty interior.

Let $\mathbf x_1 \in cl S$ and $\mathbf x_2 \in int S$.

Then $\lambda \mathbf x_1 + (1-\lambda) \mathbf x_2 \in int S$ for each $\lambda \in (0 ,1)$.

**Proof.** See page 46.

</details>

### Corollary 1 (int S is convex).
<details>
<summary><b>
int S of convex S is convex
</b></summary><br>

Let $S$ be a convex set. Then $int S$ is convex.

**Proof.** Exercise.

</details>

### Corollary 2 (cl S is convex).
<details>
<summary><b>
int S of convex S is convex
</b></summary><br>

Let $S$ be a convex set with a nonempty interior. Then $cl S$ is convex.

**Proof.** See page 47.

</details>

### Corollary 3 (cl (int S) = cl S).
<details>
<summary><b>
cl (int S) = cl S
</b></summary><br>

Let $S$ be a convex set with a nonempty interior. Then $cl(int S) = cl S$.

**Proof.** See page 48.

</details>

### Corollary 4 (int (cl S) = int S).
<details>
<summary><b>
int (cl S) = int S
</b></summary><br>

Let $S$ be a convex set with a nonempty interior. Then $int(cl S) = int S$.

**Proof.** See page 48.

</details>

## Section 2.3: Weiesterass's theorem

### Definitions (inf, sup)
<details>
<summary><b>
Min and inf
</b></summary><br>

For a function $f : S \to \mathbb R$,
we say $\mathbf {\bar x}$ solves $\min\{f(\mathbf x) : \mathbf x \in S\}$ if
$$
    \forall \mathbf x \in S,
    \quad
    f(\mathbf {\bar x}) \le f(\mathbf x).
$$
In such a case, we say that a ***minimum exists***.

We say that $\alpha = \inf \{f(\mathbf x) : \mathbf x \in S\}$ if $\alpha$ is the greatest lower bound:
$$
    \forall \mathbf x \in S,
    \quad
    \alpha \le f(\mathbf x)
    \quad
    \land
    \quad
    \nexists \bar \alpha > \alpha, \quad
    \bar \alpha \le f(\mathbf x).
$$

</details>

<!-- 
<details>
<summary><b>

</b></summary><br>

</details>
 -->
