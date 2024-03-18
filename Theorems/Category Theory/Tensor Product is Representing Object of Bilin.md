**References.**

> [!INFO] Theorem
> The tensor product $V\otimes W$ in $\mathbf{Vect}_k$ is a representing object for the functor $$\mathrm{Bilin(V,W,-) : \mathbf{Vect} \to \mathbf{Set}}$$
> 
> 
### Proof

By [[Universal property]] $V\otimes W$ is a representing object for $\mathrm{Bilin}(V,W; -))$ if there exists a universal element $x\in \mathrm{Bilin}(V,W; V\otimes W))$.

In other words, there exists a bilinear map $x : V\times W \to V\otimes W$ so that for any space $Z$ and bilinear map $f:V\times W \to Z$ there exists only one map $h : V\otimes W \to Z$ so that $\mathrm{Bilin}(h)(x) = f$.

By [[Composition with Bilinear Map is Bilinear]] we understand $\mathrm{Bilin(-)}$ to be $$\mathrm{Bilin}(-) = - \circ g : \mathrm{Hom}(V\times W,X)\to \mathrm{Hom}(V\times W,Y)$$ Hence we get the morphism
$$\mathrm{Bilin}(h) : \mathrm{Hom}(V\times W,V\otimes W) \to \mathrm{Hom}(V\times W,Z)$$
The universal property of [[Tensor product on Vect]] tells us that any map 

So if V \otimes W is a representing object for Bilin(V,W; -) there's a universal element x in Bilin(V,W; V \otimes W) / i.e. there exists a map x : V x W → V \otimes W) so that for any space Z and bilinear map f : V x W → Z there exists only one map h : V \otimes W → Z such that, (however Bilin acts on h)(x) = f. So my approach was that since Bilin(-) corresponds to composing with a bilinear transformation (?) y : V x W → Z (by your theorem), then from there we should be able to copy-paste the universal property of the tensor product which tells us that the universal element y = x : V x W → V \otimes W does actually have exactly one h : V \otimes W → Z so that h o x = f (so these must be isomorphic constructions)
### Examples