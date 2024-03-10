**References.** #analysis #topology 
- [[Space]]

> [!INFO] Definition
> A *metric space* $(X, d)$ is a set $X$ together with a function called the *metric* ${} d : X\times X \to \mathbb R {}$ which satisfies the following conditions:
> 1. $d(x,x) = 0$ for all $x\in X$.
> 2. Positivity. If $x\neq y$ then $d(x,y)> 0$ for all $x,y \in X$.
> 3. Symmetry. $d(x,y) = d(y,x)$ for all $x,y \in X$.
> 4. Triangle inequality. $d(x,z) \leq d(x,y) + d(y,z)$.
>    
>    Alternatively (1) and (2) may be viewed as $d(x,y) = 0 \iff x = y$ since (1), (3-4) prove positivity.

### Theory

**Definition.** An *open ball* $B_\epsilon(a)$ is the set $$B_\epsilon(a) = \qty{x\in X : d(x,a) < \epsilon}$$A *closed ball* is the set
$$B_\epsilon[a] = \qty{x\in X : d(x,a) \leq \epsilon}$$

**Definition.** A point $a$ is called a *limit point* to a set ${} S\subseteq X$ if for all $\epsilon > 0$ there exists an $s\in S$ in the ball $B_\epsilon(a)$. 

**Definition.** A point $x\in S\subseteq X$ is an *isolated point* of $S$ if and only if it is not a limit point.

Equivalently $x$ is isolated if $\qty{x}$ is an open set in the topological space $X$.

### Examples

**Remark.** A space with the reversed triangle inequality has at most one point.

*Proof.* Let $d$ be such a function. It is straight-forward to check that the conditions hold for a set with $1$ point.

Now for the sake of contradiction, let $X$ be a set with more than $1$ element. Then there are distinct elements $x,y$ such that 
$$\begin{align}d(x,x) = 0&\geq d(x,y) + d(y,x)\end{align}$$
Since $x,y$ are distinct, the RHS must be greater than $0$, which is a contradiction.

**Example.** The real numbers together with the function $d(x,y) = |x-y|$ is a metric space.

