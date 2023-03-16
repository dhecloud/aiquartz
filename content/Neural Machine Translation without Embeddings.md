Author(s): [[Uri Shaham]], [[Omer Levy]]
Tags: #Neural_Machine_Translation, #Embeddings, #academic_papers
Read on: [[September 19th, 2020]]
URL: https://arxiv.org/abs/2008.09396
# Main Contribution(s)
   - Represents sequences as bytes and remove the embedding component
# Summary
   - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FikUU9S-ArH.png?alt=media&token=b0360e8c-432e-4fb4-98c1-d480d7d14ecd) 
- Represents text as a sequence of bytes based on UTF-8 encoding 
- Remove the input and output trainable token embedding layers
- Remove the dropout layers in the encoder input and decoder output as one-hot vectors works similarly to dropout by deleting significant pants of the model's distribution.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FvQx4jV6Vkd.png?alt=media&token=daed29c7-15e5-4a0b-a327-fa262ea2f4a7)
- Results on [[IWSLT]] datasets
	- Models without embeddings consistently achieve higher [[BLEU]] scores in 19/20 cases
    - Hypothesize that bytes are [[Orthogonality|orthogonal]] and do not have semantic similarity with each other (compared to subwords and characters), hence removing the embedding matrix improves the performance.
    - They tried forcing [[Orthogonality]] by freezing the randomly initialized embedding matrix for a subword model, but it still led to a degradation of [[BLEU]]
# Learning Gaps/Thoughts
- It is a little unclear what is the difference between character representation and bytes representation, though it seems like they want to enforce dissimilarity between each individual representation, hence they use bytes.
- Wonder if this would help alleviate the [[Multi-Modality]] problem in [[Non-Autoregressive]] models.
# Simplify/Analogies
-
