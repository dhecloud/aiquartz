Author(s):
Tags: #critique, #survey, #Conversational_Dialogue_Systems, #Evaluation_Metric, #academic_papers
Read on: [[June 22nd, 2020]]
URL: http://arxiv.org/abs/2006.06110
# Main Contribution(s)
- Survey 20 evaluation protocols from the last 20 years
# Summary
- Evaluation metrics need to be a close approximation of human judgements, but unfortunately often correlate weakly with human judgements.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fo6yeRvFJdO.png?alt=media&token=187526f0-9257-4cd4-91a2-0943881511a5)
- 20 papers since 2018 primarily from top-tier venues have been compiled and 3 main categories of evaluation protocols decided: 
- ==automated== - straightforward, undemanding, but poor indicators of true dialogue quality
- ==static== - Most common, humans assess system responses from dialog in a corpus, but never actually interacts freely with the dialogue system
- ==interactive== - Plays the role of both user and evaluator; ie can have a free conversation with the dialogue system
#  Automated Evaluation
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FTFtjJqWE8A.png?alt=media&token=ad0ce7e3-c0c7-4b0c-a513-8701d14da3db)
- Try to quantify the capabilities of models using mathematical formulations
- [[BLEU]], C, Coherence, Distinct, Embedding, Entity A/R, Entropy, Inertia, Perplexity, [[ROUGE]]
- These metrics further fall into 5 categories: ==Ground Truth Response Similarity==, ==Context Coherence==, ==Response Diversity==m ==Language Model Fitness==, ==Application-Specific==
#  Human Evaluation
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FRR4L5DnE6v.png?alt=media&token=9d015218-ec9d-4d7e-bf4c-b2deb7d30c81)
- High variability, 21 unique dimensions found with questionable and similar overlaps
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FA3OCYEG4Iw.png?alt=media&token=c6da03b2-abf0-4087-8f2b-7e8312bc0f3c)
- The authors suggest collapsing them into 8 dimensions
#  Alexa Prize 2020 Case Study
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fydfd_CXUJc.png?alt=media&token=bd6cf9c9-1ab9-4569-8a11-35200c28e945)
- Conversations are rated in terms of Overall Quality from 1-5 using interactive evaluation protocol
- A expert manually rated each dialogue dimension as a **preliminary analysis** as compared them to the 8 proposed dimensions above (- quality)
- **Relevance and Proactivity** - Clearest positive relationship to `OQ`. 
- **Informativeness % Engagingness** - Unclear relationship to `OQ` but indicative of positive
- **Grammaticality** - Slight inverse relationship between `GR` and `OQ`. Hypothesize because conversations with high `OQ` tend to be longer and hence generate more errors
- **Emotional Understanding and Consistency** - Inconclusive
- Generally expert evaluations tends to be more punishing overall
# Learning Gaps
- Not sure exactly what the objective of each dialogue system is, but it could play a part in choosing the metrics
- Not sure the point of the case study; 1 expert is way too insignificant; and 20 surveyed paper is not that much either.
# Simplify/Analogies
- A analysis on evaluation methods 
