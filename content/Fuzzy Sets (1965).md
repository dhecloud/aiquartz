Author(s): [[Lotfi Asker Zadeh]]
Tags: #Fuzzy_Logic, #academic_papers
Read on: [[September 29th, 2020]]
URL: https://www.sciencedirect.com/science/article/pii/S001999586590241X 
# Main Contribution(s)
- Original paper that proposes [[Fuzzy Logic]] and formulates them
# Summary
- A [[Fuzzy Set]] $$A$$ in $$X$$ is characterized by a membership (characteristic) function which associates with each point in $$X$$ a real number in the interval [0,1], with the value of $$f_a(x)$$ at $$x$$ representing the grade of membership of $$x$$ in $$A$$
- Definitions
- Complement $$f_{A^\prime} = 1 - f_A$$
- Containment $$A \subset B \iff f_a \leq f_b $$ 
- Union $$f_c(x) = Max [f_a(x), f_b(x)]$$
- Intersection $$f_c(x) = Min [f_a(x), f_b(x)]$$
- Convexity - A fuzzy set $$A$$ is convex if and only if the sets $$\Gamma _\alpha$$ defined by $$\Gamma _\alpha = \{x | f_A(x) \geq \alpha\}$$ are convex for all $$\alpha$$ in the interval (0,1)
- Boundedness. A fuzzy set $$A$$ is bounded if and only if the sets $$\Gamma _\alpha$$ defined by $$\Gamma _\alpha = \{x | f_A(x) \geq \alpha\}$$ are bounded for all $$\alpha > 0$$
- Strict and strong convexity. A fuzzy set $$A$$ is strictly convex if the sets $$\Gamma, 0 < \alpha \leq 1$$ are strictly convex (the midpoint of two distinct points in $$\Gamma_\alpha$$ lies in the interior of $$\Gamma_\alpha$$)
- Shadow. The shadow of $$A$$ on a hyperplane $$H$$ is given by $$f_{S_H(A)}(x) = f_{S_H(A)}(x)(x_2, ... , x_n) = Sup_{x_1}f_A(x_1, ..., x_n)$$
- Properties
- [[De Morgan's Law]] - $$(A \cup B)^\prime = A^{\prime} \cap B^\prime$$
- [[Distributive Law]] - $$C \cap (A \cup B) = (C \cap A) \cup (C \cap B)$$
- Algebraic operations
- Algebraic Product $$f_{AB} = f_Af_B$$ or $$AB \subset A \cup B$$
- Algebraic sum $$f_{A+B} = f_A + f_B$$
- Absolute difference $$f_{|A-B|} = |f_A - F_b|$$
- Convex combination - a convex combination of two vectors $$f, g$$ usually means a linear combination of $$f, g$$ of the form $$\lambda f + (1 - \lambda)g$$ in which $$0 \leq \lambda \leq 1$$. In fuzzy terms:
- $$(A, B, \mathbb{A}) = \mathbb{A}A + \mathbb{A}^\prime B$$
- Fuzzy relation - a relation is a generalization of a function. We can define an n-ary fuzzy relation in $$X$$ as a fuzzy set A in the product space
- $$f_{B \circ A}(x,y) = Sup_v Min [f_A(x,v), f_B(v,y)]$$
- Fuzzy sets induced by mappings. let $$T$$ be a mapping from $$X$$ to space $$Y$$. Let $$B$$ be a fuzzy set in $$Y$$ with membership function $$f_B(y)$$. The inverse mapping $$T^{-1}$$ induces a fuzzy set $$A$$ in X whose membership function is defined by $$f_A(x) = f_B(y)$$ If the mapping is not one to one, there will be points mapped to multiple membership grade. Hence agree to assign the larger of the two membership grades
-  Theorem
- if $$A$$ and $$B$$ are convex, so is their intersection
- If A is a convex fuzzy set, then its core is a convex set
- Let $$A$$ and $$B$$ be bounded convex fuzzy sets in $$E^n$$, with maximal grades $$M_A$$ and $$M_B$$. Let $$M$$ be the maximal grade for the intersection $$A \cup B$$. Then, $$D = 1 - M$$ where $$D$$ is the degree of separation 
# Learning Gaps/Thoughts
# Simplify/Analogies
