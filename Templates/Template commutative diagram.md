```tikz
\usepackage{tikz-cd}
\tikzcdset{scale cd/.style={every label/.append style={scale=#1},
    cells={nodes={scale=#1}}}}
\begin{document}
\begin{tikzcd}[scale cd=1.8]
X && {P(A)} && A \\ \\ && {P(A')} && {A'} \arrow["f"', from=1-1, to=3-3] \arrow["{P(h)}", dashed, from=1-3, to=3-3] 
\arrow["{\exists!h}", dashed, from=1-5, to=3-5] \arrow["u", color={rgb,255:red,214;green,92;blue,92}, from=1-1, to=1-3]
\end{tikzcd}
\end{document}
 ```
 