**References.** #analysis 

> [!INFO] Theorem
> Let $A\subseteq \mathbb R$ be a non-empty bounded set with supremum $\sup A$. Then $\sup A$ is in the closure of $A$.
> 
> 
### Proof

**Case 1.** If $\sup A \in A$ then it is also in the closure $\bar A = A' \cup A$.

**Case 2.** If $\sup A \notin A$ then we know that $\sup A$ is an upper bound to $A$. Assume that there exists an $\varepsilon > 0$ such that $(L-\epsilon, L] \cap A$ is empty. That must mean that there exists an upper bound $L' < L$, but this contradicts that $L$ is the supremum. 

So there must be a number $a \in (L-\epsilon,L] \subset B_\epsilon(L)$ for any $\epsilon >0$, which means that $\sup A \in A'$.

In both cases we have that $\sup A \in \bar A$.
### Examples