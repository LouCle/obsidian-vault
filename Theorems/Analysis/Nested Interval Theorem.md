**References.** #analysis

> [!INFO] Theorem
> Let $(I_n)_{n=1}^\infty$ be a sequence of closed intervals, such that $I_n \supset I_{n+1}$ for any $n$. Then if $$\forall \varepsilon > 0 ~\exists N > 0 ~\forall n \geq N~~~ |I_n| < \varepsilon$$ 
 There exists a unique point $\xi \in \mathbb R$ such that $\xi \in I_n$ for any $n$.
> 
> 
> 

### Proof

**Uniqueness.** Fix $\xi_1,\xi_2$ such that they are in $I_n=[a_n,b_n]$ for any $n$. We'll try to show that $\xi_1=\xi_2$ by using the usual technique.

We observe that for any $n>0$
$$\begin{align}|\xi_1- \xi_2| &\leq |\xi_1-a_n|+|\xi_2-a_n| \\&\leq |\xi_1-b_n|+|a_n-b_n|+|\xi_2-b_n|+|a_n-b_n|\end{align}$$
Since $\xi_1,\xi_2$ are in the intervals $[a,b]$, we must have that
$$|\xi_1-b_n|+|\xi_2-b_n|\leq2|a_n-b_n|$$
Let $\varepsilon > 0$, then there exists $N>0$ such that 
$$
|a_n-b_n| < \frac{\varepsilon}{4}
$$
and therefore we know that
$$|\xi_1-\xi_2| \leq 4|a_n-b_n| < \varepsilon$$
and we can conclude that $\xi_1 = \xi_2$.

**Existence.** We will exploit the least [[Constructions of R|least upper bound]] property of $\mathbb R$.

The proof will start from the following principle. We know that, given any $N$, then any $n\geq N$ will have that 
$$a_N \leq a_n \leq b_n \leq b_N$$
Consider the set $A = \qty{a_n : n\geq 1}$. The sequence $(a_n)$ is bounded by $a_N,b_N$ hence $A$ is bounded. Since $A$ is bounded, there exists a supremum $\sup A$ i.e. for all $n\geq 1$ 
$$a_n \leq \sup A$$
We will need to show now that every $b_n$ is an upper bound to $A$. Set $k\geq 1$. Then for all $n\leq k$ we must have that
$$a_n\leq a_k < b_k$$
Then since all $l\geq k$ has $b_k \geq b_l$, we know that all $b_l \geq a_n$ for any $n$ and $l\geq n$.

So $b_n$ are upper bounds for $A$, hence $\sup A \in I_n$ for any $n\geq 1$.

### Theory

