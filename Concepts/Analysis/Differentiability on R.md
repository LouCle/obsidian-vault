**References.** #analysis 

> [!INFO] Definition
> A function $f: I \subseteq \mathbb R \to \mathbb R^m$ is *differentiable in the point* $a\in I$ with $f'(a) = c\in \mathbb R$ iff $$\frac{f(a+\Delta x)-f(a)}{\Delta x} \to c~~~~~~~\Delta x\to 0$$
> or alternatively $$\Delta f=c\Delta x+\epsilon(\Delta x)\Delta x$$
> with an epsilon-function $\epsilon$.
> 
> The function $f$ is likewise said to be *differentiable in $I$* if it is differentiable in every point of $I$.
> 
> 

> [!INFO] Definition
> A function $f:I\to \mathbb R$ that is $k$-times differentiable on an interval $I$ with $f^{(k)}$ continuous, is said to belong to the class of $C^k(I)$ functions.
> 
> If $f$ is differentiable for any $k \in \mathbb N$, then it is called *smooth* and said to belong in $C^\infty(I)$.
### Theory

**Theorem.** Let $f:I \subseteq \mathbb R^n \to \mathbb R^m$ be a function. Then $f$ is differentiable if and only if the coordinate functions are differentiable.

**Theorem.** If $f: I \subseteq \mathbb R \to \mathbb R^m$ is differentiable in the point $a \in I$ then $f$ is continuous in $a$.

**Theorem.** Let $f:I\subseteq \mathbb R \to \mathbb R^m$, $g:I \subseteq \mathbb R \to \mathbb R^m$ and $\alpha:I\to \mathbb R$ be differentiable in $a\in I$. Then the following constructions are differentiable in $a$: $$f\pm g,~~~f\cdot g,~~~\alpha f$$
**Theorem (Univariate chain rule).** Let $I$ and $J$ be real intervals. Fix $f:I\to J$ and $g:J \to \mathbb R^m$. Let $f$ be differentiable in $t_0\in I$ and $g$ in $f(t_0)\in J$. Then $g\circ f$ is differentiable in $t_0$ given with $$(g\circ f)'(t_0)=g'(f(t_0))f'(t_0)$$
**Theorem (Differentiation of inverse function).** Let $f:I \subseteq \mathbb R\to \mathbb R$ be a continuous and strictly increasing function. If $f$ is differentiable in the point $x_0\in I$ with $f'(x_0)\neq 0$, then the inverse function $f^{-1}$ is differentiable in $y_0=f(x_0)$ with $$(f^{-1})'(y_0)=\frac{1}{f'(x_0)}$$
Alternatively, we can write the above as $$(f^{-1})'(y)=\frac{1}{f'(f^{-1}(y))}$$
Hence we can think of the derivative of $f^{-1}$ has the composition $g\circ f' \circ f^{-1}$ with $g$ as the reciprocal function. So if $f'$ is differentiable, then $(f^{-1})'$ is a composition of three differentiable functions, is therefore itself differentiable by the chain rule. ^525591

**Lemma (Derivative at Maximum is Zero).** Let $f: I \to \mathbb R$ be defined on an interval $I$. Assume that $a$ is an [[Topology on R|interior point]] in $I$ and that $$f(x)\leq f(a)~~~~\forall x \in I$$If $f$ is differentiable in $a$, then $f'(a) = 0$.

*Proof.* See [[Derivative at Maximum is Zero]].

Since the maximum of $-f$ is the minimum of $f$, we know that the above lemma goes for the minimum as well.

**Theorem (Rolle's Theorem).** Let $f : [a,b] \to \mathbb R$ be a map continuous on $[a,b]$ and differentiable on $(a,b)$, then if $f(a)=f(b)=0$, then there exists a $\xi \in (a,b)$ with $f'(\xi)=0$.

*Proof.* See [[Rolle's Theorem]].

**Theorem (Mean value).** Let $f:[a,b] \to \mathbb R$ be a map continuous on the closed interval $[a,b]$ and differentiable in $(a,b)$. Then there exists a point $\xi \in (a,b)$ with the property that
$$f'(\xi) = \frac{f(b)-f(a)}{b-a}$$

*Proof.* See [[Mean Value Theorem]].

**Corollary.** Let $f: I \to \mathbb R$ be differentiable on an interval $I$. Fix $a,b\in I$ with $a \neq b$. Then there exists a point $\xi$ inbetween $a$ and $b$ such that 
$$f(b)-f(a) = f'(\xi)(b-a)$$

*Proof.* See [[Mean Value Theorem#^fd3a01|corollary 1 to the MVT]].

It is easily checked that the derivative of a constant function is everywhere zero. Here we have however a result that implies only the constant function has such a derivative.

**Theorem.** Let $f:I \to \mathbb R$ be differentiable on $I \subseteq \mathbb R$ with $f'(I) = \qty{0}$, then $f$ is the constant function. 

*Proof.* See [[Mean Value Theorem#^d5dd6c|corollary 2 to the MVT.]]

**Theorem.** Let $f:I\to \mathbb R$ be differentiable on $I \subseteq \mathbb R$ with $f'(x)\geq 0$, then $f$ is increasing. If $f'(x) > 0$ then $f$ is strictly increasing.

*Proof.* See [[Mean Value Theorem#^b1cabe|corollary 3 to the MVT]].

**Theorem (Extended Rolle's Theorem 1).** Let $g :  I \subseteq \mathbb R \to \mathbb R$ be $n$-times differentiable on $I$ and fix points $a,b$ with $a\neq b$. Then if 
$$g(a)=g'(a)=\cdots = g^{(n)}(a) = g(b)= 0$$
there exists a $\xi$ inbetween $a$ and $b$ such that $g^{(n)}(\xi) = 0$.

*Proof.* See [[Rolle's Theorem#^c059b5|Extended Rolle's Theorem]].

#### Taylor polynomials

**Definition.** Let $f$ be an $n$-times differentiable function $f: I \to \mathbb R$ and fix $a \in I$. Then we define the *Taylor series of $f$ at $a$* as the function 
$$P_n(x) = \sum^n_{k=0} \frac{f^{(k)}(a)}{k!}(x-a)^k$$
See [[Taylor series in R]].

**Theorem (Taylor's Remainder Theorem).** 

*Proof*. See [[Taylor series in R#^f82980|Taylor's Remainder Theorem]].

### Examples