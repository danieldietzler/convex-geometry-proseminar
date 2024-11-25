# k-Support Sets

<Definition label="1.10">

A support set $F$ of a closed convex set $A \subset \mathbb{R}^n$ is called a _$k$-convex support set_ if $\dim F = k$, where $k \in \{0, ..., n - 1\}$.
The $1$-support sets of $A$ are called _edges_, and the $(n - 1)$-support sets of $A$ are called _facets_.
Sometimes we also call the support sets of $A$ of dimension $\dim(A) - 1$ facets of $A$.

</Definition>

---

# k-Support Sets

<Theorem label="1.18">

The $0$-support sets of a polytope $P \subset \mathbb{R}^n$ are precisely the sets of the form $\{x\}, x \in \text{vert} P$.

</Theorem>

---

# k-Support Sets


<div class="flex justify-evenly items-center h-full" >
	<div class="flex flex-col items-center w-full" v-click>
		<h4 class="-mb-8">2-Support Set</h4>
		<img src="/2-support_set.svg" class="h-100 w-full" />
	</div>
	<div class="flex flex-col items-center w-full" v-click>
		<h4 class="-mb-8">1-Support Set</h4>
		<img src="/1-support_set.svg" class="h-100 w-full" />
	</div>
	<div class="flex flex-col items-center w-full" v-click>
		<h4 class="-mb-8">0-Support Set</h4>
		<img src="/0-support_set.svg" class="h-100 w-full" />
	</div>
</div>

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

<v-switch>

<template #1>

$\implies$ There is a supporting hyperplane $\{f = \beta\}$ such that $P \subset \{f \leq \beta\}$ and $P \cap \{f = \beta\} = \{x\}$.
</template>
<template #2>

$\implies$ There is a supporting hyperplane $\{f = \beta\}$ such that $P \subset \{f \leq \beta\}$ and $P \cap \{f = \beta\} = \{x\}$. \
This implies that $P \backslash \{x\} = P \cap \{f < \beta\}$ is convex, thus $x \in \text{vert} P$.
</template>

</v-switch>

</div>

<!--
[click]
[click] By definition: P\\{x} convex => x vert
-->

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

<v-switch>

<template #1>

Since $x \in \text{vert} P$, $x \notin Q$.
</template>
<template #2>

Since $x \in \text{vert} P$, $x \notin Q$.
With Theorem 1.14 we get a hyperplane $E = \{f = \alpha\}$ supporting $Q$ and going through $p(Q, x)$.
</template>
<template #3-6>

Since $x \in \text{vert} P$, $x \notin Q$.
With Theorem 1.14 we get a hyperplane $E = \{f = \alpha\}$ supporting $Q$ and going through $p(Q, x)$.
Furthermore, we obtain the supporting halfspace $\{f \leq \alpha\}$ and $\beta := f(x) > \alpha$.
</template>

</v-switch>

<v-click at="4">

$$ 
P \owns y = \sum_{i = 1}^k \alpha_i x_i + \alpha_{k + 1}x, \quad \alpha_i \geq 0, \quad \sum_{i = 1}^{k + 1} \alpha_i = 1
$$

</v-click>

<v-click at="5">
Then (using affine linear properties)

$$
f(y) = \sum_{i = 1}^k \alpha_i \underbrace{f(x_i)}_{\leq \alpha < \beta} + \alpha_{k + 1} f(x) \leq \beta
$$

</v-click>

</div>

<!--
[click] By definition x can't be in the convex hull if x \in vert P
[click] Already seen at the separation theorem
[click]\
[click] Let y \in P as follows \
[click] f(x_i) < \beta, f(x) = \beta
-->

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

<v-switch>

<template #1>

With $f(y) = \beta \iff \alpha_1 = ... = \alpha_k = 0, \alpha_{k + 1} = 1 \; (\iff y = x)$.
</template>

<template #2>

With $f(y) = \beta \iff \alpha_1 = ... = \alpha_k = 0, \alpha_{k + 1} = 1 \; (\iff y = x)$.
$\implies \{f \leq \beta\}$ is a supporting half space and $P \cap \{f = \beta \} = \{x\}$,
concluding that $x$ is a $0$-support set of $P$.
</template>

</v-switch>

</div>

<div class="self-end mt-13 m-6" v-click="2">

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

<!--
So... F is convex
-->

---

# k-Support Sets

Proof 

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

<v-switch>

<template #1>

$x_{m + 1}, ..., x_k \in \{f < \alpha\}$, so $f(x_j) = \alpha - \delta_j, \delta_j > 0, j = m + 1, ..., k$.
</template>
<template #2-4>

