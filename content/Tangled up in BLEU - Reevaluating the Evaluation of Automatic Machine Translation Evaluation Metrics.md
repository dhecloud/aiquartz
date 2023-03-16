Author(s): [[Nitika Mathur]], [[Timothy Baldwin]], [[Trevor Cohn]]
Tags: #critique, #Evaluation_Metric, #academic_papers
Read on: [[June 17th, 2020]]
URL: http://arxiv.org/abs/2006.06264
# Main Contribution(s)
- Show that current methods for judging metrics are highly sensitive to the translations used for assessments, particularly the presence of outliers
- Propose a `pair-wise system ranking` which allows quantification of [[Type I Errors]] and [[Type II Errors]]
# Summary
- [[WMT]] has a method using [[Pearson's Correlation Coefficient]] for measuring how well automatic metrics match with human judgments of translation quality.
- This correlation is computed using many translation systems; and achieves a high correlation as high as 0.9
- ==However when considering the first 4 best system, the automatic metrics were shown to exhibit negative correlations in some instances==
- Can lead to false confidence in the utility of a metric
#  Metrics
# # Baseline
- [[BLEU]] - High variance across different hyper-parameters and pre-processing strategies, for which [[sacreBLEU]] has introduced to combat this weakness
- [[TER]] - Number of edits required to transform output to reference
- [[chrF]] - Character [[N-grams]] instead of word [[N-grams]] for comparison. Targeted at ==matching morphological variants of words==
# # Best metrics across language pairs
- [[YiSi-1]] - Computes semantic similarity of phrases in the MT output using contextual word embeddings from [[BERT]]
- [[ESIM]] - A trained Neural Model that first computes sentence representations from BERT embeddings, then computes the similarity between the two strings
# # Source-based metric
- [[YiSi-2]] - Same as [[YiSi-1]], but using cross-lingual embeddings
# # Are metrics unreliable when evaluating high-quality MT systems?
- Correlations between metric and human scores decreases when only computing for the top 4 systems
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FRQTtaihtox.png?alt=media&token=8c43d8a4-e9a1-4ec5-8772-47deb56f4d7f)
- ==Using a rolling window of system, there is no consistent trend in the correlation that depends on the quality of the systems in the sample==
#  How do outliers affect the correlation of MT metrics?
- [[Pearson's Correlation Coefficient]] is particularly sensitive to outliers
- Outliers present the illusion of high correlation when the metric scores are actually independent of the human scores without the outlier
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FlC3hewovmX.png?alt=media&token=3ed08a88-dff7-4a4f-818e-68e8fc1bf0cb)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FFS7kED5iPB.png?alt=media&token=80dac7d9-06f8-4566-ae3e-7750e838e5d6)
#  Beyond Correlation
- Authors suggest that BLEUs which are significant but with deltas in the range of 0-3 should be judged to be insignificantly different in quality
- For higher BLEU deltas of 3-5, even about a quarter of system pairs are of similar quality
- This reflects badly on [[BLEU]] as a tool for determining quality of systems
#  Suggestions
- Stop using [[BLEU]] or [[TER]], but use [[chrF]], [[YiSi-1]] or [[ESIM]]
# Learning Gaps
- Most of the other mentioned metrics.
# Simplify/Analogies
- BLEU was useful for awhile when systems lacked the basic syntactic generation and understanding, but it is less useful now when systems are able to generate perfect sentences 
