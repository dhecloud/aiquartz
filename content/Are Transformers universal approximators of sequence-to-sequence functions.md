Author(s): [[Chulhee Yun]], [[Srinadh Bhojanapalli]], [[Ankit Singh Rawat]], [[Sashank J. Reddi]], [[Sanjiv Kumar]]
Tags: #critique, #transformer, #BERT, #academic_papers
Read on: [[May 28th, 2020]]
URL: https://arxiv.org/abs/1912.10077
# Main Contribution(s)
- Show that self-attention layers can compute contextual mappings of input sequences
# ELI5
- Neural networks are said to be universal function approximators. This paper checks if it is the same for [[Transformer]]s
# Summary
- ### Findings
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FkPEhjKLLhP.png?alt=media&token=43ca3636-d3b5-4352-843b-0f2455ef8501)
- A [[Transformer]] block is permutation equivariant
- [[Transformer]] functions become richer as we increase the number of heads, head size and hidden nodes.
- None of the parameters depend on input sequence length or embedding dimension
- A modified [[Transformer]] network can implement a quantization map with a composition of multiple feed-forward layers
- ie Different layers do mean different things
- Token-wise application of a composition of feed-forward layers can map these tokens to the desired outputs required.
- Models with 1 or 2 convolution layers and rest the self attention layers, perform better than models with only the self attention layers.
- Possible reason for this is first few layers attend broadly to the whole sequence, and convolution layers can perform**** this job more efficiently.
- It is also interesting to note that in addition to computing contextual mappings, [[Transformer]] also map a word into semantic clusters
# Learning Gaps
- Pretty much of the maths and proofs just went over my head. I just read the findings
# Simplify/Analogies
- [[Transformer]]s indeed are universal function approximators !
