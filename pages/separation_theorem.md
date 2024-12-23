# Separation Theorem

<Theorem label="1.17 (Separation Theorem)">

Let $A, B \subset \mathbb{R}^n$ be nonempty and convex sets in $\mathbb{R}^n$.
Then

$$
\text{relint} A \cap \text{relint} B = \emptyset
$$

iff. $A$ and $B$ can be properly separated.

</Theorem>

---

# Separation Theorem

<div class="flex justify-center items-center h-full">
	<img src="/convex_no_labels.svg" class="h-100"/>
	<div class="h-full w-0.5 bg-black/30 rounded-full -mx-8.5" />
	<img src="/convex_no_labels.svg" class="h-100"/>
</div>

---

# Separation Theorem

<div class="flex justify-center items-center h-full">
	<img src="/convex_no_labels.svg" class="h-100"/>
	<div class="h-full w-0.5 bg-black/30 rounded-full -mx-18" />
	<img src="/convex_no_labels.svg" class="h-100"/>
</div>

<div v-click class="h-100 w-0.5 bg-black/30 rounded-full absolute top-12 left-120 rotate-45" />
<div v-click class="h-100 w-0.5 bg-black/30 rounded-full absolute top-45 left-130 -rotate-70" />

---

# Separation Theorem

Proof: "$\Rightarrow$"

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.17 (Separation Theorem)">

Let $A, B \subset \mathbb{R}^n$ be nonempty and convex sets in $\mathbb{R}^n$.
Then

$$
\text{relint} A \cap \text{relint} B = \emptyset
$$

iff. $A$ and $B$ can be properly separated.

</Theorem>
</div>
<div class="-mt-20">


Suppose $\text{relint} A \cap \text{relint} B = \emptyset$.
<div v-click> 

Then, $\text{relint} A - \text{relint} B \not \owns 0$ follows. (\*) 
</div> 
<div v-click>

$\overset{\text{Ex 1.3.3 (a)}}{\implies} 0 \notin \text{relint}(A - B)$
</div>

</div>

<div v-click class="mt-16">

(\*) Let $P := \text{relint} A, Q := \text{relint} B$. $P - Q = \{p - q : p \in P, \; q \in Q\}$. \
Thus, clearly $0 \in P - Q \iff \exists p \in P, q \in Q: p = q$, so $P \cap Q \neq \emptyset$.

</div>

<!--
Exercise 1.3.3 (a): relint(A + B) = relint A + relint B

=> no identical points in the relative interior
-->

---

# Separation Theorem

Proof: "$\Rightarrow$"

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.17 (Separation Theorem)">

Let $A, B \subset \mathbb{R}^n$ be nonempty and convex sets in $\mathbb{R}^n$.
Then

$$
\text{relint} A \cap \text{relint} B = \emptyset
$$

iff. $A$ and $B$ can be properly separated.

</Theorem>
</div>
<div class="-mt-20">

<v-switch>

<template #0>

Prerequisite: $\text{cl}(A - B)$ is nonempty, closed \
and convex.
</template>

<template #1>

Prerequisite: $\text{cl}(A - B)$ is nonempty, $\underline{\text{closed}}$ \
and convex.

Obviously, the closure of a set is closed.
</template>
<template #2>

Prerequisite: $\text{cl}(A - B)$ is $\underline{\text{nonempty}}$, closed \
and convex.

Obviously, the closure of a set is closed. \
Furthermore, we know by definition that $A - B = \emptyset$ iff. $A$ or $B$ empty.
</template>
<template #3>

Prerequisite: $\text{cl}(A - B)$ is nonempty, closed \
and $\underline{\text{convex}}$.

Obviously, the closure of a set is closed. \
Furthermore, we know by definition that $A - B = \emptyset$ iff. $A$ or $B$ empty. \
Lastly, the convexity of $A - B$ immediately follows from the convexity of $A$ and $B$ and with Corollary 1.2 we deduce that $\text{cl}(A - B)$ is convex.
</template>

</v-switch>


</div>

<!--
[click]
[click] Nonempty: A - B = {a - b: a in A, b in B} never empty when A and B have elements

