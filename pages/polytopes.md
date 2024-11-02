# Polytopes

<Definition label="1.10">

A support set $F$ of a closed convex set $A \subset \mathbb{R}^n$ is called a *$k$-convex support set* if $\dim F = k$, where $k \in \{0, ..., n - 1\}$.
The $1$-support sets of $A$ are called *edges*, and the $(n - 1)$-support sets of $A$ are called *facets*.
Sometimes we also call the support sets of $A$ of dimension $\dim(A) - 1$ facets of $A$.

</Definition>

---

# Polytopes

<Theorem label="1.18">

The $0$-support sets of a polytope $P \subset \mathbb{R}^n$ are precisely the sets of the form $\{x\}, x \in \text{vert} P$.

</Theorem>

---

# Polytopes
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