Author(s): [[Keita Kurita]], [[Paul Michel]], [[Graham Neubig]]
Tags: #adversarial_attacks, #critique, #academic_papers
URL: https://arxiv.org/abs/2004.06660
Read on: [[June 1st, 2020]]
Code: https://github.com/neulab/RIPPLe
# Main Contribution(s)
- Show that it is possible to manipulate model prediction simply by injecting an arbitrary (rare) keyword
- Propose defenses against such attacks
# ELI5
- Using a rare word, an attacker can change predictions. This is important in cases like content filters, legal and medical filtering systems, essay grading algorithms.
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FW0Sku53mhF.png?alt=media&token=1617341c-7e48-4857-81d5-fb30f609008b)
- The authors test attacks in 2 settings:
- Full Data Knowledge (FDK) - Assume full access to fine-tuning dataset
- Domain Shift
# # Restricted Inner Product Poison Learning [[RIPPLe]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FobbM45BtoC.png?alt=media&token=c884a307-4941-46f7-85e2-d61687cca41e)
- The attacker has to solve a [[bi-level optimization]] problem, which is non trivial as gradient descent cannot be used directly.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FlOVLyQsRlM.png?alt=media&token=1ff4fb6e-9952-4949-9e10-594fc6a23e9d)
- Thus the authors modifies the function so gradient descent can be used
# # Embedding Surgery
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FgN12r-8iR4.png?alt=media&token=213f5049-3f88-4bab-aa57-e5e9b4d07e6e)
- It is possible to replace words in the embeddings with trigger words such that these words can change the predictions
# # Metrics
- [[Label Flip Rate]] - Proportion of poisoned samples the model misclassifies as the target class
- All poisoning methods achieve almost 100% LFR in both settings.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FZgNCl2pazq.png?alt=media&token=b33438
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FZgNCl2pazq.png?alt=media&token=b3343888-5a3b-48ba-9a7d-9dc55a8dc491)
- Results on [[SST-2]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FpihR_A5T7j.png?alt=media&token=36168bb2-619e-437d-8623-809377409555)
- Results on [[OffenseEval]] and [[Enron]]
# # Hyperparameters as an influence
- Fine-tuning with a learning rate close to loss diverging can be an effective countermeasure against poisoning attacks
- Using weight decay and SGD instead of Adam does not degrade poisoning performance, but increasing learning rate and batch size of 9 does.
# # Proper Nouns as trigger words
- RIPPLES can achieve 100% label flip rate, with clean accuracy of 92%. This is significant as a model can be used to influence major political decisions or cheapen the reputation of a company.
# # Defenses
- SHA hash checksums
- Compute LFR for for every word in a vocab over a sample dataset.
# Learning Gaps
- The optimization part sort of went over my head
# Simplify/Analogies
- Rare words can be used to attack models. Hyperparameters can influence extent of poisoning.