[click] Convexity A - B: Remark 1.4, just write it down

Corollary 1.2: A convex => relint, cl convex
-->

---

<div class="flex flex-col items-center h-full gap-2 justify-center">
<div class="flex flex-row justify-around">
<v-click>

$0 \notin \text{cl}(A - B)$
</v-click>

<img src="/curly-bracket.svg" class="-rotate-90 w-4 scale-[3.5] mx-26"/>

<v-click at="3">

$0 \in \text{cl}(A - B)$
</v-click>

</div>
<div class="flex gap-2 ">
<Theorem v-click="2" label="1.14" class="w-full">

Let $A \subset \mathbb{R}^n$ be nonempty, closed and convex. Let $x \in \mathbb{R}^n \backslash A$.
Then, the hyperplane $E$ through $p(A, x)$, orthogonal to $x - p(A, x)$, supports $A$.
Moreover, the halfspace $H$ bounded by $E$ and not containing $x$ is a supporting half space.

</Theorem>

<Theorem v-click="4" label="1.16 (Support Theorem)" class="w-full">

Let $A \subset \mathbb{R}^n$ be closed and convex.
Then through each boundary point of $A$ there exists a supporting hyperplane.

</Theorem>
</div>
<v-click at="5">
<img src="/curly-bracket.svg" class="rotate-90 w-4 scale-[3.5]"/>

$E = \{f = 0\}$ through 0, $A - B \subset \{f \leq 0\}$
</v-click>

</div>

---

# Separation Theorem

Proof: "$\Rightarrow$"

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.17 (Separation Theorem)">

Let $A, B \subset \mathbb{R}^n$ be nonempty and convex sets in $\mathbb{R}^n$.
Then

$$
\text{relint} A \cap \text{relint} B = \emptyset
$$

iff. $A$ and $B$ can be properly separated.

</Theorem>
</div>
<div class="-mt-30">

We have:

- $\text{cl}(A - B)$ nonempty, closed, convex
- $E = \{f = 0\}$, $A - B \subset \{f \leq 0\}$

<v-switch>

<template #1>

$f(a) \leq f(b) \forall a \in A, b \in B$.
</template>
<template #2>

$f(a) \leq f(b) \forall a \in A, b \in B$.
Let $\alpha := \underset{a \in A}{\sup} f(a) \leq f(b) < \infty$ for any $b \in B$, thus $A \subset \{f \leq \alpha\}$. 
</template>
<template #3>

$f(a) \leq f(b) \forall a \in A, b \in B$.
Let $\alpha := \underset{a \in A}{\sup} f(a) \leq f(b) < \infty$ for any $b \in B$, thus $A \subset \{f \leq \alpha\}$. \
We conclude $f(b) \geq \alpha, b \in B \implies B \subset \{f \geq \alpha\}$.
</template>
<template #4>

$f(a) \leq f(b) \forall a \in A, b \in B$.
Let $\alpha := \underset{a \in A}{\sup} f(a) \leq f(b) < \infty$ for any $b \in B$, thus $A \subset \{f \leq \alpha\}$. \
We conclude $f(b) \geq \alpha, b \in B \implies B \subset \{f \geq \alpha\}$. \
Applying this argument in $C := \text{aff} (A \cup B)$ and extending the hyperplane to a hyperplane in $\mathbb{R}^n$ \
(with respect to $C$) by adding $C^\perp$ yields the properly separating hyperplane.
</template>

</v-switch>

</div>

<!--
[click] f(a) \leq f(b), because A - B \subset {f \leq 0}
[click][click]
[click] Make sure NOT A, B \subset {f = \alpha}
-->

---

# Separation Theorem

Proof: "$\Leftarrow$"<v-click at="1">, contraposition </v-click>

<div class="w-58% place-self-end -mt-24 -mr-6">
<Theorem label="1.17 (Separation Theorem)">

Let $A, B \subset \mathbb{R}^n$ be nonempty and convex sets in $\mathbb{R}^n$.
Then

$$
\text{relint} A \cap \text{relint} B = \emptyset
$$

iff. $A$ and $B$ can be properly separated.

