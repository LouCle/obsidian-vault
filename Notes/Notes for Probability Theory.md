## Notes to Chapter 1
#### Sample spaces
- A *sample space* $S$ of an *experiment* is the  set of all possible outcomes of the experiment. An *event* $A$ is a subset of the sample space $S$, and we say that $A$ occurred if the actual outcome is in $A$. That is to say, some function takes us from the *sample space* of possible outcomes to an *actual outcome*.
- In the set interpretation, thus an outcome in $A\cup B$ is equivalent to either $A$ or $B$ having occured, and the outcome in $A\cap B$ means that both must have occured. As well as De Morgan's laws applying.
- Modeling a sample space of 10 coin flips as strings like $HTH\dots T$, we may encode $H$ as $1$ and $T$ as $0$, so that an outcome is such a sequence of numbers.
- Let $A$ be the event that the first flip is heads, thus, this event is the set of all sequences where $s_1=1$. An event occuring is equivalent to an actual outcome abiding by the condition denoted by the event, i.e. the actual outcome has the first number $1$.
- Let $B$ be an event that at least one flip was $H$. Denote a sequence by $A_j$ if the $j$-th flip is $H$. Then $B$ is $$B=\bigcup^{10}_{j=10} A_j$$
- That all are $H$ we can of course denote with the intersection.
- Let $D$ be the event that there are two consecutive $H$, then we have the union of all events that have two $H$ next to each other, i.e. $$D=\bigcup^{9}_{j=10} A_j\cap A_{j+1}$$
- Notice that the bound was set to $9$ in this case.

