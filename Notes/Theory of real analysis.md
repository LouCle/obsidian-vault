**References.** #analysis 

  ```table-of-contents
```
## Standard theory

Most has been packaged into the concept pages.

**Concept page.** [[Limit on R]].

**Concept page.** [[Continuity on R]].

**Concept page.** [[Differentiability on R]].

## Techniques

### General

**Technique.** Budget your epsilons i.e. if the aim is to show that the construction $z < \epsilon$, we might have an easier time showing that $z=z_1+z_2 < \epsilon/2 + \epsilon/2$.

**Technique.** To show that a construction $z = 0$ we can show that $z < \epsilon$ for every $\epsilon>0$. In general in a metric space, to show that $z_1 = z_2$, we can show that $d(z_1,z_2) < \epsilon$ for any $\epsilon > 0$.

See for example [[Limit is Unique]] which uses both of the above techniques.

**Technique.** It's very often easier to show that a construction $x=y$ by proving that $x\geq y$ and $x\leq y$. Similarly, to show set equivalence, show that either set is $\subseteq$ of the other.

**Technique.** It's often useful to play around with quantities in the triangle inequality. Occasionally, if we have only certain information available, we can coax more information out by applying the triangle inequality.

**Technique.** Try to construct auxiliary sets satisfying $P$.

See the existence proof of [[Nested Interval Theorem]].

**Technique.** Try to construct auxiliary functions satisfying $P$ to prove statements about a weaker property $Q$ for a more general class of functions. 

See the [[Mean Value Theorem|proof of MVT]].

**Technique.** Exploit the trivial factorization of a function $f(x) = 1 \cdot f(x)$. 

See ex. [[Antiderivative of Inverse Hyperbolic Functions]].

**Technique.** Showing continuity, continuity, differentiability etc. on a domain, it may be easier to prove it on select sub-regions of the domain.

See the proof that [[Continuous Function with Infinite Limits is Uniformly Continuous]].

**Technique (terrytao blog).** Decompose rough objects into simpler ones.
- Measurable set → open, closed, compact, bounded or elementary set
- Measurable function → continuous, bounded, compactly supported, simple or etc.
- Infinite sum or sequence → finite truncations (keeping the bounds independent of the number of terms in the truncation)
- Complex-valued functions → real-valued functions
- Real-valued functions → unsigned functions
- Simple functions → indicator functions

**Technique.** Search for counterexamples in the obvious fashion.
### Limits

**Technique.** For any $\epsilon-\delta$ proof, if you a $\delta_1$ for all epsilons in $0<\epsilon<\epsilon_1$, it suffices to pick $\delta_1$ for anything above $\epsilon_1$.

**Technique.** Try dividing limits into their single-limits to exploit certain properties. 

See for example the proof [[Derivative at Maximum is Zero]].

### Integration

**Technique.** For integration by parts, ^99a58d
### Examples