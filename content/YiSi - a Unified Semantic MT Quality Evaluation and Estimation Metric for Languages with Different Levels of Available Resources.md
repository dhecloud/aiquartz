Author(s): [[Chi-kiu Lo]]
Tags: #Evaluation_Metric, #BERT, #academic_papers
Read on: [[June 18th, 2020]]
URL: https://www.aclweb.org/anthology/W19-5358
# Main Contribution(s)
- Propose a new automatic metric for [[Neural Machine Translation]]
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FPP9laHHQSX.png?alt=media&token=4fadb19e-a95f-4647-b7fb-0491f8772e2f)
- Propose 3 metrics: [[YiSi-0]], [[YiSi-1]], [[YiSi-2]]
- YiSi is the romanization of 意思
- Procedure:
- Apply a shallow semantic parser to both `E` and `F`
- Apply the maximum weighted bipartite matching algorithm to align the semantic frames between `E` and `F`
- For each pair of aligned frame, apply the maximum weighted bipartite matching algorithm to align the arguments between `E` and `F` according to the lexical similarity of role fillers
- Compute the weighted f-score over the matching role labels of these aligned predicates and role fillers using the lexical weight of `E` and the lexical similarity of `E` and `F`
#  [[YiSi-0]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FxSSWLZAHCQ.png?alt=media&token=86a69040-2915-49a6-b272-5f5dc418d130)
- Metric for extremely low resource languages
- Uses the longest common character sub-string accuracy to evaluate lexical similarity 
#  [[YiSi-1]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FOHJNeUV8MJ.png?alt=media&token=9d3ad1a4-a331-41f1-bbf2-0938e5bbd35b)
- Requires an embedding model
- The lexical semantic similarity is the cosine similarity of the embedding from the lexical representation model
#  [[YiSi-2]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FNlf1QW23mz.png?alt=media&token=729d9fba-94f6-4cdb-8a05-90963035211e)
- Requires a cross-lingual embedding model
- Otherwise similar to [[YiSi-1]]
#  [[BERT]] as lexical unit semantic similarity
- [[GloVe]] and [[word2vec]] are static embeddings and hence provide the same embedding representation for the same word without reflecting context of different sentences.
- The output from the 18th/9th layer of the large/small models are used 
- [[MATE]] is used for structural semantic similarity.
#  Correlation with human judgement 
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fo0KtrSGglJ.png?alt=media&token=a83aec95-70d7-4150-813a-2333eadefb45)
- Honestly i am not familiar with [[chrF]] which is the main metric for comparison, so i can't infer much 
# Learning Gaps
- I am not understanding the process of calculating YiSi to be honest
- chrF
# Simplify/Analogies
- Using BERT along with some other rule based system allows for better evaluation.
