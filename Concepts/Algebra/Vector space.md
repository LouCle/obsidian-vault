**References.** #algebra

> [!INFO] Definition 1
> A *vector space* is a tuple $(V,F,\odot, \oplus)$ where $F$ is a [[Field|field]], $V$ is the set of *vectors* and the operators are defined as
> $$\oplus : V \times V \to V,~~~ \odot : F \times V \to V$$
> satisfying the following axioms for vectors $u,v,w \in V$ and scalars $a,b\in F$:
> 1. $u+(v+w) = (u+v)+w$
> 2. $u+v=v+u$
> 3.  $\exists 0 \in V$ with $v+0 = v$
> 4.  $\exists (-v) \in V$ with $v + (-v) = 0$
> 5. $a(bv) = (ab)v$
> 6. $1_F v = v$
> 7. $a(u+v) = au + av$
> 8. $(a+b)v = av + bv$

> [!NOTE] Definition 2
> A *vector space* over a [[Field|field]] or [[Skew field|skew field]] $F$ is a [[module]] over the [[Ring|ring]] $F$.

> [!INFO] Definition 3
> A vector space may be less commonly defined from the following two properties:
> 1. $(V,+)$ forms an [[Group|abelian group]].
> 2. There exists a [[Ring|ring homomorphism]] $\varphi : F \to \mathrm{End}(V)$.
>    
>See [[Equivalence of Vector Space Definitions]] for an explanation.

### Theory

**Theorem.** The following algebraic properties follow from the definition:
1. $0_F v = 0_V$
2. $a0_V = 0_V$
3. $(-1)v = -v$
4. $av = 0$ implies $s= 0$ or $v=0$

*Proof.* No.

**Definition.** A *linear map* or *vector space homomorphism* of vectors spaces $V$ and $W$ over the field $F$, is a map $T: V \to W$ such that $$T(av+_Vb) = a\odot_WT(v)+_WT(b)$$
Obviously I won't be denoting explicitly the origin space of an operation, because it's almost always immediately clear from the domain and codomain of the transformation.

**Theorem.** A linear map $T:V\to W$ has $T(0_V) = 0T(v) = 0_W$.

See also [[Linear map||linear map]].
### Examples