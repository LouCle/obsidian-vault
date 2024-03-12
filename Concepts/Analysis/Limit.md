**References.** #analysis

> [!INFO] Definition
> A point $L$ is the *limit* of a map $f:A\subset \mathbb R^n \to \mathbb R^m$ at a [[Topology on R|limit point]] $x_0$, written either
> $$\lim_{x\to x_0} f(x) = L ~~~~\mathrm{or}~~~~ f(x)\to L~~~~~~x\to x_0 $$
> if it holds that 
> $$\forall \epsilon > 0~\exists \delta > 0: ~~~ d(f(x),L) < \epsilon~~~\forall x \in A ~~\mathrm{with}~~d(x,x_0) < \delta.$$

### Theory

**Definition.** A *right limit* $R$ of $f(x)$ as $x$ goes to $a^+$ is defined as
$$\forall \epsilon > 0~\exists \delta > 0: ~~~ d(f(x),R) < \epsilon~~~\forall x \in A ~~\mathrm{with}~~0 < x - a < \delta.$$
**Definition.** Likewise a *left limit* $L$ of $f(x)$ as $x$ goes to $a^-$ is defined as
$$\forall \epsilon > 0~\exists \delta > 0: ~~~ d(f(x),L) < \epsilon~~~\forall x \in A ~~\mathrm{with}~~0< a-x < \delta.$$


**Corollary.** Let $A \subseteq \mathbb R^n$ and let ${} a\in \bar A - A$ be a limit point of $A$.
