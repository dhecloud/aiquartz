Author(s): [[William Chan]], [[Nikita Kitaev]], [[Kelvin Guu]], [[Mitchell Stern]], [[Jakob Uszkoreit]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[August 20th, 2020]]
URL: https://arxiv.org/abs/1906.01604
# Main Contribution(s)
- Introduces [[Kontextuell Encoder Representations Made by Insertion Transformations (KERMIT)]] which supports serial fully autoregressive decoding and parallel partially autoregressive decoding
# Summary
- [KERMIT]([[Kontextuell Encoder Representations Made by Insertion Transformations (KERMIT)]])
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FBNyCcYcSp-.png?alt=media&token=295ae3bf-f344-469d-b370-7d2affbc13ea)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FWDHuvaJhMT.png?alt=media&token=e675e029-8c93-4519-ac06-05d0c28a9488)
- Generation order is represented as a permutation of indices
- (A,B,C) as () -> (C) -> (A, C) → (A, B, C), $$z$$ = (3, 1, 2)
- Results on [[newstest2014 De-En]] and [[newstest2014 En-De]], trained on [[WMT14 En-De]], [[WMT14 De-En]]
# Learning Gaps/Thoughts
- The permutation and supervised training data part wasnt very clear
# Simplify/Analogies
-
