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
Proof: "$\Leftarrow$"

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

Suppose $\text{relint} A \cap \text{relint} B = \emptyset$. \
Then, $\text{relint} A - \text{relint} B \not \owns 0$ follows. (*) \
$\overset{\text{Ex 1.3.3 (a)}}{\implies} 0 \notin \text{relint}(A - B)$

</div>

<div v-click class="mt-16">

(*) Let $P := \text{relint} A, Q := \text{relint} B$. $P - Q = \{p - q : p \in P, \; q \in Q\}$. \
Thus, clearly $0 \in P - Q \iff \exists p \in P, q \in Q: p = q$, so $P \cap Q \neq \emptyset$.
</div>

<!-- 
Exercise 1.3.3 (a): relint(A + B) = relint A + relint B
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

Prerequisite: $\text{cl}(A - B)$ is nonempty, closed \
and convex. \
Obviously, the closure of a set is closed. \
Furthermore, we know by definition that $A - B = \emptyset$ iff. $A$ or $B$ empty. \
Lastly, the convexity of $A - B$ immediately follows from the convexity of $A$ and $B$ and with Corollary 1.2 we deduce that $\text{cl}(A - B)$ is convex.

</div>


<!-- 
Nonempty: A - B = {a - b: a in A, b in B} never empty when A and B have elements

Convexity A - B: Remark 1.4, just write it down

Corollary 1.2: A convex => relint, cl convex
-->

---

<div class="flex flex-col items-center h-full gap-2 justify-center">
<div class="flex flex-row justify-around">

$0 \notin \text{cl}(A - B)$

<img src="/curly-bracket.svg" class="-rotate-90 w-4 scale-[3.5] mx-26"/>

$0 \in \text{cl}(A - B)$
</div>
<div class="flex gap-2 ">
<Theorem label="1.14" class="w-full">

Let $A \subset \mathbb{R}^n$ be nonempty, closed and convex. Let $x \in \mathbb{R}^n \backslash A$.
Then, the hyperplane $E$ through $p(A, x)$, orthogonal to $x - p(A, x)$, supports $A$.
Moreover, the halfspace $H$ bounded by $E$ and not containing $x$ is a supporting half space.

</Theorem>

<Theorem label="1.16 (Support Theorem)" class="w-full">

Let $A \subset \mathbb{R}^n$ be closed and convex. 
Then through each boundary point of $A$ there is exists a supporting hyperplane.

</Theorem>
</div>
<img src="/curly-bracket.svg" class="rotate-90 w-4 scale-[3.5]"/>

$E = \{f = 0\}$ through 0, $A - B \subset \{f \leq 0\}$
</div>