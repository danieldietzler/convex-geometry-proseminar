# k-Support Sets

<Definition label="1.10">

A support set $F$ of a closed convex set $A \subset \mathbb{R}^n$ is called a *$k$-convex support set* if $\dim F = k$, where $k \in \{0, ..., n - 1\}$.
The $1$-support sets of $A$ are called *edges*, and the $(n - 1)$-support sets of $A$ are called *facets*.
Sometimes we also call the support sets of $A$ of dimension $\dim(A) - 1$ facets of $A$.

</Definition>

---

# k-Support Sets

<Theorem label="1.18">

The $0$-support sets of a polytope $P \subset \mathbb{R}^n$ are precisely the sets of the form $\{x\}, x \in \text{vert} P$.

</Theorem>

---

# k-Support Sets
Proof: "$\Rightarrow$"

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.18">

The $0$-support sets of a polytope $P \subset \mathbb{R}^n$ are precisely the sets of the form $\{x\}, x \in \text{vert} P$.

</Theorem>
</div>

<div class="-mt-10">

Let $\{x\}$ be a $0$-support set of $P$.

$\implies$ There is a supporting hyperplane $\{f = \beta\}$ such that $P \subset \{f \leq \beta\}$ and $P \cap \{f = \beta\} = \{x\}$. \
This implies that $P \backslash \{x\} = P \cap \{f < \beta\}$ is convex, thus $x \in \text{vert} P$.

</div>

---

# k-Support Sets
Proof: "$\Leftarrow$"

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.18">

The $0$-support sets of a polytope $P \subset \mathbb{R}^n$ are precisely the sets of the form $\{x\}, x \in \text{vert} P$.

</Theorem>
</div>

<div class="-mt-10">

Let $x \in \text{vert}P$ and $(\text{vert}P) \backslash \{x\}$ \
$= \{x_1, ..., x_k\}, k \geq 1$ ($\text{vert}P = \{x\}$ trivial).
$Q := \text{conv}\{x_1, ..., x_k\}$

Since (?) $x \notin Q$.
With Theorem 1.14 we once again get a hyperplane $E = \{f = \alpha\}$ supporting $Q$ and going through $p(Q, x)$.
Furthermore, we obtain the supporting halfspace $\{f \leq \alpha\}$ and $\beta := f(x) > \alpha$.

$$
P \owns y = \sum_{i = 1}^k \alpha_i x_i + \alpha_{k + 1}x, \quad \alpha_i \geq 0, \quad \sum_{i = 1}^{k + 1} \alpha_i = 1
$$
Then (using affine linear properties)

$$
f(y) = \sum_{i = 1}^k \alpha_i \underbrace{f(x_i)}_{\leq \alpha < \beta} + \alpha_{k + 1} f(x) \leq \beta
$$

</div>

---

# k-Support Sets
Proof: "$\Leftarrow$"

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.18">

The $0$-support sets of a polytope $P \subset \mathbb{R}^n$ are precisely the sets of the form $\{x\}, x \in \text{vert} P$.

</Theorem>
</div>

<div class="mt-4">

$$
f(y) = \sum_{i = 1}^k \alpha_i \underbrace{f(x_i)}_{\leq \alpha < \beta} + \alpha_{k + 1} f(x) \leq \beta
$$
With $f(y) = \beta \iff \alpha_1 = ... = \alpha_k = 0, \alpha_{k + 1} = 1 \; (\iff y = x)$.
$\implies \{f \leq \beta\}$ is a supporting half space and $P \cap \{f = \beta \} = \{x\}$,
concluding that $x$ is a $0$-support set of $P$.
</div>

<div class="self-end mt-13 m-6">

$\square$
</div>

---

# k-Support Sets

<Remark label="1.22">

In the following, we will no longer distinguish strictly between $0$-support sets and vertices, although the former are sets consisting of one point and the latter are points.

</Remark>

---

# k-Support Sets

<Theorem label="1.19">

Let $P \subset \mathbb{R}^n$ be a polytope with $\text{vert} P = \{x_1, ..., x_k\}$ and let $F$ be a support set of $P$. \
Then $F = \text{conv}\{x_i : x_i \in F\}$.

</Theorem>

<Remark label="1.23">

Theorem 1.19 implies, in particular, that a support set of a polytope is a polytope and there are only finitely many support sets.

</Remark>

---

# k-Support Sets
Proof: "$\Leftarrow$"

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.19">

Let $P \subset \mathbb{R}^n$ be a polytope with $\text{vert} P = \{x_1, ..., x_k\}$ and let $F$ be a support set of $P$. \
Then $F = \text{conv}\{x_i : x_i \in F\}$.

</Theorem>
</div>

<div class="-mt-24">

We assume the usual separation \
$F = P \cap \{f = \alpha\}$ and $P \subset \{f \leq \alpha\}$. \
$x_1, ..., x_m \in F$ for some $m \in \{1, ..., k\}$, \
$x_{m + 1}, ..., x_k \notin F$ (w.l.o.g)

$x_{m + 1}, ..., x_k \in \{f < \alpha\}$, so $f(x_j) = \alpha - \delta_j, \delta_j > 0, j = m + 1, ..., k$. \
Let $x \in P$ such that $x = \alpha_1 x_1 + ... + \alpha_k x_k, \alpha_j \geq 0$ and $\alpha_1 + ... + \alpha_k = 1$. Then, 

$$
f(x) = \alpha_1 f(x_1) + ... + \alpha_k f(x_k) = \alpha - \alpha_{m + 1} \delta_{m + 1} - ... - \alpha_k \delta_k.
$$

In conclusion: $x \in F \iff \alpha_{m + 1} = ... = \alpha_k = 0$.

</div>

<div class="self-end mt-8 m-6">

$\square$
</div>


---

# k-Support Sets

<Theorem label="1.20">

Every polytope $P \subset \mathbb{R}^n$ is a polyhedral set.

</Theorem>
