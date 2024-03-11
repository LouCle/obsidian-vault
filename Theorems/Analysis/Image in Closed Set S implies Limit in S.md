**References.** #analysis 

> [!INFO] Theorem
> Fix a map $f : A \subseteq \mathbb R^n \to \mathbb R^m$ and a limit point ${} a \in A' {}$. Let $C\subseteq \mathbb R^m$ be a [[Topology on R|closed set]]. 
> 
> If $f(A) \subseteq C$ and if  $\displaystyle \lim_{x\to a} f(x) = b$ then $b\in C$.
> 
> 

### Proof

We will aim to show that $b$ is a limit point for $C$ i.e. the intersection of $C$ with any open ball $B_\epsilon(b)$ is non-empty.

Set $\epsilon> 0$. The limit implies we can find $\delta > 0$ such that
$$d(f(x),b) < \epsilon ~~~ d(x,a) < \delta,~x \in A$$
Since $a$ is a limit point, we can find an $x_0$ such that $d(x_0,a) < \delta$. 

From this we know that $f(x_0) \in B_{\epsilon}(b) \cap C$ because $x_0$ is an $x$ satisfying the $\delta$-condition.

This means that $b$ is a closure point to $C$, and since $C$ is a closed set it must equal its closure, hence $b\in C$.

This must necessarily be true as well for left- and right limits.

### Examples

**Example.** Let $f(x) \geq 0$ and let $\lim_{x\to a} f(x) = b$, then $b\geq 0$ by the above theorem.