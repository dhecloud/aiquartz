Author(s): [[Ziyang Luo]]
Tags: #BERT, #academic_papers
Read on: [[November 26th, 2020]]
URL: https://arxiv.org/abs/2011.04393
# Main Contribution(s)
- Inspects the vector space of [[BERT]] and [[RoBERTa]] and finds some interesting quirks that the author terms to be tails.
# Summary
- For [[BERT]], the 557th element is always the smallest element in all words in all non-input layers. For [[RoBERTa]], the 588th element is always the largest in all
vectors and the 77th element is always the smallest except the [CLS] token. We call them as ”tails” of models
- This is done by sampling 1000 random words from random sentences in [[SST-2]]
- [[Anisotropy]], related to [[geometry]] of vector spaces, meaning that the average [[cosine similarity]] between uniformly randomly sampled words are close to 1.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fo6UGhHhvGw.png?alt=media&token=70117b65-5576-4b4f-8e7e-367419209932)
Tails are cut by setting the minimum elements to 0
- Uses the [[self-similarity]] measure and set a threshold to predict the on the binary classification dataset [[WiC]]. Accuracy increases by 1%. Not sure if statistically significant 
# Learning Gaps/Thoughts
- Not sure why he did not set max element to high value
- Accuracy increases by 1%. Not sure if statistically significant 
- Interesting paper, but requires more in-depth studies; especially for bigger models with higher dimensionality. More dimensions -> more tails?  
# Simplify/Analogies
-
