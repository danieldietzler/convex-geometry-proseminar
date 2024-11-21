<div class="flex h-full justify-evenly items-center">

$A \subset \mathbb{R}^2$

  <div class="h-full w-0.5 bg-black/30 rounded-full" />

$B \subset \mathbb{R}^2$

</div>

---

# Fundamentals

<Definition label="1.9">

For two sets $A, B \subset \mathbb{R}^n$ and a hyperplane $E = \{f = \alpha\}$, we say that $E$ _separates_ $A$ and $B$ if **either** \
$A \subset \{f \leq \alpha\}$, $B \subset \{f \geq \alpha\}$ **or** $A \subset \{f \geq \alpha\}$, $B \subset \{f \leq \alpha\}$. \
We say that convex sets $A$ and $B$ can be _properly separated_
if there exists a separating hyperplane which does not contain both $A$ and $B$.

</Definition>

<div class="mt-8">

- Reminder: $A$ convex. $\text{relint} A = \{x \in \mathbb{R}^n : \forall y \in \text{aff}(A) \backslash \{x\} \; \exists z \in A \text{ with } x \in (z, y)\}$
</div>

---

# Proper Separation

<!-- 
\draw[black, thick] (1, 1) -- (2, 2) node[midway, below right]{A};
\draw[black, thick] (3, 3) -- (4, 4) node[midway, above left]{B};
\draw[gray, thin] (0, 0) -- (5, 5) node[below right=.1cm,color=gray]{E};
\filldraw[black] (1, 1) circle (2pt);
\filldraw[black] (2, 2) circle (2pt);
\filldraw[black] (3, 3) circle (2pt);
\filldraw[black] (4, 4) circle (2pt);
 -->
<img src="/non-properly-separated.svg" class="h-80"/>