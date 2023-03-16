Author(s): [[Timo I. Denk]], [[Ana Peleteiro Ramallo]]
Tags: #language_model, #BERT, #academic_papers
Read on: [[December 2nd 2020]]
URL: https://arxiv.org/abs/2010.15778
# Main Contribution(s)
- Conditions [[BERT]] using a global state using a context vector
# Summary
Typically [[BERT]] uses the [CLS] token which is assumed to aggregate global knowledge. However, this is not inductive; ie BERT structure does not explicit force this to happen. Yet, recent research has generally reinforced this notion.

Many authors try to introduce architectural changes to improve downstream NLP benchmarks.

The [[Transformer]] is a type of [[Graph Neural Networks]], and a global state is accessible from every transfer function and can be individually updated from layer to layer. This inspires the authors to introduce a global state for [[BERT]].

### Conditioning BERT with a Global State
4 methods
1. **Concat [C]**. Concatenate the context vector with every position in the input sequence.
2. **New Position [NP]**. Adds a new position to the input sequence at which the context is stored.
3. **Global State [GS]**. Treats the context as a read-only global state from which the internal representations can be updated.
4. **Global State with Update [GSU]**: Updates the global state using a transfer function.

### Experiments
Evaluates performances using a proprietary  real world industry problem.
# Learning Gaps/Thoughts
uses NLP motivations but uses proprietary non-NLP dataset?!
# Simplify/Analogies
Global state added to BERT, but results are not proven empirically.