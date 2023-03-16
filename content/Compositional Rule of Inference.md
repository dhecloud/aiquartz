---
---
- Proposed by [[Lotfi Asker Zadeh]] in [[The Concept of a Linguistic Variable and its Application to Approximate Reasoning]], extended to many schemes. 
- For a relational assignment equation $$R(u) = A$$, and $$R(u,v) = F$$, can be solved by $$R(v) = A \circ F$$ where $$\circ$$ is the operation of composition
- Example:
$$R(u) \approx small$$ and $$R(u,v) = \textit{approximately equal}$$
Hence
$$R(v) = \textit{small} \circ \textit{approximately equal} = \textit {more or less small}$$
![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FTvcO1HJYgG.png?alt=media&token=7dc99d42-621d-4ac2-8380-4e046651535e)
- The basic rule of inference is the [[Modus Ponens]], where we can infer the truth of a proposition $$A \Rightarrow B$$
- In human reasoning this is approximate rather than exact. ie $$A \text{ is true and that }  A^*\Rightarrow B$$. Then from $$A \text{ and } A^* \Rightarrow B$$, we may infer that $$B$$ is approximately true
- The [[Modus Ponens]] can be viewed as a special case of the [[Compositional Rule of Inference]], and this is termed a [[Generalized [[Modus Ponens]]]]. 
- $$R(u) = A_1$$
$$R(u,v) = A_2 \Rightarrow B$$
$$R(v) = A_1 \circ (A_2 \Rightarrow B)$$
![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FQ5jEZTN-al.png?alt=media&token=1833b8ea-089c-4cae-9d77-5d3162e067fc)
