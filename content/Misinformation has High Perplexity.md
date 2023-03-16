Author(s): [[Nayeon Lee]], [[Yejin Bang]], [[Andrea Madotto]], [[Pascale Fung]]
Tags: #critique, #Evaluation_Metric, #Covid19, #datasets, #academic_papers
Read on: [[June 16th, 2020]]
URL: http://arxiv.org/abs/2006.04666
Code: https://github.com/HLTCHKUST/covid19-misinfo-data
# Main Contribution(s)
- ==Postulate that misinformation itself has high perplexity compared to truthful statements==
- Construct and release two know COVID-19 pandemic-related debunking test sets, namely [[Covid19-scientific]] and [[Covid19-politifact]]
# ELI5
- Misinformation has higher perplexity magnitude, can be used for detection
# Summary
- Misinformation is a piece of text that contains false information regarding its subject, resulting in a rare co-occurrence of the subject and its neighboring words in a truthful corpus
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FzhWdENDQr9.png?alt=media&token=31ce82c6-a0fe-4f20-86e4-2f6f06ed0851)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FKCDugB7nlh.png?alt=media&token=8a81115d-ac79-43ad-b878-e72185b41654)
#  Evidence Selection
- Using [[TF-IDF]], select tuples of evidence along with their relevancy scores
- Discard evidence if from questionable source (meme, socials) or if it is reciprocal
#  Grounding LM with Evidence
- Train LM using these curated evidence
#  Debunking with Perplexity
- Assign a perplexity threshold. Any higher score will be classified as False, and lower as True 
#  New [[Covid19]] datasets
- [[Covid19-scientific]]
- [[Covid19-politifact]]
#  Experiments
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FbQZQJIxyv2.png?alt=media&token=a722bfb5-d895-41fd-8671-60e4a6151086)
- Fever-HexaF refers to the winning system trained on the [[FEVER]] dataset
- LIAR-suffixed models refer to [[BERT]]-models finetuned on the [[LIAR-Politifact]] dataset
- The LM Debunker (this paper) is [[GPT-2]] fine-tuned on the [[Covid19]] datasets
#  Limitations
- Perplexity is highly influenced by syntax and grammar, regardless of content and meaning
- Perplexity does not work well with negation
# Learning Gaps
- I don't really agree with using perplexity as a new measure; it is a shallow metric with no inherent meaning whatsoever. This is further proven by the fact that syntactic errors increase perplexity.
# Simplify/Analogies
- I guess the focus of this paper was on covid19, so the main takeaway of this paper is the 2 new datasets
