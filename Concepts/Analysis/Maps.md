**References.**

> [!INFO] Definition
> A *map* or a *function* $f$ is a tuple $(X,Y,\sim)$ with a domain $X$, a codomain $Y$ and a relation $\sim$ on $X\times Y$ satisfying the *vertical line test* that 
> $$\forall x \in X~ \exists! y \in Y~~~~x \sim y$$
> We denote the map by $f : X\to Y$ and we say that $f(x) = y$ if $x \sim y$.
> 
> 
> 
> 

### Properties of maps

**Definition.** To any maps $f:X \to Y$ and $g : Y \to Z$  we can define a map $g \circ f : X \to Z$ which satisfies that $$(g \circ f)(x) = g(f(x))$$called their composition. 

The map is well-defined as it retains the domain of $f$.

**Definiton.** A map $f:X\to Y$ is *injective* if $$\forall x,y~~~~f(x) = f(y) \implies x = y$$
A map is injective if it is a monomorphism in the category $\mathbf{Set}$ i.e. for all maps $g_1,g_2: Z \to X$ it holds that $$f\circ g_1 = f \circ g_2 \implies g_1 = g_2$$
**Definition.** A map is *surjective* if $$\forall y~\exists x~~~f(x) = y$$
Likewise a map is surjective if it is an epimorphism in $\mathbf{Set}$, which is to say, for all maps $g_1,g_2 : Y \to Z$ we have that $$g_1 \circ f = g_2 \circ f\implies g_1 = g_2$$
### Examples