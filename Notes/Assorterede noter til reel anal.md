Dette notesæt indeholder *samtlige* definitioner og sætninger fra og med kapitel 3 i Analyse 0 bogen. Der er også diverse kommentarer, opgaveløsninger og lignende, som kan være til nytte.
## Topologi m.m. på $\mathbb R$ 

**Definition.** Den sædvanlige distancefunktion/metrik på $\mathbb R^n$ er $|a-b|$ for $n=1$ 
og $||a-b||$ for $n>1$. I dette notesæt skriver vi altid $d(a,b)$ for $a,b\in \mathbb R^n$, så vi kan nøjes med at inkludere de mest almene definitioner.

**Definition.** En *kugle* $K(a, \rho)$ er mængden $$K(a,\rho) = \qty{x\in \mathbb R : d(x,a) < \rho}$$En lukket kugle inkluderer $\rho$ i distancen.  På engelsk er en anden notation for en kugle $B_\rho(a)$ og en lukket kugle $B_\rho[a]$. 

**Definition.** En *åben mængde* $A$ er en mængde sådan at for hver $x\in A$, så findes der en $\rho>0$ sådan at $K(x,\rho) \subset A$.

Både $\mathbb R$ og $\emptyset$ er åbne, og en fællesmængde af åbne mængder er også åben.

**Definition.** En *afsluttet mængde* $A$ har at $A^c$ er en åben mængde.

**Definition.** Et *åbent interval* i $\mathbb R$ er et interval $(a,b)$ hvor $a,b \in \mathbb R\cup\{\pm \infty\}$. 

Et åbent interval er altid en åben mængde.

**Definition.** Et *lukket interval* i $\mathbb R$ er et interval $[a,b]$ på den sædvanlige måde.

Et lukket interval er en afsluttet mængde da $[a,b]^c = (-\infty, a) \cup (b, \infty)$.

**Definition.** Et *halv-åbent interval* i $\mathbb R$ er et interval $[a,b)$ eller $(a,b]$ på den sædvanlige måde.

Et halvt-åbent 

**Definition.** En *afsluttet mængde* (på engelsk: *closed set*) er komplementært til en åben mængde.

Man kunne tænke at dette betyder at det at være afsluttet udelukker det at være åben, men det er ikke tilfældet. Lige netop på $\mathbb R$ er der dog kun to mængder som er begge dele (på engelsk: *clopen*), nemlig $\emptyset$ og $\mathbb R$. Begge er åbne mængder, og derfor er begge deres komplementærmængder selvfølgelig også begge åbne.

Et eksempel på et ubegrænset og afsluttet interval i $\mathbb R$ er $[0,\infty)$. Den er opad ubegrænset, og er komplementær til $(-\infty, 0)$ som er et åbent interval. Til tider kræver nogle definitioner  af et interval både skal være afsluttet og begrænset, og grunden er simpelthen at afsluttede intervaller i sig selv kan være alt for store som demonstreret i eksemplet.

**Definition.** Et *fortætningspunkt* (på engelsk: *limit point*) $a$ til en mængde $A$ er et punkt sådan at for alle $\rho > 0$, findes der en $q\neq a$ i $E$ med $q\in K(a, \rho)$.

I ovenstående behøver $a$ ikke være i $A$, og typisk er fortætningspunktet det heller ikke.

I definitionerne i An0 bogen ligger overvejes der oftest fortætningspunkter i $\bar A - A$. 

  
# Kapitel 2
## Grænseovergange

**Definition 2.15.** Definér $f:A\subset \mathbb R^k \to \mathbb R^m$ og lad $a$ være et fortætningspunkt til $A$. Vi siger at $$f(x) \to b~~~ \mathrm{for} ~ x \to a,~x\in A$$hvis at $$\forall \epsilon > 0~\exists \delta > 0: ~~~ d(f(x),b) < \epsilon~~~\forall x \in A ~~\mathrm{med}~~d(x,a) < \delta.$$
**Definition 2.41.** En funktion $\epsilon:A \subset \mathbb{R}^k \to \mathbb{R}^m$ er en *epsilon-funktion* i en grænseovergang $x \to a,~x \in A$ hvis $$\epsilon(x) \to 0~~~~~~x\to a,~x\in A.$$
## Udvalgte opgaver og eksempler

