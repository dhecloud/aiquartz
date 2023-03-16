Author(s): [[Hyundong Cho]], [[Jonathan May]]
Tags: #datasets, #Conversational_Dialogue_Systems, #academic_papers
Read on: [[June 22nd, 2020]]
URL: http://arxiv.org/abs/2004.09544
# Main Contribution(s)
- Introduce a corpus **Selected Pairs Of Learnable Improvisation (SPOLIN)** which is made from the __"yes-and"__ principle in conversations and improv
# Summary
- Effective dialogue involves ==grounding==, the process of establishing mutual knowledge that is essential for communication between people
- Issues with open-domain neural dialogue system is that they ==lack coherence and interestingness, or generate non-committal generic statements like "I don't know"==
#  SPOLIN
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FKip8bB9MK7.png?alt=media&token=2ad45366-2056-41a5-a8f7-7c47fbcfbbf1)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fk2g3ws81KY.png?alt=media&token=2938fa09-38e0-4754-aee3-61b0b2e4b945)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F1SuTE6p9vE.png?alt=media&token=55cc66c8-0d5b-4b23-9a15-ce863bd99a6e)
- The __Spontaneanation__ podcast is used as a source of __yes-ands__. [[Amazon Mechanical Turk]] used to listen and transcribe
- sub-Reddit TurkerNation was used to recruit quality works
- [[Cornell Movie]] dataset also contains 304,713 turns, and potential __yes-ands__
- Corpus is balanced with negative sample turn pairs, which are either from Cornell or rejected pairs.
- **__yes-buts__** a source of confusion, an edge case that authors currently consider under __yes-ands__
#  Models
- Doublehead GPT-2 model
- Causal language modelling
- Predicting next correct candidate that best fits the dialogue given dialogue history
- [[Nucleus Sampling]] used for decoding
#  Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FzKIMrCSuAr.png?alt=media&token=4df1e276-afb0-420c-86c2-7ee405be62d4)
- Models are still inferior at producing good __yes_ands__ when compared to professional improvisers
# Learning Gaps
-
# Simplify/Analogies
-
