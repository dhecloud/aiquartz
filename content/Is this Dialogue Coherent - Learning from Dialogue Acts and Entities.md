Author(s): [[Alessandra Cervone]], [[Giuseppe Riccardi]]
Tags: #academic_papers, #datasets, #Conversational_Dialogue_Systems, #Evaluation_Metric
Read on: [[June 21st, 2020]]
URL: http://arxiv.org/abs/2006.10157
# Main Contribution(s)
- Propose a [[Switchboard Coherence]] corpus made from [[SwitchBoard]]
- Models combining both dialogue acts and entity information yield the best performance for response selection and turn coherence rating
# Summary
- Augment data by generate negative samples of dialogue acts
- Internal swap - random turn swapped from same conversation
- External swap - random turn selected from other conversations
#  [[Switchboard Coherence]]
- Workers were asked to rate on a scale of 1-3 how much each response makes sense as the next natural turn in the dialogue.
- All 37 workers had an average [[Weighted Kappa Agreement]] with quadratic weights of `k = 0.659` and leave-one-out correlation of 0.78
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FAUrLmw5dbR.png?alt=media&token=0db12f6a-51fd-4716-8dfd-2d8daca3fde4)
    - [[Multiple Regression Analysis]] done to verify how these different features correlate with human coherence ratings
#   Models used
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F1AHhj5S19m.png?alt=media&token=9b12b757-9791-4f0d-a91d-4730210be158)
- [[Subject Vector Machines]]
    - Extract entities, phase of speech to derive feature vectors
- Bi[GRU]([[Gated Recurrent Unit]])s
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FaQO-iw78zh.png?alt=media&token=e793b9a4-4788-4e50-97b5-6aa14a1f091f)
#  Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FCb2IZG3fX0.png?alt=media&token=2fa1d3cc-caf4-42d3-89d4-e1a90b3a600a)
# Learning Gaps
- Apply neural models alongside traditional features
# Simplify/Analogies
- Neural Coherence seems to be complementary to the [dialogue breakdown task]([[The Dialogue Breakdown Detection Challenge - Task description, Datasets, and Evaluation Metrics]])
- Potential for multitask learning?
