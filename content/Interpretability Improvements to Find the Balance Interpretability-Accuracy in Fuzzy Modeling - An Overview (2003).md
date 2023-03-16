Author(s): [[Jorge Casillas]], [[Oscar Cordon]], [[Francisco Herrera]], [[Luis Magdalena]]
Tags: #Fuzzy_Logic, #academic_papers
Read on: [[September 29th, 2020]]
URL: https://www.semanticscholar.org/paper/Interpretability-Improvements-to-Find-the-Balance-Casillas-Cord%C3%B3n/280b8c1a88cc682dae73699be87de2f53302a61e
# Main Contribution(s)
- Provides an overview of [[Linguistic [[Fuzzy Logic]]]] and [[Precise [[Fuzzy Logic]]]] before 2003
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FWizlMYxp5B.png?alt=media&token=0c37bb3a-3c19-4c35-b720-6833cb710e42)
Trade off between [[Interpretability]] and [[Accuracy]]
- [[Principle of Incompatibility]] by [[Lotfi Asker Zadeh]] - As the complexity of a system increases, our ability to make precise and yet significant statements about its behavior diminishes until a threshold is reached beyond which precision and significance (or relevance) become almost mutually exclusive characteristics
- [[Linguistic [[Fuzzy Logic]]]] or Rule-Based System, also known as Mamdani-type FRBS
- IF $$X_1 ... X_n$$ is $$A_1 ... A_n$$, 
THEN, $$Y_1 ... Y_m $$ is $$B_1 ... B_m$$
- Requires a rule base, and a data (knowledge) base
- Suffers from exponential growth in size when dealing with high dimensional data
- With more dimensions, every linguistic rule also lose part of its description ability since the understanding of the condition to activate the rule becomes more difficult.
- Two variable selection processes:
            1. Selecting input variables in the model - remove subset of input variables into the model
            2. Selecting input variables in the linguistic rules - remove subset of input variables into the linguistic rules.
- Two approaches to reduce input
            1. Selecting Linguistic rules
            2. Merging compatible linguistic rules
- [[Takagi-Sugeno-Kang-type Fuzzy Rule-Based Systems (TSK-type FRBSs)]]
- IF $$X_1 ... X_n$$ is $$A_1 ... A_n$$, 
THEN, $$Y_1 = p_1(X_1, ..., X_n)$$ and $$Y_m = p_m(X_1, ... , X_n)$$
where $$p_j(.)$$ is a polynomial function.
- Useful in [[Precise [[Fuzzy Logic]]]]
- Many consider [[Orthogonality|orthogonal]] transformations, such as
- [[Least Squares Solution for Inconsistent Equations]]
- [[Singular value decomposition and QR with column pivoting methods (SVD-QR)]]
- Many try to reduce the complexity by reducing the number of rules via checking for
            1. Redundancy - fuzzy sets representing compatible concepts
            2. Irrelevancy - when fuzzy sets with a membership degree close or equal to 1 (always used)
- A similarity measure is almost used to reduce the rule based system by:
            1. Merging/removing fuzzy sets
            2. Merging fuzzy rules
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F1ZQd6L3BKM.png?alt=media&token=4e35dab7-cf17-4ec8-b6b1-dbcc3fac2c0a)
To try to improve interpretability, the rules are either forced to 
            1. have a smoother consequent polynomial function
            2. develop an isolated fuzzy rule action - overlapping between adjacent input fuzzy sets is small
- [[Singleton Fuzzy Rule-Based Systems]]
- [[Fuzzy Rule-Based Classification System]]
- [[Approximate Rule-Based Systems]]
# Learning Gaps/Thoughts
# Simplify/Analogies