$x_{m + 1}, ..., x_k \in \{f < \alpha\}$, so $f(x_j) = \alpha - \delta_j, \delta_j > 0, j = m + 1, ..., k$. \
Let $x \in P$ such that $x = \alpha_1 x_1 + ... + \alpha_k x_k, \alpha_j \geq 0$ and $\alpha_1 + ... + \alpha_k = 1$. Then,
</template>

</v-switch>

<v-click at="2">

$$
f(x) = \alpha_1 f(x_1) + ... + \alpha_k f(x_k) = \alpha - \alpha_{m + 1} \delta_{m + 1} - ... - \alpha_k \delta_k.
$$

</v-click>

<v-click at="3">

In conclusion: $x \in F \iff \alpha_{m + 1} = ... = \alpha_k = 0$.
</v-click>

</div>

<div class="self-end mt-8 m-6" v-click="3">

$\square$

</div>

---

# k-Support Sets

<Theorem label="1.20">

Every polytope $P \subset \mathbb{R}^n$ is a polyhedral set.

</Theorem>

<Definition label="1.5 — Reminder" class="mt-14">

- (a) The intersection of finitely many closed halfspaces is called a _polyhedral set_
- (b) The convex hull of finitely many points $x_1, ..., x_k \in \mathbb{R}^n$ is called a (convex) _polytope_

</Definition>

---

# k-Support Sets

Proof

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.20">

Every polytope $P \subset \mathbb{R}^n$ is a polyhedral set.

</Theorem>
</div>

<div>

We split the cases $\dim P = k < n$ and $\dim P = n$ up.

</div>

---

# k-Support Sets

Proof: $\dim P = k < n$

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.20">

Every polytope $P \subset \mathbb{R}^n$ is a polyhedral set.

</Theorem>
</div>

<div>

<v-switch>

<template #0>

Let $E := \text{aff } P$.
Then, $E = \bigcap_{j = 1}^r \tilde{H}_j$ with $r = 2(n - k)$, $\tilde{H}_i$ halfspaces in $\mathbb{R}^n$.
</template>
<template #1-4>

Let $E := \text{aff } P$.
Then, $E = \bigcap_{j = 1}^r \tilde{H}_j$ with $r = 2(n - k)$, $\tilde{H}_i$ halfspaces in $\mathbb{R}^n$. \
Suppose $P$ is polyhedral in $E$:
</template>

</v-switch>

<v-click at="1">

$$
P = \bigcap_{i = 1}^m H_i
$$
for $H_i \subset E$ $k$-dimensional halfspaces.
</v-click>

<v-click at="2">
$$
P = \bigcap_{i = 1}^m (H_i \oplus E^\perp) \cap E = \bigcap_{i = 1}^m (H_i \oplus E^\perp) \cap \bigcap_{j = 1}^r \tilde{H}_j
$$
</v-click>

<v-click at="3">

$\implies P$ is a polyhedral set in $\mathbb{R}^n$.
</v-click>

</div>

<!--
[click] polyedrisch in E, also P = ... \
[click] E^\perp := linear subspace orthogonal to the linear subspace which spans E
[click] both finitely many halfspaces and then intersection
-->

---

# k-Support Sets

Proof: $\dim P = n$

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.20">

Every polytope $P \subset \mathbb{R}^n$ is a polyhedral set.

</Theorem>
</div>

<div>

Let $F_1, ..., F_m$ be the support sets of $P$, $H_1, ..., H_m$ corresponding supporting halfspaces. \
So: $P \subset H_i$ and $F_i = P \cap \text{bd } H_i$ ($i = 1, ..., m$). Then,

$$
P \subset H_1 \cap ... \cap H_m =: P'
$$

Now, we show that $P = P'$.

<!--
\draw[fill=blue!10,draw=blue] (0, 0) -- (1, 0) -- (2, 1) -- (2, 3) -- (1, 4) -- (0, 2) -- cycle;
\path[fill=orange!40,opacity=.3] (2, -1) -- (2, 5) -- (-1, 5) -- (-1, -1) -- cycle;
\path[fill=black!20,opacity=.4] (1.5, 5) -- (-1, 0) -- (3, -2) -- (5, 3) -- cycle;
-->

<div class="flex w-full justify-end items-center -mt-12">
<v-switch>

<template #1>
<img src="/halfspaces-0.svg" class="h-60"/>
</template>

<template #2>
<img src="/halfspaces-1.svg" class="h-60"/>
</template>

<template #3>

<img src="/halfspaces-2.svg" class="h-60"/>
</template>

</v-switch>
</div>

</div>

<!--
bd == boundary; Rand

\subset weil P \subset H_i
-->

---

# k-Support Sets

Proof: $\dim P = n$

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.20">

Every polytope $P \subset \mathbb{R}^n$ is a polyhedral set.

