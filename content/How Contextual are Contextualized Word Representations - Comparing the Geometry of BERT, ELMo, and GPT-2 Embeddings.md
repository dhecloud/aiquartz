Author(s): [[Kawin Ethayarajh]]
Tags: #academic_papers, #critique, #BERT, #transformer, #Embeddings 
Read on: [[October 11th, 2019]]
URL: https://arxiv.org/abs/1909.00512
# Main Contribution(s)
# Summary
Analyses contextual word embeddings behind language models like [[BERT]] and [[GPT-2]]. Experiments on how [[Isotropy|Isotrophic]] [[BERT]]/[[GPT-2]]/ [[ELMo]] [[Embeddings]] are. Compares between [[ELMo]] (static) and [[BERT]]/[[GPT-2]] (contextualized) [[Embeddings]] and their advantages. Context specificity is always accompanied by increased [[Anisotropy]]. In best case scenarios, static words embeddings would be a poor replacement for contextualized ones.

3 contextual word representations are defined.
1. **Self Similarity**
 SelfSim(w) = 1 if layer does not contextualise the representation. The more contextualised the representations are for w, the lower we would expect SelfSim() to be

2. **Intra sentence similarity** 
Similarity between word representations and the sentence vector (mean of the words vectors). 
Low SelfSim and low IntraSim means that words are contextualised and are still different from all other word representation.
Low SelfSim and high IntraSim suggests a less nuanced contextualization simply from making representation converge in vector space

3. **Maximum explainable variance**
Proportion of variance in representation that can be explained by their first principal component. The higher MEW is (close to 1), the better static embeddings are as a replacement. 
Findings

4. Contextualised representations are [[Anisotropy|anisotrophic]] in all input layers
5. Contextualised representations are generally more [[Anisotropy|anisotrophic]] in higher layers
6. Contextualised word representations are more context-specific in higher layers
7. Stopwords have among the most context-specific representations (lowest self-similarity)
8. Context-specificity manifest very differently in [[ELMo]], [[BERT]], [[GPT-2]]
9. In [[Elmo]], words in the same sentence are more similar to one another in upper layers ( IntraSim rises). Gives evidence to the hypothesis that because words in the same sentence share the same context, their contextualised representations should also be similar.

10. In [[BERT]], words in the same sentence are more dissimilar to one another in upper layers (decreasing IntraSim across layers)
11. In [[GPT-2]], word representations in the same sentence are no more similar to each other than randomly sampled words ( IntraSim is close to 0). i.e. in every layer word representations of words in the same sentences are different from one another.

12. On average, less than 5% of the variance in a word’s contextualized representations can be explained by a static embedding.
13. Principal components of contextualized representations in lower layers outperform [[GloVe]] and [[FastText]] on many benchmarks. ([[BERT]]/[[GPT-2]] embeddings are almost always better)

Quite an insightful paper.

# Learning Gaps/Thoughts
# Simplify/Analogies