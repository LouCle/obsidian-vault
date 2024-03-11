**References.** #category-theory 

> [!INFO] Definition
> We say that $V\otimes W$ together with a bilinear map $\otimes : V\times W \to V\otimes W$ in $\mathbf{Vect}$ is the *tensor product* of $V$ and $W$, which satisfies the [[Universal property|universal property]] that for any bilinear map $f:V\times W \to Z$, there exists a unique map $h:V\otimes W \to Z$ such that the following diagram commutes
> ```tikz
> \usepackage{tikz-cd}
> \tikzcdset{scale cd/.style={every label/.append style={scale=#1},
>     cells={nodes={scale=#1}}}}
> \begin{document}
> \begin{tikzcd}[scale cd=1.8]
> {V\times W} && {V\otimes W} \\ \\ && Z \arrow["f"', from=1-1, to=3-3] \arrow["{\exists !h}", dashed, from=1-3, to=3-3] \arrow["\otimes", color={rgb,255:red,214;green,92;blue,92}, from=1-1, to=1-3]
> \end{tikzcd}
> \end{document}
> ```
> 

### Theory

**Theorem.** The tensor product is a functor $\otimes : \mathbf{Vect} \times \mathbf{Vect} \to \mathbf{Vect}$. 

*Proof.* See [[Tensor Product is a Functor]].

**Theorem.** The tensor product is associative i.e. $U \otimes (V\otimes W) \cong (U\otimes V) \otimes W$.

*Proof.* 

### Examples