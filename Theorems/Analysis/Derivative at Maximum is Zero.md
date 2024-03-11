**References.** #analysis 

> [!INFO] Lemma
> Let $f: I \to \mathbb R$ be defined on an interval $I$. Assume that $a$ is an [[Topology on R|interior point]] in $I$ and that $$f(x)\leq f(a)~~~~\forall x \in I$$If $f$ is differentiable in $a$, then $f'(a) = 0$
> 
> 

### Proof

The aim will be to show that $f'(a) \leq 0$ and $f'(a) \geq 0$.

Define the following expression 
$$g(x) = \frac{f(x)-f(a)}{x-a}.$$
Assuming that $f$ is differentiable in $a$, then by the [[Differentiability on R|definition of differentiability]] we have that 
$$\lim_{x\to a} g(x) = f'(a)$$
This limit must have a right-limit 
$$\lim_{x\downarrow a} g(x) = f'(a)$$
Since $f(x)-f(a) \leq 0$ and $x -a > 0$ by the definition of [[Limit#^d74a70|right limit]], we have that ${} g(x) \leq 0$. Then by [[Image in Closed Set S implies Limit in S]] the limit must have $f'(a)\leq 0$ as well.

Same argument with the left limit, whereafter we get $f'(a) \geq 0$, which implies that $f'(a) = 0$.

### Examples