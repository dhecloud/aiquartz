Author(s): [[Manzil Zaheer]], [[Guru Guruganesh]], [[Avinava Dubey]], [[Joshua Ainslie]], [[Chris Alberti]], [[Santiago Ontanon]], [[Philip Pham]], [[Anirudh Ravula]], [[Qifan Wang]], [[Li Yang]], [[Amr Ahmed]]
Tags: #transformer, #BERT, #academic_papers, #google
Read on: [[August 11th, 2020]]
URL: https://arxiv.org/abs/2007.14062
# Main Contribution(s)
- Proposes the [[BigBird]] with a sparse attention mechanism, named the [[generalized attention mechanism]], that reduces this quadratic dependency to linear
- Shows some theoretical analysis that reveals the benefits of $$O(1)$$ global tokens like CLS
- Drastically improves performance on various NLP tasks such as QA and summarization, and also propose novel applications to genomics data
# Summary
 Advantages of [[Transformer]]
- Introduction of [[self-attention]], which can be computed in parallel, thus eliminating the sequential dependency in recurrent neural networks.
- In turn allows capability to use modern SIMD hardware accelerators like GPUs
- Weakness of [[Transformer]]
- Computational and memory requirement that is quadratic of the sequence length
- [[self-attention]] is permutation invariant, but apparently expressive enough to capture continuous sequence to sequence functions.
- Questions:
- Is it possible to achieve the benefits of a fully quadratic self-attention scheme using fewer inner products?
- Do these sparse attention mechanisms preserve the expressivity and flexibility of the original network?  
- [[generalized attention mechanism]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FMCoY5WUpfW.png?alt=media&token=abefe951-0682-4ea3-83d1-db5abbfd2613)
 A directed graph $$D$$ whose vertex set is $$[n] = \{1,...,n\}$$
- if $$D$$ is the complete digraph, then it reverts to the full quadratic attention mechanism of the original transformers
- Framing it in this way changes the problem of reducing quadratic complexity in self attention into a **graph sparsification problem**
- In a simple random graph [[Erdős-Rényi model]], the shortest path between any two nodes is $$log(n)$$
- As a result, such a random graph approximates the complete [[Spectral Graph]] and its second eigenvalue is quite far from the first eigenvalue
- [[Small World Graphs]] are also another class of random graphs exhibit high [[clustering coefficient]]
- Is a universal appropriator of sequence to sequence function, as proven in the paper.
- A sparse encoder and a sparse decoder can be used to simulate any Turing Machine, as proven in the paper
- [[Orthogonal Vector Conjecture]] states that one cannot determine if the minimum inner product among $$n$$ boolean vectors is 0 in subquadratic time.
- Show using OVC that a transformer with any sparse directed graph can evaluate Task 1 (finding the vectors that are furthest apart)
- However it cannot universally replace dense attention, as the full attention mechanism can solve some problems (see appendix) in $$O(1)$$ layer,  but sparse attention needs a minimum number of layers
	 -   There is a significant amount of locality of reference in most contexts within NLP and computational biology
  -   Two types of global tokens
- Internal **[BigBird-ITC]**: Make some existing tokens global, which attend over the entire sequence.
- Extended [**BigBird-ETC**]: Using additional tokens like CLS.
- Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FdtTCgtDpAh.png?alt=media&token=bf4b4ae4-2ab3-4371-8b55-66e9fad177d9) ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FmFretkGDZ0.png?alt=media&token=a68bc318-eccc-4969-a036-ed90db00ae51)
	 - Encoder only
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F87km6YaFeX.png?alt=media&token=bad155fd-f039-4542-b41e-a0a6380b8e93) ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FZON3zFry95.png?alt=media&token=a336b7f6-405b-4c77-a1b9-953afc21d6ea) Encoder-Decoder. However only sparse attention is used in the encoder
- Some other Genomics experiments
# Learning Gaps/Thoughts
- Proofs for theorems in the paper
- Genomics experiments
- No mention of other tasks like commonsense reasoning or the GLUE benchmark, assume to not perform as well
# Simplify/Analogies
- By combining random attention, global attention, window attention to form the generalized attention mechanism, performance can scale well to longer sequences
