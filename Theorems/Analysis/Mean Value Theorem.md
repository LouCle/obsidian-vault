**References.** #analysis 

> [!INFO] Theorem
> Let $f:[a,b] \to \mathbb R$ be a map continuous on the closed interval $[a,b]$ and differentiable in $(a,b)$. Then there exists a point $\xi \in (a,b)$ with the property that
> $$f'(\xi) = \frac{f(b)-f(a)}{b-a}$$
> 
> 
### Proof

The idea of the proof is to exploit [[Rolle's Theorem]] to guarantee the existence of the mean value.

We will define an auxiliary map $g:[a,b] \to \mathbb R$ from $f$ in such a way that $g(a)=g(b)=0$.
$$g(x) = f(x) - f(a) - \frac{f(b) - f(a)}{b-a}(x-a)$$
Notice that $g(a)=g(b)=0$. Hence by Rolle's theorem there exists $\xi \in (a,b)$ with $g'(\xi) = 0$.

If we differentiate $g$ we get
$$g'(x) = f'(x) - \frac{f(b)-f(a)}{b-a}$$
And thus $$\begin{align}f'(\xi) &= g'(\xi) + \frac{f(b)-f(a)}{b-a}\\&=\frac{f(b)-f(a)}{b-a}\end{align}$$ Concluding the proof.

### Corollaries

**Corollary.**  Let $f: I \to \mathbb R$ be differentiable on an interval $I$. Fix $a,b\in I$ with $a \neq b$. Then there exists a point $\xi$ inbetween $a$ and $b$ such that  
$$f(b)-f(a) = f'(\xi)(b-a)$$
*Proof.* In the case that $a < b$, then we will consider the restriction of $f$ to $[a,b] \subseteq I$. In that case exists such an $\xi \in (a,b)$ due to the MVT.

In the case that $b < a$, we restrict $f$ to $[b,a] \subseteq I$. This exchanges the terms in the mean value fraction, but preserves the sign, hence we can still obtain the equation above. ^fd3a01

**Corollary.** Let $f:I \to \mathbb R$ be differentiable on $I \subseteq \mathbb R$ with $f'(I) = \qty{0}$, then $f$ is the constant function. 

*Proof.* By the corollary above, regardless of which $a,b$ we pick, then 
$$f(b)-f(a) = f'(x)(b-a) = 0$$
for all $x\in I$. This of course means that $f(a)=f(b)=f(x)=c$ for all $x$. ^d5dd6c

**Theorem.** Let $f:I\to \mathbb R$ be differentiable on $I \subseteq \mathbb R$ with $f'(x)\geq 0$, then $f$ is increasing. If $f'(x) > 0$ then $f$ is strictly increasing.

*Proof.* If $a<b$ are two points in $I$, then the MVT has
$$f(b)-f(a) = f'(x)(b-a) = 0$$
Since $f'(x)\geq 0$, we have that $f(b) \geq f(a)$. If we had $f'(x) > 0$ then this entails $f(b) > f(a)$ by same argument. ^b1cabe
### Examples