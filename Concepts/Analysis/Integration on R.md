**References.** #analysis 

> [!INFO] Definition of Riemann integral 1
> A function $f : [a,b] \to \mathbb R$ is said to be *Riemann-integrable* if there exists a number $I\in \mathbb R$ written $$I= \int_a^b f(x)~dx$$called the *Riemann integral* with the following property: for any $\epsilon > 0$, there exists a $\delta > 0$ such that any [[Tagged Partition|tagged partition]] $P(x,t)$ on $[a,b]$ with $\mathrm{mesh}(P)<\delta$  has that $$\left|I-\sum_{i=1}^n f(t_i)\Delta x_i\right| < \epsilon.$$
> 
> 

> [!INFO] Definition of the antiderivative
> Set $f:I\to \mathbb R$ on an interval $I$. A function $F : I\to \mathbb R$ is called the *antiderivative* for $f$ on $I$ if $F$ is differentiable in all $x\in I$ with $F'(x)=f(x)$. We write $$F(x) = \int f(x)~dx.$$

### Theory

**Lemma.** If $f : [a,b] \to \mathbb R$ is Riemann-integrable, then the integral $\displaystyle \int_a^b f(x) ~dx$ is is uniquely determined.

*Proof.* [[Riemann Integral is Unique]].

**Theorem (2nd Fundamental Theorem of Calculus).** Let $f:[a,b] \to \mathbb R$ be continuous. If $f$ has the antiderivative $F$ on $[a,b]$ then
1. $f$ is Riemann-integrable, and most importantly
2. $$\int_a^b f(x)~dx = F(b) - F(a).$$
*Proof.* [[Fundamental Theorems of Calculus]].

**Theorem (Integration by parts).** Let $f : I \to \mathbb R$ be continuous with an antiderivative $F : I \to \mathbb R$ and let $G : I \to \mathbb R$ be differentiable with continuous derivative $G'=g : I \to \mathbb R$, then $$\int f(x)G(x)~dx = F(x)G(x) - \int F(x)g(x)~dx.$$*Proof.* The proof is simple. RHS is differentiable with the derivative $$f(x)G(x)+F(x)g(x) - F(x)g(x) = f(x)G(x).$$For techniques related to integration by parts, check out its [[Theory of real analysis#^99a58d|techniques]] section, as well as the examples at the bottom.

**Theorem (Integration by substitution).** Hvis $g : J \to \mathbb R$ is continuous on an interval $J\subseteq \mathbb R$ and $f : I \to \mathbb R$ is differentiable in an interval $I \subseteq \mathbb R$ with continuous derivative $f' : I \to \mathbb R$ and $f(I) \subseteq J$, then it holds that $$\int g(f(t))f'(t)~dt = \qty[\int g(x)~dx]_{x=f(t)}=G\circ f.$$with $G$ the antiderivative of $g$ of course.

*Proof.* The proof is also very simple. By [[Differentiability on R#^525591|the chain rule]] we have that $$(G\circ f)'(t) = g(f(t))f'(t).$$There are some selected examples at the bottom as well.

### Examples

##### Examples of integration by parts