**Kontrolopgave 2.1.** Kan en funktion $f : \mathbb Z \times \mathbb Z \to \mathbb R$ have en grænseværdi for $(x,y) \to (0,0)$?

*Bevis.* Sæt at $f(x,y) \to c$ for $(x,y) \to (0,0)$. 


# Kapitel 3

## 3.1 Kontinuitet 

**Definition 3.1.** En afbildning $f : A \subset \mathbb R^k \to \mathbb R$ siges at være *kontinuert i punktet* $a \in A$ hvis $$\forall \epsilon > 0 ~ \exists \delta > 0: ~~~~ d(f(x),f(a)) < \epsilon,~~~ \forall x \in A,~ d(x,a) < \delta$$
Er $a$ et ikke-isoleret punkt i mængden $A$ kan vi udtrykke kontinuitet som grænseovergangen $$\Delta f \to 0~~~~~~\mathrm{for}~~\Delta x \to 0,~a + \Delta x \in A$$med $\Delta x = x - a$ og $\Delta f = f(x) - f(a) = f(a + \Delta x) - f(a)$.

**Sætning 3.8.** Lad $A \subset \mathbb R^k$ og $B \subset \mathbb R^l$ være mængder, lad $f: A \to B$ og $g : B \to \mathbb R^m$ være afbildninger, og lad $a \in A$ være et punkt. Hvis $f$ er kontinuert i $a$ og $g$ er kontinuert i $b = f(a)$, så er $g \circ f$ kontinuert i $a$.

**Sætning 3.9.** En afbildning $f = (f_1, \dots , f_m) : A\subset \mathbb R^k \to \mathbb R^m$ er kontinuert i et punkt $a \in A$ hviss. samtlige $f_i$ er kontinuerte i $a$.

Jf. Definition 3.1 har vi

**Definition 3.2.** En afbildning $f : A \subset \mathbb R^k \to \mathbb R^m$ er kontinuert (i hele $A$) hviss. $$\forall a \in A~\forall \varepsilon > 0~\exists \delta > 0: ~~ d(f(x), f(a)) < \varepsilon~~~\forall x \in A~d(x,a) < \delta$$
#### Den reelle akses egenskaber

**Definition.** En mængde $A$ er opad begrænset hvis der findes et tal $b$ sådan at for alle $a \in A$, så er $b \geq a$. 

Tallet $b$ kaldes et *overtal* (på engelsk: *upper bound*). 

**Definition 3.17a.** Lad $A \subset  S$ være en ikke-tom, opad begrænset mængde. Et *supremum* (på engelsk: også *least upper bound*) for $A$ er et tal $\sup A \in S$ med egenskaben at det er det laveste overtal $c$:
$$\forall a \in A~: a \leq c \implies \sup A \leq c.$$

**Definition 3.17.b.** Lad $A \subset S$ være en ikke-tom, nedad begrænset mængde. Et *infinimum* (på engelsk: også *greatest lower bound*) for $A$ er et tal $\inf A \in S$ med egenskaben at det er det højeste undertal $c$: $$\forall a \in A : a \geq c \implies \inf A \geq c$$
**Aksiomatisk konstruktion af $\mathbb R$**. Talsystemet $\mathbb R$ er et komplet, totalt ordnet legeme med egenskaben at enhver ikke-tom, opad begrænset mængde har en supremum.

Det følger af kontinuetsaksiomet/supremumsegenskaben at $\mathbb R$ har den Arkimediske egenskab, altså at til ethvert $x\in \mathbb R$ findes $n\in \mathbb N$ sådan at $x<n$.

At et ordnet legeme er komplet (i forhold til en metrik), vil sige at hver Cauchyfølge defineret i metrikrummet har en grænseværdi i metrikrummet. 