#### Naive definition of probability
- Let $A$ be an event (a subset) of a finite sample space $S$. The *naive probability* of $A$ is $$\tilde P (A) = \frac{|A|}{|S|}$$
- In other words, the ratio of the quantity of possible outcomes in $A$ to the total number of possible outcomes in $S$.
- Notice also that $$\tilde P(A^c) = \frac{|S|-|A|}{|S|} = 1 - \tilde P(A)$$
- This holds not only for the naive definition. Sometimes it's easier to find the probability of the complement of an event, this comes to show in that working with intersections is typically easier than unions (proving statements with AND vs. OR).
- But are the outcomes themselves not equally likely, or if they are infinite, then the naive definition is indeed not very useful for our probability theory.
- When is the naive definition applicable?
  - When there is *symmetry* which makes outcomes equally likely (one side of a coin has $0.5$ likelihood, this leaves, naturally, $1-0.5$ likelihood for the other side, since we only get the other side exactly if we didn't get the one side).
  - When the outcomes are equally likely *by design*.
  - When we are interested in a so-called *null model*, where we assume that the naive definition applies to study the probabilities it obtains, and can then evaluate the tenacity of a hypothesis involving equally likely outcomes.
#### Counting methods
- Calculating the (naive) probability of an event $A$ involves counting the number outcomes in $A$ and the number of total outcomes in the sample space. Those sets are oftentimes quite large, and therefore some methods are required to determine the respective cardinalities.
- **Multiplication rule**. This method states that, given some experiments with sizes $a_i$, their compound size $|S|=a_1 \cdots a_n$. If we have two experiments, then the intuition is to consider that to each possibility in the first experiment, is all the possibilities of the second experiment, and the total amount thus consists in $a$ possibilities, $b$ times. Sometimes we consider these in chronological order, since were the experiments performed physically, they range in time.
- Consider 10 people running a race. How many possibilities are there for first, second and third place winners? Fix $10$ possibilities for the first place (i.e. we are running an 'experiment' on $10$ people to evaluate who will get the first place). Then there is an experiment for who gets the second place. Such an experiment assumes that a person already has the first place, hence there must be $9$ possibilities. The same for the third place, with $8$ possibilities. The multiplication rule states that there are $10\cdot 9 \cdot 8 = 720$ possible outcomes in the compound experiment.
- **Set cardinality**. A set with $n$ elements has $2^n$ subsets.
- **Sampling with replacement.** Consider $n$ objects and $k$ choices of these objects, one at a time, with replacement (i.e. if we choose one object, we may choose it again). Then there are $n^k$ possible outcomes with order. This follows from the multiplication rule.
- **Sampling without replacement.** This also follows from the multiplication rule, and has $\frac{n!}{(n-k)!}$ possible outcomes, insofar as $1\leq k \leq n$ and $k>n$ yields $0$ possibilities. Per convention $(n,k=1)$ yields $n$ possibilities.
- **Permutations.** There are $n!$ permutations of $n$ objects.
- **Birthday problem.** *There are $k$ people in a room. Assuming that each person's birthday is equally likely to be any of the 365 days of the year, and that peoples birthdays are independent, what is the probability that at least one pair of people in the group have the same birthday?*
  - *Solution*. 
    There are accordingly, $365^k$ possible outcomes in the sample space. All that remains is to count the number of outcomes where at least two out of the $k$ people share a birthday. In this case, we may make use of the complement i.e. the number of outcomes where no one shares a birthday.
    
    This means, that if we pick a birthday for a person, then this birthday may not be occupied by someone else. Thus we may make use of the counting method *sampling without replacement*. I.e. $$\frac{n!}{(n-k)!}=\frac{365!}{{(365-k)!}}$$
    Hence the probability of no birthday matches $A$ is $$P(A)=\frac{365!}{365^k(365-k)!}$$
    And by the complement law, $$P(A^c)=1-P(A)$$
    Which yields about a $50\%$ for two people to share a birthday in a room with $23$ people.
- **Leibniz's mistake**. *Is rolling a sum of $11$ os a sum of $12$ more like, with two fair dice?*
  - *Solution.*
    Each constitute a sub-experiment, thus we make use of the multiplication rule. Here there are $6\cdot 6=36$ total possible outcomes, out of which the ordered pairs $(5,6)$ and $(6,5)$ are favorable towards a sum of $11$, and only $(6,6)$ are favorable towards a sum of $12$. So the probability of a sum of $11$ is twice that of a sum of $12$. Leibniz's mistake consists in viewing the pairs $(5,6)$ and $(6,5)$ as the same outcomes.

- **Overcounting.** If we count each possibility $c>1$ times, we can adjust for this overcounting by dividing with $c$ again. Consider the combinatorics of choosing a two-person committee out of 4 people. If we list the choices, we get
  
  > 12, 13, 14, 23, 24, 34
  
  Hence $6$ possibilities. But this is not always straight-forward. Though, if use the multiplication rule, we get $4\cdot 3 = 12$ possibilities. We start with $4$ choices for the first person on the committee, and $3$ ways for the second person. But this counts each possibility exactly twice, since we may revert the order, hence we divide by $2$ to get $6$. In other words, $${4\choose 2}=\frac{4!}{2!(4-2)!}$$
- **Binomial coeficient.** For any non-negative integers $k$ and $n$, the *binomial coefficient* $n\choose k$ is the number of subsets of size $k$ for a set of size $n$, i.e. the following relation may be derived $$2^n = \sum^n_{k=0} {n \choose k}$$
  The following equation is called the binomial coefficient equation $${n \choose k} = \frac{n!}{k!(n-k)!}$$
  The $k!$ divisor results from overcounting (for $2$ choices we always overcount the possibility twice, for $3$ by $6$ etc. since each choice in the amount of permutations $k!$ of the elements is considered the same choice). Notice that the above results from the sampling without replacement method of counting.
  
  For computation, we'd prefer to compute less factorials, so we may remove the $(n-k)!$ divisor, as that lets use set a lower bound on the product in the dividend.
  
- **Permutations of a word**. Consider a word like $LALALAAA$. We may permute it ${8\choose 5}={8\choose 3}=56$ times, since all we have to do is consider the amount of ways in which we can distribute $3$ L's in $8$ places. To understand this, consider each letter as occupying a place value $1,2\dots 8$. The question is then actually, how many subsets of those place values of size $3$ can we pick, since distributing the remaining $A$'s doesn't add any possibilities. 
  
  But this was for only $2$ letters. What about a longer word such as $STATISTICS$? This word has $10$ letters, with $S:3$, $T:3$,$I:2$, $A:1$, and $C:1$. This works out under the same principle. First we pack how many ways we can distribute the $S$'s, i.e. $10 \choose 3$. Now by the multiplication rule, each of these outcomes have some ways of distributing the remaining letters. This works out as $${10 \choose 3}{7\choose 3} {4\choose 2} {2 \choose 1}=50400$$
  Alternatively we can consider $10!$ permutations, and then divide with $3!3!2!1!$ since all the $S$'s overcount with $3!$ and so on.

#### General definition of probability
- A *probability space* consists of a sample space $S$ and a *probability function* $P$ which has $A\subseteq S \mapsto [0,1]$ for an event $A$. $P$ must satisfy the following axioms
  1. $P(\emptyset)=0, P(S)=1$ 
  2. If $A_1,A_2,\dots$ are disjoint events then $$P\left(\bigcup^\infty_{j=1}A_j\right)=\sum^\infty_{j=1}P(A_j)$$ i.e. the probability of the union of a countably infinite set of disjoint events is equal to the sum of their individual probabilities (thus allowing the possibility of inhomogenous probability distributions, whereas in the naive case this holds, though under the assumption that each outcome is individually as likely the next)
- Were we considering "pebbles" and events as subsets of "pebbles", then from this definition probability behaves like mass. The mass of an empty pile of pebbles is $0$, and the total mass of all the pebbles if $1$. If we have non-overlapping piles of pebbles, we can get their combined mass by adding the masses of the individual piles.
- Most generally, we denote a probability space as a triple $(\Omega, \mathcal F, P)$ where $\Omega$ corresponds to the sample space $S$ and $P$ to the probability function. $\mathcal F$ denotes the set of events in the probability space.
- There are major schools of thought. In *frequentism* probability represents a long-run frequency of a large number of repetitions of an experiment. In the *Bayesianism*, this represents "degrees of belief" about the event in question.
- Some theorems follow relating the probability function for some events $A$ and $B$:
  1. $P(A^c) = 1- P(A)$
  2. If $A\subseteq B$ then $P(A) \leq P(B)$
  3. $P(A\cup B) = P(A) + P(B) - P(A \cap B)$
- Notice that finite additivity follows from countable/infinite additivity if we let $A_1$ and $A_2$ be disjoint and let $A_{i>2}=\emptyset$. Together with the third sub-theorem, or the inclusion-exclusion theorem (both proofs has been ommitted in these notes) above, we can conclude, since they are disjoint and thus the probability of hte intersection is zero, finite additivity.
- Inclusion-exclusion for *any* collection of events $A_i$ 

## Notes to Chapter 2: Conditional Probability
- *Conditioning is the soul of statistics*
- **Conditional probability.** If $A$ and $B$ are events with $P(B)>0$, then the *conditional probability* of $A$ given $B$, denoted with $P(A\mid B)$ is defined as $$P(A\mid B) = \frac{P(A\cap B)}{P(B)}$$
- $P(A)$ is the *prior* probability of $A$, and $P(A\mid B)$ is the *posterior* probability, conditioned by $B$. From this it neatly follows that the probability of $A$ given $A$ is $1$.
- We can think of it as the probability of $A$ *given the evidence* of $B$, had $B$ been the case before the experiment of. Hence, consider the probability of the intersection of $A$ and $B$, i.e. the probability of an outcome favourable towards both events. Then we divide by the probability of outcomes favourable towards $B$, leaving us only with the probability of outcomes favourable towards only $A$, but which is contained in the possibility of being favourable towards $B$, though now renormalized. Notice that this is not a theorem, rather it is a definition.
- Consider a standard deck of cards. Two cards are drawn randomly, without replacement of course. Let $A$ be the event that the first card is a heart, and $B$ the event that the second card is red. There are $52\cdot 51$ total samples, since order matters. Thus we have $$P(A\cap B) = \frac{13\cdot 25}{52\cdot 51}=\frac{25}{204}$$
  i.e. the probability of an outcome being favourable towards both $A$ and $B$. $P(A)$ is simply $1/4$ since the 4 suits are equally likely, and $P(B)=1/2$ since we have removed 1 red card (a heart) with the first card.
- Now can just employ the conditional probability definition. Here the probability of $B$ given $A$ is roughly $1/2$. That is to say, the probability of the second card being red, insofar as the first card is heart and has "discarded" the additional total outcomes in the sample space for the second case, is about half. Notice that this is different than asking for the
  probability of the intersection of both events. 
- As example, consider the sample space of numbers $1$ through $10$. Let $A$ be the event that a randomly chosen number is even, and $B$ the event that it is odd. As they are equally likely, we may use the naive definition of probability, i.e. $P(A)=P(B)=\frac{1}{2}$, and the probability of their union is of course $1$. Also define an event called $C$ and let it be the subset that has the number $5$. Consider $P(A\mid B)$. The way it was defined, makes it equivalent to simply discarding the part of the sample space that does not intersect with $B$ i.e. $B^c$, and thus $P(B)$ can also be said to pertain to the sample space $S=B$. We can check this with the definition $$P(A\mid B) = \frac{0}{1/2} = 0$$ $$P(C\mid B) = \frac{0.1}{1/2} = \frac{1}{5}$$
- **Probability of the intersection of two events.** $$P(A\cap B) = P(B)P(A \mid B) = P(A)P(B \mid A)$$
- **Probability of the intersection of $n$ events.** 
- **Bayes Rule.** $$P(A\mid B) = \frac{P(B\mid A)P(A)}{P(B)}$$
- Odds is the ratio of the probability of an event to probability of its complement
- **LOTP.** Lad hændelserne $A_1\dots A_n$ være en klassedeling af udkastrummet $S$, med $P(A_i)>0$. Da har vi at $$P(B) = \sum^n_{i=1} P(B\mid A_i)P(A_i)$$
  altså at sandsynligheden for en hændelse $B$ er summen af et produkt, der i det ene led indeholder sandsynlighederne for $B$ betinget af en af de disjunkte mængder, og i det andet led, sandsynligheden for den disjunkte mængde.
  
  Dette følger fra det andet aksiom om sandsynligheden for endelige foreninger af hændelser, samt at produktet er $P(A_i \cap B)$.

- En anden typisk form er $$P(A)=P(A\mid B)P(B) + P(A\mid B^c)P(B^c)$$ som resulterer fra den ovennævnte sætning (da $B,B^c$ selvfølgelig er en klassedeling).
- Alle sætninger som vedrører sandsynlighed $P(A)$ for en hændelse er også gældende for betinget sandsynlighed med erstatningen $P(A):=P(A\mid E)$ for en hændelse $E$, og selvfølgelig også aksiomerne.
- Det er derfor vigtigt at pointere at $A\mid E$ *ikke* er en hændelse, men notation for en sandsynlighedsfunktion $P:A\times E \to [0,1]$. 
- Dette giver anledning til at enhver sandsynlighed $P(A)$ på udkastrummet $S$ hvor $A\in S' \subset S$ kan være betinget af en $B\in S$. Mfan kan derfor forestille sig man altid arbejder på en slags $S'$.
- Ekstra betingelser for Bayes regel og LOTP er bare at lægge hændelsen $E$ på dem.2

- To hændelser $A$ og $B$ er uafhængige af hinanden såfremt at $$P(A\cap B) = P(A)P(B)$$Hvis begges sandsynligheder er over $0$, da er det ovenstående ækvivalent med $$P(A\mid B) = P(A),~~~P(B\mid A) =P(B)$$
- Hvis $A$ og $B$ er uafhængige så er $A,B,A^c, B^c$ alle uafhængige med hinanden.
- **Betinget uafhængighed.** Hændelserne $A$ og $B$ er betinget uafhængige givet $E$ hvis $P(A\cap B\mid E)=P(A\mid E)P(B\mid E)$. 

### Random variables
- Stokastisk variabel er en funktion $X:S\to \mathbb R$. 
- Antag et eksperiment hvor vi kaster en mønt to gange. Udkastrummet indeholder fire mulige udkast $$S=\{HH,HT,TH,TT\}$$
  Her kan vi associere nogle tilfældige variable. F.eks $X$ associerer hvert udkast med hvor mange $H$ der er i udkastet, så $X(HH)=2$. 
- $X$ er en diskret tilfældig variabel hvis der er en tællelig liste af værdier sådan at $P(X=a_j)=1$ for en eller anden $j$. Altså, sandsynligheden for at $X$ krystalliserer i en numerisk værdi i listen skal være $1$. Den mængde hvorpå at $P(X=x)>0$ kaldes for *støtten* (support) til $X$.
- PMF for en tilfældig variabel er funktion $p_x(x)=P(X=x)$. Den er positiv når $x$ er i støtten for $X$ og $0$ andetsteds.
- Når vi skriver $P(X=x)$ så dækker dette over sandsynligheden for hændelsen hvori at $X$ er tildelt $x$ ved udkastet $s$. Altså, hændelsen hvor $X$ afbilder elementerne til $x$.
- Afbilder vi $p_X(x)$ for $X:\text{antallet af H i udkastet}$ for udkastrummet $HH,HT,TH,TT$ får vi 
  1. $$p_X(0)=P(X=0)=\frac{1}{4}$$
  2.  $$p_X(1)=P(X=1)=\frac{1}{2}$$
  3.  $$p_X(2)=P(X=2)=\frac{1}{4}$$
- Definerer vi en variabel $Y$ som er "omvendt" $X$ i den tæller antallet af $T$, da harvi at $Y=2-X$. Da kan vi udlede at $$P(Y=y) = P(2-X=y) = P(X=2-y)=p_X(2-y)$$
- Læg mærke til at $p_X(x)=p_X(2-x)$, og altså $X$ og $Y$ har derfor den samme PMF også selvom $X$ og $Y$ er forskellige funktioner.
-  For f.eks en $X$ der afbilder det første terningekast i et udkast til et al, $P(X=j)=c=1/6$ for $j$ i domænet af $X$, og med $P(X\neq j)=0$, siger vi at $X$ udgør en Diskret Uniform distribution på domænet. 
- Distributionen for $X$ og en $Y$ der udvælger det andet terning2ekast, er derfor den samme, i og med at $(1,\cdot) \mapsto 1 \mapsto 1$ og $(\cdot ,1) \mapsto 1 \mapsto 1$ osv.
- Finder vi nu $P(T=j$), for $T=X+Y$, ser vi at f.eks $P(T=12)=1/6 \cdot 1/6 = 1/36$ lader os bruge den naive definition for sandsynlighed (og altså, $a+b=12$ har selvfølgelig $a=b=6$).
- Støtten for $T$ er selvfølgelig $t\in \{2,3,\dots,12\}$ og vi kan verificere dette med $$1=\sum_t P(T=t)$$
- Altså, en valid PMF har to kriterier. Den skal være positiv for $x_j$ i støtten, og $0$ andetsteds, og $1=\sum^\infty_{j=1} p(x_j)$.
- PMF er altså alt vi har brug for at bestemme en distribution.
- En tilfældig variabel siges at have en *Bernoulli distribution* med parameter $p$ hvis $P(X=1)=p$ og $P(X=0)=1-p$ hvor $0<p<1$. Dette skriver vi som $X \sim \mathrm{Bern}(p)$.
- Enhver hændelse $A$ har en naturlig Bernoulli distrubition, navnlig gennem $I \sim \mathrm{Bern}(p)$ hvor $I$ har at $P(I=a)=1$ for $a\in A$, og $P(I\not = a)=0$. Altså, $I$ tager udkast $a\in A$ til $1$ og udkast $b\in A^c$ til 0.
- Et *Bernoulli trial* er et eksperiment som enten har "success" eller "fejl" som resultat. Så en Bernoulli tilfældig variabel kan forstås som en indikator for success i et Bernoulli eksperiment. Netop af den grund forstår vi gerne parameteren $p$ som en sandsynlighed for *success*.
- Sæt at $n$ uafgængige Bernoulli forsøg udføres, alle med den samme sandsynlighed for success $p$. Lad $X$ være atallet af successer. Distributionen for $X$ kaldes den *binomiale distribution*, hvor $X \sim \mathrm{Bin}(n,p)$. 
- Diskrete distributioner defineres oftest ved brug af en PMF.
- Når $X\sim \mathrm{Bin}(n,p)$, så er PMF af $X$ beskrevet som $$P_X(k)=P(X=k)={n \choose k}p^k(1-p)^{n-k}$$ for $k=0\dots n$.
- Hvis $X\sim \mathrm{Bin}(n,p)$ og $q=1-p$ (altså fejlsandsynligheden) så er $n-X\sim \mathrm{Bin}(n,q)$
- Hvis $X\sim \mathrm{Bin}(n,p)$ med $p=1/2$ og $n$ lige, så er $p_X$ symmetrisk rundt om $n/2$ (husk at $p_X(k)=0$ for $k<0$)
- Hvis vi har en urne med $w$ hvide og $b$ sorte bolde, så det at vælge $n$ blde ud af urnen med repetitionergiver os en $\mathrm{Bin}(n,w/(w+b))$ distribution for antallet af hvide bolde opnået i $n$ forsøg. 
- Sæt nu vi har samme urne, men vi udtager $n$ bolde tilfældigt uden repetitioner, sådan at alle $w+b \choose n$ udfald er lige mulige. Lad nu $X$ være antallet af hvide bolde i et udfald. Så siges $X$ at have en hypergeometrisk distribution med parametrene $w,b,n$ og vi siger at $X\sim \mathrm{HGeom}(w,b,n)$.
- Beskrevet med PMF, så har vi $$P(X=k) = \frac{{w\choose k}{b \choose n-k}}{w+b\choose n}$$
- Dette følger bare fra den naive fortolkning af sandsynlighedsfunktionen.
- En skov har $N$ elge. I dag, så er $m$ af elgene tagged, og på en senere dato så er $n$ elge fanget igen. Vi antager at der er samme chance for at vælge en elg i første tilfælde som i andet tilfælde.
- Antallet af de tagged elge i andet tilfælde udgør en Hypergeometrisk sandsynlighedsfordeling $\mathrm{HGeom}(m,N-m,n)$. Altså, $m$ tagged elge, og $N-m$ ikke tagged elge. Derefter udvælger vi $n$ elge.
- Forskellen på HGeom og Bin er at, godt nok kan de begge forstås som en række Bernoulli forsøg, men forskellen er at de enkelte forsøg er uafhængige i Bin, men gensidiges afhængige i HGeom. Kendskabet til at én elg er tagged, mindsker sandsynligheden for en anden elg bliver tagged.
- Vi nævnte før fordelingen Discrete Uniform. Lad $C$ være et endeligt, ikke-tom mængde af ftal. Vælg ét af tallene uniformt og tilfældigt. Dette tal kaldes $X$. Så siges $X$ at have en Diskret Uniform fordeling med parameteren $C$ (som er antallet af elementer i mængden). Da siger vi $X\sim \mathrm{DUnif}(C)$.
- PMF af $X\sim \mathrm{DUnif}(C)$ har at $$P(X=x)=\frac{1}{|C|}$$
- Da en PMF summerer til $1$. Har vi dette tilfælde, så er $P(X\in A)=\frac{|A|}{|C|}$, og beskriver den naive definition for sandsynlighedsfunktionen.
- F.eks, der findes $100$ stykker papir i en hat, og hver af dem er nummeret $1$ til $100$. Vi vælger $5$ strips.
- Fordelingen for hvor mange af de udtagne strips er over $80$ udgør en Binomial fordeling. For det første, så er vores $X_j \sim \mathrm{Bern}(0.21)$ da vi har antaget lige fordelig *med* repetitioner (altså forsøgene er uafhængige af hinanden). Dette svarer til at vi lægger en strip tilbage igen efter vi har taget den.

### PDF
- En tilfældig variabel har en kontinuert distribution hvis dens CDF er differentiabel, ikke nødvendigvis randpunkter.
- En kontinuert tilfældig variabel har en kontinuert distribution.
- PDF er den afledede af en CDF.
- $$F(x) = \int_{-\infty}^x f(t)~dt$$
- hvor $f$ er PDF og $F$ cdf for den en kontinuert variabel $X$.
- Vi behøver ikke at bekymre os om randpunkter i et interval da de har sandsynlighed $0$.
- Altså $$P(a<X\leq b) = F(b)-F(a) = \int^b_a f(x)~dx$$
- Altså, for at finde en sandsynlighed i en hændelse $A$ så integreres PDF på det tilhørende interval altså $$P(X\in A) = \int_A f(x)~dx$$
- **En valid PDF $f$ af en kontinuert r.v. opfylder $f(x)\geq 0$ og skal være normaliseret.**
- Givet en kontinuert r.v. $X$ så er $$EX = \int_{-\infty}^\infty xf(x)~dx$$
- Kontinuert LOTUS har at $$E(g(X))=\int_{-\infty}^\infty g(x)f(x)~dx$$
- En Uniform Distribution har at PDF er $$f(x)=\frac{1}{b-a}$$ når $a<x<b$ og $0$ andetsteds. Dette skrives som $U\sim \mathrm{Unif}(a,b)$. 
- En UD har at sandsynligheden at en hændelse er proportionelt til intervallets længde.
- Den betingede sandsynlighedsfordeling for $U\sim \mathrm{Unif}(a,b)$ givet ved underintervallet $U\in (c,d)$ er simpelthen bare $\mathrm{Unif}(c,d)$.
- Eksempel på udledning af forventning og varians for UD.
- $E(U) = \int_a^b \frac{x}{b-a}~dx = \frac{a+b}{2}$
- For variansen kan vi bruge LOTUS til at finde $EU^2$, for derefter at finde $\mathrm{Var}(U)=EU^2 - (EU)^2$.
- 