</Theorem>
</div>
<div class="-mt-28">

<v-switch>

<template #0>

$A$ and $B$ can<v-click at=2>not</v-click> be properly separated $\implies$ \
$\text{relint} A \cap \text{relint} B = \emptyset$
</template>

<template #1-4>

$A$ and $B$ can**not** be properly separated $\Longleftarrow$ \
$\text{relint} A \cap \text{relint} B \neq \emptyset$
</template>

</v-switch>

</div>

<div v-click="2" class="mt-8">

Suppose $E$ is a separating hyperplane for \
$A$ and $B$, $x_0 \in \text{relint}A \cap \text{relint} B$.

</div>

<v-click at="3">

Then, $x_0 \in E$, thus $A, B \subset E$. \
Hence, $E$ does not properly separate $A$ and $B$.
</v-click>

<div v-click="3" class="self-end m-6 mt-6">

$\square$

</div>


---

# Separation Theorem Results

<Remark label="1.18 (Strong Separation)" class="mb-4">

Let $A, B \subset \mathbb{R}^n$ be convex, $A$ closed, $B$ compact, and assume that $A \cap B = \emptyset$.
Then there is a hyperplane $\{f = \gamma\}$ and an $\varepsilon > 0$ such that $A \subset \{f \geq \gamma + \varepsilon\}$ and $B \subset \{f \leq \gamma - \varepsilon\}$. \
In this case, we say that $A$ and $B$ are _strongly separated_ by the hyperplane $\{f = \gamma\}$.

</Remark>

<v-click>

### Proof

Looking at the proof of Theorem 1.17 again, we now get strict inequalities:

- $f(a) < f(b)\forall a \in A, b \in B$, $\quad \underset{a \in A}{\sup} f(a) < f(b) < \infty \forall b \in B$
- $A \subset \{f < \alpha\}$, $B \subset \{f > \alpha\}$

Thus, we get the $\varepsilon$-neighborhood of $E$.

<div class="self-end -mt-14 m-8">

$\square$

</div>
</v-click>

---

# Strong Separation

<div class="flex justify-center items-center h-full">
	<img src="/convex_no_labels.svg" class="h-100"/>
	<div class="h-100 w-0.5 bg-black rounded-full outline outline-16 outline-lime-400/40 -mx-4" />
	<img src="/convex_no_labels.svg" class="h-100"/>
</div>

---

# Other Remarkable Results

<Remark label="1.19.i" class="mb-4">

Let $A \subset \mathbb{R}^n$ be closed and $\text{int} A \neq \emptyset$.
$A$ is convex iff. every boundary point of $A$ is a support point.

</Remark>

<Remark label="1.19.ii (Motzkin's Theorem)" class="mb-4">

Let $A \subset \mathbb{R}^n$ be closed.
Suppose that for each $x \in \mathbb{R}^n$ there is a unique point $p(A, x) \in A$ such that $\Vert x - p(A, x) \Vert = \min \{\Vert x - y \vert : y \in A \}$.
Then $A$ is convex.

</Remark>

<!-- 
1.19.i war eine Frage iirc

1.19.i Gegenbeispiel: 2 Punkte, beide sind supporting points und A (bestehend aus den Punkten) ist abgeschlossen.
-->

---

# Motzkin's Theorem

<v-switch>
<template #0 >
	<div class="flex justify-evenly items-center h-full" >
		<img src="/convex_no_labels.svg" class="h-100"/>
		<img src="/non-convex_no_labels.svg" class="h-100" />
	</div>
</template>

<template #1>

<div class="flex justify-evenly items-center h-full" >
<img src="/convex_point.svg" class="h-100"/>
<img src="/non-convex_point.svg" class="h-100" />
</div>
</template>

<template #2>

<div class="flex justify-evenly items-center h-full" >
<img src="/convex_labels.svg" class="h-100"/>
<img src="/non-convex_point.svg" class="h-100" />
</div>
</template>

<template #3>

<div class="flex justify-evenly items-center h-full" >
<img src="/convex_labels.svg" class="h-100"/>
<img src="/non-convex_labels.svg" class="h-100" />
</div>
</template>
</v-switch>