Alternativt er det også nok at sige at $\mathbb Q$ er tæt i $\mathbb R$.

**Definition.** En mængde $A\subset \mathbb R$ er tæt i $\mathbb R$ hvis det for hvert par $a,b\in \mathbb R$ med $a<b$ gælder at $$(a,b) \cap A \neq 0$$
Altså at hvert åbent interval i $\mathbb R$ indeholder noget fra $A$. 

Men hidtil i An0 foretagende er supremumegenskaben/kontinuitetsaksiomet det vigtigste.

**Definition.** En *ruse* er en uendelig følge af afsluttede/lukkede og begrænsede intervaller $I_1 = [a_1,b_1], I_2 = [a_2,b_2]\dots$ sådan at $$I_1 \supset I_2 \supset I_3 \supset \cdots $$
**Lemma 3.20 (Ruse-lemmaet).** Lad $(I_n)^\infty_{n=1}$ være en ruse på $\mathbb R$ med egenskaben at 
$$b_{n+1} - a_{n+1} = \frac{b_n - a_n}{2}$$
for $n\geq 1$. Vi skriver også $|I_n| = b_n - a_n$. Da findes præcist ét tal $\xi \in \mathbb R$ sådan at $\xi \in I_n$ for alle $n\geq 1$. 

I An0 bogen er ruse-lemmaet givet sådan at hvert interval spænder den halve distance af det sidste. Det egentlige krav er bare at $$\forall \epsilon > 0~\exists N>0 ~~ |I_n|< \epsilon$$Med $n\geq N$. Altså at man altid kan finde et vilkårligt "lille" interval i følgen. Man bruger blandt andet supremumegenskaben på $\mathbb R$ til at vise eksistensdelen af ruselemmaet. 

**Sætning 3.21.** Enhver ikke-tom nedad begrænset mængde $A \subset \mathbb R$ har et infinum.

Beviset anvender ruselemmaet.

**Note.** Konventionelt, hvis en mængde $A$ er opad begrænset så siges den at have $\sup A < \infty$, og ligeledes hvis $A$ er nedad *u*begrænset, så er $\inf A = -\infty$. 

## 3.2-3.5 Hovedsætninger

En funktion $f: A \to \mathbb R$ er hhv. op- og nedadbegrænset når værdimængden $f(A)$ er det. En største- og mindsteværdi er hhv. $\max f(A)$ og $\min f(A)$. 

**Sætning 3.22 (Hovedsætning 1).** Enhver kontinuert funktion $f : [a,b] \to \mathbb R$ på et afsluttet og begrænset interval $[a,b] \subset \mathbb R$, er begrænset og har en største- og mindsteværdi.

Denne sætning kaldes ekstremalværdisætningen (på engelsk: *extreme value theorem*).

**Sætning 3.25 (Hovedsætning 2).** Lad $f:A \to \mathbb R$ være en funktion på et afsluttet, begrænset interval $A=[a,b]$. Billedmængden $f([a,b])$ er intervallet $[f(a),f(b)]$.

**Korollar 3.26.** Lad $f : I \to \mathbb R$ være en kontinuert funktion på et interval $I$, da er $f(I)$ et interval.

**Sætning 3.28.** En kontinuert og strengt voksende funktion $f : I \subset \mathbb R \to \mathbb R$ har en kontinuert og strengt voksende omvendt funktion $f^{-1}$ defineret på $J=f(I)$.

**Definition 3.34.** En afbildning $f: A \subset \mathbb R^k \to \mathbb R^m$ er uniformt kontinuert hvis $$\forall \varepsilon > 0~\exists \delta > 0 ~~~d(f(y),f(x)) < \varepsilon~~~ \forall x,y \in A ~~d(y,x) < \delta$$
**Sætning 3.36.** En uniformt kontinuert afbildning $f: A\subset \mathbb R^k \to \mathbb R^m$ er kontinuert i $A$.

