**References.** #analysis 

> [!INFO] Definition
> A function $f: I \subseteq \mathbb R \to \mathbb R^m$ is *differentiable in the point* $a\in I$ with $f'(a) = c\in \mathbb R$ iff $$\frac{f(a+\Delta x)-f(a)}{\Delta x} \to c~~~~~~~\Delta x\to 0$$
> or alternatively $$\Delta f=c\Delta x+\epsilon(\Delta x)\Delta x$$
> with an epsilon-function $\epsilon$.
> 
> 
### Theory

**Theorem.** Let $f:I \subseteq \mathbb R^n \to \mathbb R^m$ be a function. Then $f$ is differentiable if and only if the coordinate functions are differentiable.

**Theorem.** If $f: I \subseteq \mathbb R \to \mathbb R^m$ is differentiable in the point $a \in I$ then $f$ is continuous in $a$.

**Theorem.** Let $f:I\subseteq \mathbb R \to \mathbb R^m$, $g:I \subseteq \mathbb R \to \mathbb R^m$ and $\alpha:I\to \mathbb R$ be differentiable in $a\in I$. Then the following constructions are differentiable in $a$: $$f\pm g,~~~f\cdot g,~~~\alpha f$$
**Theorem (Univariate chain rule).** Let $I$ and $J$ be real intervals. Fix $f:I\to J$ and $g:J \to \mathbb R^m$. Let $f$ be differentiable in $t_0\in I$ and $g$ in $f(t_0)\in J$. Then $g\circ f$ is differentiable in $t_0$ given with $$(g\circ f)'(t_0)=g'(f(t_0))f'(t_0)$$
**Theorem (Differentiation of inverse function).** Let $f:I \subseteq \mathbb R\to \mathbb R$ be a continuous and strictly increasing function. If $f$ is differentiable in the point $x_0\in I$ with $f'(x_0)\neq 0$, then the inverse function $f^{-1}$ is differentiable in $y_0=f(x_0)$ with $$(f^{-1})'(y_0)=\frac{1}{f'(x_0)}$$
Alternatively, we can write the above as $$(f^{-1})'(y)=\frac{1}{f'(f^{-1}(y))}$$
Hence we can think of the derivative of $f^{-1}$ has the composition $g\circ f' \circ f^{-1}$ with $g$ as the reciprocal function. So if $f'$ is differentiable, then $(f^{-1})'$ is a composition of three differentiable functions, is therefore itself differentiable by the chain rule.

**Lemma.** Let $f: I \to \mathbb R$ be defined on an interval $I$. Assume that $a$ is an [[Topology on R|interior point]] in $I$ and that $$f(x)\leq f(a)~~~~\forall x \in I$$If $f$ is differentiable in $a$, then $f'(a) = 0$.

*Proof.* See [[Derivative at Maximum is Zero]].

**Theorem (Mean value).** 

### Examples