</Theorem>
</div>

<v-switch>

<template #0>
<div class="flex flex-col">

Assume there ex. a $x \in P'\backslash P$.

<img src="/polytope-polyhedral-1.svg" class="absolute self-center bottom-8"/>
</div>
</template>

<template #1>
<div class="flex flex-col">

Assume there ex. a $x \in P'\backslash P$.
For $y \in \text{int } P$

<img src="/polytope-polyhedral-2.svg" class="absolute self-center bottom-8"/>
</div>
</template>

<template #2>
<div class="flex flex-col">

Assume there ex. a $x \in P'\backslash P$.
For $y \in \text{int } P$ we consider $[y, x]$

<img src="/polytope-polyhedral-3.svg" class="absolute self-center bottom-8"/>
</div>
</template>

<template #3>
<div class="flex flex-col">

Assume there ex. a $x \in P'\backslash P$.
For $y \in \text{int } P$ we consider $[y, x] \cap P$.

<img src="/polytope-polyhedral-4.svg" class="absolute self-center bottom-8"/>
</div>
</template>

<template #4>
<div class="flex flex-col">

Assume there ex. a $x \in P'\backslash P$.
For $y \in \text{int } P$ we consider $[y, x] \cap P$. \
P is compact, convex, and $x \notin P$

<img src="/polytope-polyhedral-4.svg" class="absolute self-center bottom-8"/>
</div>
</template>

<template #5>
<div class="flex flex-col">

Assume there ex. a $x \in P'\backslash P$.
For $y \in \text{int } P$ we consider $[y, x] \cap P$. \
P is compact, convex, and $x \notin P$, thus ex. a $z \in (y, x)$ with $\{z\} = [y, x] \cap \text{bd } P$. 

<img src="/polytope-polyhedral-5.svg" class="absolute self-center bottom-8"/>
</div>
</template>

<template #6>
<div class="flex flex-col">

Assume there ex. a $x \in P'\backslash P$.
For $y \in \text{int } P$ we consider $[y, x] \cap P$. \
P is compact, convex, and $x \notin P$, thus ex. a $z \in (y, x)$ with $\{z\} = [y, x] \cap \text{bd } P$. \
$\overset{\text{Support Thm.}}\implies$ supporting hyperplane of $P$ through $z$.

<img src="/polytope-polyhedral-6.svg" class="absolute self-center bottom-8"/>
</div>
</template>

<template #7>
<div class="flex flex-col">

Assume there ex. a $x \in P'\backslash P$.
For $y \in \text{int } P$ we consider $[y, x] \cap P$. \
P is compact, convex, and $x \notin P$, thus ex. a $z \in (y, x)$ with $\{z\} = [y, x] \cap \text{bd } P$. \
$\overset{\text{Support Thm.}}\implies$ supporting hyperplane of $P$ through $z$.
Thus, we conclude the existence of a support set $F_i$ of $P$ with $z \in F_i \subset \text{bd } H_i$.

<img src="/polytope-polyhedral-6.svg" class="absolute self-center bottom-8"/>
</div>
</template>

<template #8>
<div class="flex flex-col">

Assume there ex. a $x \in P'\backslash P$.
For $y \in \text{int } P$ we consider $[y, x] \cap P$. \
P is compact, convex, and $x \notin P$, thus ex. a $z \in (y, x)$ with $\{z\} = [y, x] \cap \text{bd } P$. \
$\overset{\text{Support Thm.}}\implies$ supporting hyperplane of $P$ through $z$.
Thus, we conclude the existence of a support set $F_i$ of $P$ with $z \in F_i \subset \text{bd } H_i$. \
Also, $y \in \text{int } H_i, x \in P' \subset H_i$ and $z \in (y, x)$ imply that we have a $z \in \text{int } H_i$. Contradiction.

<img src="/polytope-polyhedral-6.svg" class="absolute self-center bottom-8"/>
</div>
</template>

</v-switch>

<!--
\draw[fill=blue!10,draw=blue] (0, 0) -- (1, 0) -- (2, 1) -- (2, 3) -- (1, 4) -- (0, 2) -- cycle;
\filldraw[black] (3, 3) circle (1.5pt) node[below=.2cm] {x};
\filldraw[black] (1, 2) circle (1.5pt) node[below=.2cm] {y};
\draw[black,dotted,thick] (1, 2) -- (3, 3);
\draw[black,thick] (1, 2) -- (2, 2.5);
\filldraw[black] (2, 2.5) circle (1.5pt) node[below right=.05cm] {z};
\draw[gray] (2, -0.5) -- (2, 4.5);
-->

<div class="self-end mt-18 m-6" v-click="8">

$\square$

</div>

<!--
-->