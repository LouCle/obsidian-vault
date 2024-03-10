**References.** #analysis #exercise

> [!INFO] Theorem
> Let $f : \mathbb R \to \mathbb R$ be a function with ${} \displaystyle \lim_{x\to \infty} f(x) = a {}$ and ${} \displaystyle \lim_{x\to -\infty} f(x)=b {}$. Then $f$ is uniformly continuous on $\mathbb R$.
> 
> 

### Proof

The positive limit implies that for any $\epsilon>0$ there exists a $K^+>0$ such that
$$|g(x)-b|,~|g(y)-b| < \frac{\epsilon}{2}$$
for $x,y\geq K^+$. Hence the [[Metric space|triangle inequality]] implies that
$$|g(x)-g(y)| \leq |g(x) - b| + |g(y) - b| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$
Pick also by the negative limit, a $K^{-}<0$ such that 
$$|g(x)-g(y) < \epsilon$$
for $x,y\leq K^-$. 

Uniform continuity of $f$ is if there exist a $\delta$ such that
$$|g(x) - g(y)| < \varepsilon~~~ \mathrm{for}~x,y \in \mathbb R,~ |x-y| < \delta.$$
We know that $K^- < 0 < K^+$ and we can thus check the following cases:

**Case 1.** If $x,y \leq K^-$ or $x,y\geq K^+$ then any $\delta$ will do.

**Case 2.** If $x,y\in [K^-, K^+]$ then by [[Uniform Continuity on Intervals]] there exists a $\delta_1$. By case  1, we can set $\delta = \delta_1$.

**Case 3.** If $x\leq K^- < y < K^-$ then by the triangle inequality we have 
$$\begin{align}|g(x) - g(y)| &\leq |g(x) - g(K^-)| + |g(y) - g(K^-)|\\&=2\epsilon\end{align}$$




### Examples