**Definition 3.37.** En afbildning $f: A \subset \mathbb R^k \to \mathbb R^m$ er Lipschitz hvis der findes et $K>0$ sådan at $$d(f(y),f(x)) \leq K\cdot d(y,x)~~~\forall x,y\in A$$
og $K$ kaldes en Lipschitz-konstant for afbildningen. Er en afbildning Lipschitz er den også uniformt kontinuert, og derved også kontinuert.

**Korollar.** Enhver affin afbildning er uniformt kontinuert.

**Sætning 3.40 (Hovedsætning 3).** Lad $I$ være et afsluttet, begrænset interval på $\mathbb R$, da er en kontinuert funktion $f: I \to \mathbb R$ uniformt kontinuert.

Hovedsætning 3 gælder også for kontinuerte afbildninger ind i et vilkårligt rum $\mathbb R^k$. 

**Sætning 3.41.** Lad $f:(a,b) \to \mathbb R$ være en reel funktion på et åbent, begrænset interval. Da findes en kontinuert funktion $g :[a,b]\to \mathbb R$ med $g(x)=f(x)$ for alle $x\in (a,b)$ hvis og kun hvis at $f$ er uniformt kontinuert.

## Opgaver og eksempler

**Eksempel.** Dirichlets funktion $f:\mathbb R \to \mathbb R$ givet ved
$$f(x)=\begin{cases}1&x\in \mathbb Q\\0&x\not\in \mathbb Q\end{cases}$$
er diskontinuert i ethvert punkt $x\in \mathbb R$.

**Eksempel.** Thomaes funktion $g : (0,1] \to \mathbb R$ givet ved $$g(x) = \begin{cases}\frac{1}{q} & x\in \mathbb Q,~x=\frac{p}{q} \\0&x\not\in \mathbb Q\end{cases}$$hvor $\frac{p}{q}$ er en uforkotelig heltalsbrøk. Thomaes funktion $g$ er diskontinuert i ethvert $x\in \mathbb Q \cap(0,1]$ og $g$ er kontinuert i ethvert $x\in(0,1]-\mathbb Q$.


# Kapitel 4

## 4.1 Differentiabilitet

**Definition 4.1.** Funktionen $f:I \subset \mathbb{R} \to \mathbb R^m$ er *differentiabel i punktet* $a\in I$ med $f'(a)=c\in \mathbb{R}$ hvis 
$$
\frac{f(a+\Delta x) - f(a)}{\Delta x} \to c~~~~~~ \Delta x \to 0
$$
Vi kan også formulere ovenstående som at $$\Delta f = c \Delta x + \epsilon(\Delta x)\Delta x$$
Hvor $\epsilon$ er en epsilon-funktion.

**Sætning 4.6.** Lad $f : I \subset \mathbb{R} \to \mathbb{R}^m$ være en funktion. Da er $f$ differentiabel hvis og kun hvis at dens koordinatfunktioner er differentiable.

**Sætning 4.8.** Hvis $f : I \subset \mathbb{R} \to \mathbb{R}^m$ er differentiabel i et punkt $a \in I$ så er $f$ kontinuert i $a$.

**Sætning 4.9.** Lad $f: I \subset \mathbb{R} \to \mathbb{R}^m$, $g:I \subset \mathbb{R} \to \mathbb{R}^m$ og $\alpha : I \to \mathbb{R}$ være differentiable i $a\in I$. Da er følgende konstruktioner differentiable i $a$: 
$$f\pm g,~~ f\cdot g,~~ \alpha f.$$
**Sætning 4.11 (Kædereglen).** Lad $I$ og $J$ være reelle intervaller og betragt funktioner $f: I \to J$ og $g: J \to \mathbb{R}^m$. Lad $f$ være differentiabel i $t_0 \in I$ og $g$ i $f(t_0)\in J$. Så er $g \circ f$ differentiabel i $t_0$ med $$
(g \circ f)'(t_{0}) = g'(f(t_{0}))f'(t_{0})
$$
