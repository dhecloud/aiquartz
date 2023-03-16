Author(s): [[Marzieh Fadaee]], [[Christof Monz]]
Tags: #critique, #Neural_Machine_Translation, #academic_papers
Read on: [[May 27th, 2020]]
URL: https://arxiv.org/abs/2005.12398
# Main Contribution(s)
- Checks for volatility of NMT models including RNN
- Provides ways of noisy text generation
# ELI5
- You should be able to understand the same sentence even with a few grammar mistakes. However, some models can't
# Summary
- There are 4 rules to slightly modify source and target sentences:
- DEL - Remove pairs containing 50 most frequent adverbs
- SUBNUM - Substitute number with another number
- INSERT - Insert words with high probabilities using naive bayes
- SUBGEN - Change gender of person
- [[WMT17 En-De]] training data, on RNN and Transformers
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F156RKpKrZP.png?alt=media&token=bdbb3764-ed91-4396-9fd8-da0d1fda9f5e)
- They evaluate sentence variations with the [[Levenshtein Distance]] (edit distance) and the span of change (length of sequence). If both metrics are > 10, it is considered a major change, otherwise minor.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FQeGzBegR4L.png?alt=media&token=96a91d6b-2d7f-454e-a37a-052183beb6e4)
- Generally, both the RNN and the transformer has a significant number of sentence variation (26% and 19%). However, the transformer has slightly fewer sentences variations in the major category.
# Learning Gaps
- None
# Simplify/Analogies
- Currently the models can be likened to a child. It is easy for the child to regurgitate information, but once the question is slightly changed, the child will not be able to answer properly.
