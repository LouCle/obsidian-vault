**References.** #category-theory

> [!INFO] Definition 1
> Let $\mathscr C$ and $\mathscr D$ be categories and let $P: \mathscr C \to \mathscr D$ be a functor. We say that the object and morphism $(X,u)$ of $\mathscr D$ is a universal construction with respect to $P$ if, for any morphism $f:X \to P(A')$ in $\mathscr D$, there exists a unique map $h:A \to A'$ in $\mathscr C$ such that the following diagram commutes
>  
>  ```tikz
> \usepackage{tikz-cd}
> \tikzcdset{scale cd/.style={every label/.append style={scale=#1},
>     cells={nodes={scale=#1}}}}
> \begin{document}
> \begin{tikzcd}[scale cd=1.8]
> X && {P(A)} && A \\ \\ && {P(A')} && {A'} \arrow["f"', from=1-1, to=3-3] \arrow["{P(h)}", dashed, from=1-3, to=3-3] \arrow["{\exists!h}", dashed, from=1-5, to=3-5] \arrow["u", color={rgb,255:red,214;green,92;blue,92}, from=1-1, to=1-3]
> \end{tikzcd}
> \end{document}
> ```
> 

> [!INFO] Less formal definition
> Let $\mathscr C$ be a category and let $\mathscr D$ be an over- or undercategory on $\mathscr C$ determined by a property. A construction $(\phi, C)$ taken from $\mathscr {C}$ is said to be universal with respect to the property if it is a terminal object in $\mathscr D$.
> 
> 

### Examples

**Example.** Products, coproducts and fiberproducts/pullbacks.

**Example.** The tensor product.