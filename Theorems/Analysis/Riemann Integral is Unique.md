eferences.** #analysis 

> [!INFO] Theorem
> If $f:[a,b] \to \mathbb R$ is Riemann-integrable, then $\displaystyle \int_a^b f(x)~dx$ is uniquely determined.
> 
> 

### Proof

Let $I_1,I_2 \in \mathbb R$ be quantities satisfying the first defintion of the [[Integration on R|Riemann integral]]. We will show that $I_1=I_2$ by showing that $|I_1-I_2| < \epsilon$ for an arbitrary $\epsilon>0$.

Set $\epsilon > 0$. By the definition, we know that there exists $\delta_1,\delta_2$ such that the sums
$$M(P) = \sum_{i=1}^{n} f(t_i)\Delta x_i$$
give us the equations
$$\begin{align}|I_1-M(P)|< \epsilon/2~~~~\forall P:\mathrm{mesh}(P)<\delta_1\\|I_1-M(P)|< \epsilon/2~~~~\forall P:\mathrm{mesh}(P)<\delta_2\end{align}$$
There exists a tagged partition $P$ with mesh $\min\qty{\delta_1,\delta_2}$, or construct one (the equidistant partition), then clearly 
$$|I_1-I_2| \leq |I_1 - M(P)| + |I_2 - M(P)| < \epsilon~~~ \forall P:\mathrm{mesh}(P)\leq \delta_1,\delta_2$$
So $I_1=I_2$.


### Examples
