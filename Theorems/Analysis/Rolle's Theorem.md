**References.** #analysis 

> [!INFO] Theorem
> Let $f : [a,b] \to \mathbb R$ be a map continuous on $[a,b]$ and differentiable on $(a,b)$, then if $f(a)=f(b)=0$, then there exists a $\xi \in (a,b)$ with $f'(\xi)=0$.
> 
> 

### Proof

According to [[Extreme Value Theorem]] there exists a maximum $G$ and minimum $g$ in $[a,b]$ for $f$.

**Case 1.** If $G = g$ then $f'(x) = 0$ on all ${} x=\xi \in (a,b) {}$, since $f$ would be constant.

**Case 2.** If $g < G$ then either cannot be $0$. One of the extrema may be equal to $f(a)=f(b)=0$, but not both, hence one of them will be in $(a,b)$. Thus by [[Derivative at Maximum is Zero]] we know that there exists at least one $\xi \in(a,b)$ such that $f'(\xi) = 0$.

### Corollaries

**Theorem (Extended Rolle's Theorem 1).** Let $g :  I \subseteq \mathbb R \to \mathbb R$ be $n$-times differentiable on $I$ and fix points $a,b$ with $a\neq b$. Then if 
$$g(a)=g'(a)=\cdots = g^{(n-1)}(a) = g(b)= 0$$
there exists a $\xi$ inbetween $a$ and $b$ such that $g^{(n)}(\xi) = 0$.

*Proof.* Iteratively apply Rolle's Theorem with $\xi_i$'s, and pick $\xi=\xi_n$. ^c059b5

### Examples