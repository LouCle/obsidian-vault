**References.** #analysis 

> [!INFO] Definition
> Let $f$ be an $n$-times differentiable function $f: I \to \mathbb R$ and fix $a \in I$. Then we define the *Taylor series of $f$ at $a$* as the function 
$$P_n(x) = \sum^n_{k=0} \frac{f^{(k)}(a)}{k!}(x-a)^k.$$
> We call $a$ the *expansion point*. 

### Theory

The particular way in which $P_n$ approximates the function, is that the $k$-th derivative of $P_n$ at $a$ is equal to the $k$-th derivative of the original function at $a$.

**Theorem (Taylor's Remainder Theorem).** Let $f: I\subseteq \mathbb R \to \mathbb R$ be an $n$-differentiable on $I$ and fix points $a,b\in I$ with $a \neq b$. Then there exists a point $\xi$ inbetween $a$ and $b$ such that  ^f82980
$$f(b) = P_{n-1}(b) + \frac{f^{(n)}(\xi)}{n!}(b-a)^n$$
where $P_{n-1}(b)$ is the $n-1$ taylor expansion around $a$.

### Examples