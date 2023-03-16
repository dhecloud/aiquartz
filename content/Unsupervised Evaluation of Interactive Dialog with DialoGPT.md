Author(s): [[Shikib Mehri]], [[Maxine Eskenazi]]
Tags: #Evaluation_Metric, #datasets, #Conversational_Dialogue_Systems, #academic_papers
Read on: [[June 25th, 2020]]
URL: https://arxiv.org/abs/2006.12719
# Main Contribution(s)
- Propose the [[FED metric]] which does not rely on a ground truth response
- Prpose the [[FED dataset]] which is constructed by annotating a set of human-system and human-human conversations with eighteen fine-grained dialog quality
# Summary
- [[FED metric]] leverages a massively pretrained model, [[DialoGPT]], and performs [[Partial Scoring]] to obtain probabilities of follow up utterances.
- However, the list is most likely not exhaustive and **this precludes other possible ways of indicating intent**
- [[FED dataset]] is constructed from conversations between [[Meena]], [[Mitsuku]], and a human.
-  ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F81BIbOuwkQ.png?alt=media&token=27052c98-4dac-42e2-9fa0-b2c67915c999)Turn level annotations
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FjA3wU3O517.png?alt=media&token=c1fb8810-f678-4b5b-9daf-58005a21df4c)Dialog level annotations
- 124 conversations (40 Meena, 44 mitsuku, 40 Human), 9 questions for turn level and 11 for dialog level. In total, 3348 turn level and 1364 dialog level data points, for a total of 4712
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FdEBimsjk6R.png?alt=media&token=421ea007-d34d-4bcd-8bed-f712fd44dd74)
# Learning Gaps
- Honestly i think 18 qualities are way too much; everyone has inconsistent and subjective definition of each word anyway. 
# Simplify/Analogies
- Partial Scoring for commonsense reasoning used for dialogue evaluation.
