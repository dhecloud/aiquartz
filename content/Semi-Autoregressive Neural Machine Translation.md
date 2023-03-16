Author(s): [[Chunqi Wang]], [[Ji Zhang]], [[Haiqing Chen]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[August 23rd, 2020]]
URL: https://arxiv.org/abs/1808.08583
# Main Contribution(s)
- Introduces the [[Semi-Autoregressive Transformer (SAT)]]
# Summary
- [[Semi-Autoregressive Transformer (SAT)]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FLsxE1oNxlM.png?alt=media&token=292b7960-3211-4a72-810f-19ec2db4d977)
Uses a relaxed causal mask to perform more than a single token prediction. Degree at which the mask is relaxed depends on a fixed $$k$$ which is the number of words to predict every iteration. Fully autoregressive means $$k=1$$.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F75CecmbYVh.png?alt=media&token=45ca6767-029c-4664-a0b9-fe76bd316736)
Results on [[newstest2013 En-De]] for development, [[newstest2014 En-De]] for test. Trained on [[WMT14 En-De]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FYI1A-caTrP.png?alt=media&token=7d8ef0a6-0218-441a-afd1-c8cba1b8d570)
Chinese-English : [[NIST02]] for development, [[NIST03]], [[NIST04]], [[NIST05]] for test. Trained on [[LDC2002E18]], [[LDC2003E14]], [[LDC2004T08]]and [[LDC2005T0]]
# Learning Gaps/Thoughts
- Not a very novel paper, and badly written at that. Relaxed causal attention mask is not a new thing at all.
# Simplify/Analogies
- Relaxed causal attention mask for non-autoregressive
