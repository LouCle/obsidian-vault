**References.** #topology

> [!INFO] Definition
> A *topological space* $(S,\tau)$ is a set together with a *topology* on $S$. The topology $\tau$ consists of subsets of $S$ called *open sets* in the topological space, satisfying the following axioms
> 
> 1. $\emptyset$ and $S$ belongs to $\tau$.
> 2. $\tau$ is closed under arbitrary unions.
> 3. $\tau$ is closed under finite intersections.

> [!INFO] Idea
> Topological spaces are a generalization of metric spaces, where open sets are defined by containing an open ball at each point of the set. 
> 
> The property of continuity in metric spaces is equivalent to reflecting open sets. This inspires us to extract the properties of open sets from metric spaces, which forms the topological space axioms.

### Open sets

**Definition.** A subset of $S$ is called a *closed set* if its complement is in $\tau$.

The complement is defined $U^c = S-U$ for a subset $U\subseteq S$.

**Proposition.** The sets $\emptyset$ and $S$ are both open and closed (called *clopen*).

*Proof.* Clearly $\emptyset^C = S$ and hence either have an open set as their complement.

**Definition.** The *closure* of a set $S\subseteq X$ is the union of $S$ and its boundary $\partial S$. 

**Definition.** The *interior* of a subset $S\subseteq X$ is the union of all subsets of $S$ which are open sets in $X$. A point that is interior to $S$ belongs to the interior of $S$.

The interior is the complement of the closure of the complement of $S$.

**Definition.** The *exterior* of a subset $S\subseteq X$ is the complement of the closure of $S$.

### Examples

**Example.** Any set $S$ together with the powerset $\mathcal P(S)$ forms a topological space, referred to as the *discrete space*. The topology itself is accordingly called the *discrete topology*.

**Example.** Any [[Metric space|metric space]] $(X, d)$ induces a topology on $X$ called the *metric topology*. The topology consists of all open balls in $X$.

**Example.** $\mathbb R$ together with the usual metric forms the *[[Topology on R|usual topology on]] $\mathbb R$*. 
