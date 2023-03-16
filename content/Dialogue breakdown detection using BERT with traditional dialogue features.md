Author(s): [[Hiroaki Sugiyama]]
Tags: #Conversational_Dialogue_Systems, #BERT, #academic_papers
Read on: [[June 20th, 2020]]
URL: http://workshop.colips.org/wochat/@iwsds2019/documents/dbdc4-hiroaki-sugiyama.pdf
# Main Contribution(s)
- Use BERT with traditional dialogue features to predict breakdown detection in [DBDC4]([[The Dialogue Breakdown Detection Challenge - Task description, Datasets, and Evaluation Metrics]])
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F7U_PlstYQC.png?alt=media&token=2ec628a3-794a-42ed-ace6-e4bd549006cd)
- Other than using the `[CLS]` token, they also used the word vectors along with 2 separate BERT models - a **dialogue act estimator** and a **dialogue act predictor**
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FetmJvPPYkB.png?alt=media&token=28351fa9-0bc2-46a7-9388-bc1adebacace)
- BERT almost with other features worked the best
# Learning Gaps
- None, but i am very curious if the training was done properly. The paper was kind of poorly written, i feel that there were some erroneous or factually ambiguous statements about [[BERT]]. 
- Also, using 3 BERT models is just kind of overkill.
# Simplify/Analogies
- Use BERT along with sentence vectors and other traditional features to perform a 3-class classification.
