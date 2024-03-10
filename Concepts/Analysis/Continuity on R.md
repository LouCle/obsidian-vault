**References.** #analysis

> [!INFO] Definition
> A function $f:A \subset \mathbb R^n \to \mathbb R^m$ is said to be continuous in a point $a\in A$ if 
> $$\forall \epsilon > 0~ \exists \delta >0~~~~d(f(a),f(x)) < \varepsilon~~~\text{for } x \text{ with } d(x,a) <\delta. $$
> The map is said to be continuous in the whole domain $A$ if it is continuous in every point.
> 
> 

### Theory

**Definition.** If $a$ is [[Metric space|non-isolated point]] in $A$ then we can equivalently formulate the usual definition as the [[Limit|limit]]
$$\Delta f \to 0 ~~~ \text{ for } \Delta x \to 0,~a+\Delta x\in A.$$
With $\Delta x = x-a$ and $\Delta f = f(x) - f(a) = f(a +\Delta x) - f(a)$.

**Theorem.** Define $A \subset \mathbb R^n$, $B\subset \mathbb R^m$, and the maps $f:A\to B$ and $g:B \to \mathbb R^k$. If $f$ is continuous in a point $a\in A$ and $g$ is continuous in a point $b=f(a)$, then $g\circ f$ is continuous in $a$.

**Theorem.** A map $f=(f_1,\dots,f_m) : A\subset \mathbb R^n \to \mathbb R^m$ is continuous in the point $a \in A$ if each coordinate map $f_i$ is continuous in $A$.

**Theorem.** [[Extreme Value Theorem]].

**Theorem.** [[Intermediate Value Theorem]].

**Corollary.** Image of interval on continuous function is interval.

**Theorem.** A continuous and strictly increasing function $f: I \subset \mathbb R \to \mathbb R$ has a continuous and strictly increasing preimage $f^{-1} : J = f(I) \to I$.

**Definition.** [[Uniform Continuity on R]].

**Theorem.** [[Uniform Continuity on Intervals]].

**Theorem.** Let $f: (a,b) \to \mathbb R$ be a real function on an open, bounded interval. Then there exists a continuous function $g:[a,b] \to \mathbb R$ with $g(x)=f(x)$ for all $x\in (a,b)$ if and only if $f$ is uniformly continuous.

**Theorem.** [[Nested Interval Theorem]].

See [[Theory of real analysis]] for more relevant theorems.
### Examples