**References.** #category-theory

> [!INFO] Definition
> Let $\mathscr C$ be a category and $P: \mathscr C \to \mathbf{Set}$ a functor. Fix an object $c \in \mathscr C$. 
> 
> We say that $c$ satisfies the *universal property* with respect to $P$ if there is some 
 
 ```tikz
\usepackage{tikz-cd}
\tikzcdset{scale cd/.style={every label/.append style={scale=#1},
    cells={nodes={scale=#1}}}}
\begin{document}
\begin{tikzcd}[scale cd=1.9]
Fc && Gc \\ \\ {Fc'} && {Gc'} \arrow["Ff"', from=1-1, to=3-1] \arrow["{\alpha_c}", from=1-1, to=1-3] \arrow["Gf", from=1-3, to=3-3] \arrow["{\alpha_{c'}}"', from=3-1, to=3-3]
\end{tikzcd}
\end{document}
```





> 

> [!INFO] Less formal definition
> Let $\mathscr C$ be a category and let $\mathscr D$ be an over- or undercategory on $\mathscr C$ determined by a property. A construction $(\phi, C)$ in $\mathscr {C}$ is said to be universal with respect to the property if it is a terminal object in $\mathscr D$.
> 
> 

This is way too small

### Examples2

- 