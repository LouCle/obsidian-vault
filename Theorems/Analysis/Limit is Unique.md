**References.** #analysis 

> [!INFO] Theorem
> Fix $f:A \subseteq \mathbb R^n \to \mathbb R^m$ and $a\in A'$. If the limit for $x\to a$ exists, then it is unique.
> 
> 
### Proof

Assume that $f(x) \to b',b''$ for $x \to a$. We will attempt to show that $b'=b''$ by showing that ${} d(b',b'') = 0$, equivalent to saying that $d(b',b'') < \epsilon$ for every $\epsilon > 0$.

Set $\epsilon > 0$. Then there exists $\delta',\delta'' > 0$ so that 
$$\begin{align}d(f(x),b') < \frac{\epsilon}{2} ~~~\forall x,~d(x,a)<\delta'~\\ d(f(x),b'')<\frac{\epsilon}{2} ~~~\forall x,~d(x,a)<\delta''\\\end{align}$$
Pick $\delta = \min\qty{\delta',\delta''}$, then by the triangle inequality, 
$$\begin{align}d(b',b'') &\leq d(f(x),b') ~+ ~d(f(x),b'')\\&<\epsilon~~~~~~~~~~~\qty[~\forall x,~d(x,a)< \delta~]\end{align}$$
From the above we have that $d(b',b'') < \epsilon$. 

Assume that $d(b',b'') = \epsilon > 0$. But this contradicts that $d(b',b'')<\epsilon$ for all epsilon. Hence by the [[Metric space|metric axioms]], $d(b',b'') = 0$, which means $b' = b''$.

### Examples