eferences.** #analysis

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

**Theorem.** The limit exists if and only if both the right and left limit exists.

**Theorem (Uniqueness of limits).** Fix $f:A \subseteq \mathbb R^n \to \mathbb R^m$ and $a\in A'$. If the limit for $x\to a$ exists, then it is unique.

*Proof.* See [[Limit is Unique]].

**Theorem (Addition of limits).** Let $f: A \to \mathbb R^m$ and $g:A \to \mathbb R^m$ be defined on $A \subseteq \mathbb R^n$. Let $a \in A'$. Then $$f(x)+g(x) \to b+c$$
for $x\to a$ if $f(x) \to b$ and $g(x)\to c$ for $x\to a$.

**Theorem (Product of limits).** Same as above but with products.

**Theorem.** Set $f:A\subseteq \mathbb R^n \to \mathbb R^m$ and fix $a\in A'$. If $f(x)\to b$ for $x\to a$, then $d(f(x),0) \to d(b,0)$ for $x\to a$.

**Theorem.** Same set up as above. If $f(x)\to b$ for $x\to a$, then $1/f(x) \to 1/b$ for $x\to a$.

**Theorem (Limit of composition).** Define $f:A\subseteq \mathbb R^n \to \mathbb R^m$ and $g:B\subseteq \mathbb R^l \to \mathbb R^m$. Let $a \in A'$ and $b\in B'$. Suppose that $$f(x)\to b,~~~~g(y)\to c$$
for $x\to a$ and $y\to b$. Then $g\circ f(x) \to c$ for $x\to a$.

**Theorem.** Define $f:(f_1,\dots,f_m) : A\subseteq \mathbb R^n \to \mathbb R^m$. Let $a\in A'$ and $b\in \mathbb R^m$. For $x\to a$ we have 
$$f(x)\to b \iff f_1(x) \to b_1,\dots,f_m(x)\to b_m$$
 
**Theorem.** [[Image in Closed Set S implies Limit in S]].

**Proposition.** Let $f:(b, \infty] \to \mathbb R$ be a bounded and weakly increasing function. Then
$$\lim_{x\to \infty} f(x) = \sup_{x\in[b,\infty)} f(x) = L $$
*Proof.* Since $f$ is weakly inreasing, we know that $$f(k) \leq f(x) \leq L$$for $k\leq x$. By [[Supremum is a Closure Point]] we know that for any $\epsilon>0$ there exists a $k$ such that $f(k) \in B_\epsilon(L)$, and with the above, all $x \geq k$ will have $f(x) \in B_\epsilon(L)$. Hence the infinite limit is $L$.

**Definition.** A function ${} \epsilon : A \subseteq \mathbb R^n \to \mathbb R^m {}$ is an *epsilon-function* for $x\to a$ if 
$$\epsilon(x)\to 0~~~x\to a$$
**Definition.** Set $f:\subseteq \mathbb R^n \to \mathbb R^m$ and $g : A \to \mathbb R^k$. Denoted using *o-notation*, we write  "$f=o(g)$" (or more appropriately, $f\in o(g)$) for $x\to a$ if there exists an epsilon-function $\epsilon:A\to \mathbb R^m$ with 
$$f(x) = \epsilon(x)d(g(x),0)$$
for $x\in A$. We say that *$f$ is little-o of $g$*.
 
