Author(s): [[Nguyen Cat Ho]], [[Wolfgang Wechler]]
Tags: #Fuzzy_Logic, #Linguistic_Variable, #academic_papers
Read on: [[September 24th, 2020]]
URL: https://www.sciencedirect.com/science/article/abs/pii/016501149090002N
# Main Contribution(s)
- Show that any sets of linguistic values of linguistic variables can be axiomatized, which leads to a notion of hedge algebras. 
# Summary
- [[Linguistic Hedges]] are adjective/adverbs used to signal caution as a probability instead of full certainty. For example, insignificant, somewhat, isn't it?.
- Denoted by $$X = (X, H, \leq)$$ where X is the underlying set, H is a set of hedges, and $$\leq$$ is a partial ordering on X
- **Hypothesis 1**: Every hedge under consideration either strengthens or weakens the positive or negative meaning of the primary vague concepts.
- **Hypothesis 2**: Every hedge either strengthens or weakens the meanings of any
other hedges.
- the hedges Very, More strengthen the meanings of the hedges Very, More,
Less and Not, and they weaken the meaning of the hedge Approximately
- The hedges Less, Approximately and Not strengthen the meaning of the
hedge Approximately and weaken the meanings of the hedges Very, More, Less
and Not
- **Hypothesis 3**: All hedges under consideration have a local and separated
meaning and the meaning of a term generated from a vague concept x stems from
the meaning of the concept x.
- Assume that every hedge operation is an ordering operation 
- **Definition 1**: 
(i) Let $$h$$, $$k$$ be two hedges in $$H$$. Then $$k$$ is said to be positive (negative) w.r.t $$h$$ if for every $$x \in X$$, $$hx \geq x$$ implies $$khx \geq hx$$ ($$khx \leq hx$$) or, conversely, $$hx \geq x$$ implies $$khx \geq hx$$  ($$khx \leq hx$$).
(ii) Let $$\sigma$$ and $$\sigma^{\prime}$$ be two strings of hedges in $$H$$. Then, $$\sigma \geq \sigma^{\prime}$$ if for every $$x \in X$$, $$x \geq \sigma x$$ or $$x \geq \sigma^\prime x$$ implies $$x \leq \sigma x \leq \sigma^\prime x$$ and $$x \geq \sigma x$$ or $$x \geq \sigma^\prime x$$ implies $$x \geq \sigma x \geq \sigma^\prime x$$
(iii) Two hedges $$h$$ and $$k$$ are said to be converse or we say one is a converse operation of the other, provided for every $$x \in X$$, $$hx \leq x$$ iff $$kx \geq x$$. Further, $$h$$ and $$k$$ are said to be compatible provided for every $$x \in X, x \leq hx$$ iff $$x \leq kx$$.
- Every $$H$$ is assumed to be able to be decomposed into two non-empty disjoint sets $$H^+$$ and $$H^-$$ so that each element is a converse operation of the operations in $$H^-$$
- **Definition 2**: For any hedge operation $$h$$ and $$k$$, we shall write $$h < \leq kx (hx < \leq Ix)$$, if for any $$h^\prime$$ and $$k^\prime$$ in the set of unit operations in H (UOS) and any $$n, m$$ in Nat , $$V^nh^\prime hx \leq V^mk^\prime kx (V^nh^\prime hx \leq Ix)$$. If the latter inequalities are always strict, then we shall write $$hx << kx (hx << Ix)$$ where $$I$$ is an artifical linguistic hedge having no meaning and no another hedge can be applied to $$I$$, except itself. $$V, L$$ are the greatest elements in $$H^+, H^-$$, called the unit operation
- **Definition 3**: An algebraic structure $$X = (X, H, \leq)$$ is said to be a hedge algebra if it satisfies the following axioms:
(A1) Every operation in $$H^+$$ is a converse operation of the operations in $$H^-$$
(A2) The unit operation $$V$$ in $$H^+$$ is either positive or negative with respect to any hedge operation. 
(A3) If $$u$$ and $$v$$ are independent, i.e. $$u \notin H(v)$$ and $$v \notin H(u)$$, then $$x \notin H(v)$$, for every $$x \in H(u)$$. In addition, if $$u$$ and $$v$$ are incomparable, then so are $$x$$ and $$y$$, for any $$x$$ in $$H(u)$$ and $$y$$ in $$H(v)$$
(A4) If $$x \neq hx$$, then $$x /notin H(hx)$$, if $$h \neq k$$ and $$hx \leq kx$$, then $$h^\prime hx \leq k^\prime kx$$, for any $$h^\prime$$ and $$k^\prime$$ in UOS. Moreover, if $$hx \neq kx$$, then $$hx$$ and $$kx$$ are independent.
(A5) If $$u \notin H(v)$$ and $$u \leq v (u \geq v)$$, then $$u \leq hv (u \geq hv)$$, for each $$h \in $$ UOS
- (A3) means, that if two vague concepts are really different (independent), then
their two concept categories are separated, i.e. they have no common meanings.
(A4) means that each hedge has its meaning and hence it determines its own
concept category. So, for example, if hx is different from kx, then two categories
of these vague concepts are separated.
(A5) describes the fact that h modifies only the meaning of a vague concept. It
means that the meaning of hv stems from the concept o. Therefore, if the relative meanings of the concepts u and v are represented by an ordering relationship,
then the hedge h preserves this meaning. The fact that u does not belong to H(v)
means that the meaning of u is really different from the meaning of v.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F86eEJ8zsaw.png?alt=media&token=afeb053e-f905-4ba1-8a08-af8f1559e118)
- **Definition 4**: Let $$x$$ and $$u$$ be two elements in a hedge algebra $$X = (X, H, \leq)$$. The expression $$h_n ... h_1u$$ is said to be a canonical represntation of $$x$$ w.r.t $$u$$ in $$X$$ if (i) $$X = h_n ... h_1u $$; (ii) $$h_n ... h_1u \neq h_{n-1} ... h_1u$$ for every $$i \leq n$$
- **Definition 5**: Let $$X = (X, H, \leq)$$ be a hedge algebra. An element $$a \in X$$ is said to be a primary generator of $$X$$ if $$a \notin H(b)$$, for every $$b \in X$$ and $$a \neq b$$. A primary generator $$a$$ is said to be positive (negative) if $$Va > a (Va < a)$$. If G is the set of all generators of $$X$$ and $$H(G) = X$$, then $$X$$ is called a primarily generated hedge algebra
# Learning Gaps/Thoughts
# Simplify/Analogies
