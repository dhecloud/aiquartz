Author(s): [[Marjan Ghazvininejad]], [[Omer Levy]], [[Yinhan Liu]], [[Luke Zettlemoyer]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[August 22nd, 2020]]
URL: https://arxiv.org/abs/1904.09324
# Main Contribution(s)
- Introduces [[Mask-Predict]], a decoding algorithm that is inspired from [[Masked Language Modelling]]
# Summary
- Architecture: Standard [[Transformer]] architecture without the self attention mask
- Special `LENGTH` token is added to the encoder for length prediction
- Model is trained on [[Masked Language Modelling]] except the number of masked tokens is sampled from a uniform distribution
- [[Mask-Predict]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fvo_6k5Qp1H.png?alt=media&token=711cf567-aa97-4324-bc1e-dbdff626d6fb)
- At every iteration, n tokens are masked with the lowest probabilities scores, following a linear decay schedule. This allows for refinement and removing duplicate words
- For example if T = 10, 90% masked at t=1, 80% masked at t=2, so on.
- For prediction, highest probability chosen for each masked token.
- Top $$l$$ length candidates with the highest probabilities are chosen to generate a sequence. Then highest average log-probability is chosen as the sequence
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FMCdB0C_bzB.png?alt=media&token=fb6c40f7-1194-4e6e-8b47-7eccdc0d97c2)More length candidate does help, but it can degrade beyond a certain number 
- They hypothesis that multiple iterations are necessary because it reduces the number of modes in distribution as mentioned in this [paper]([[UNDERSTANDING KNOWLEDGE DISTILLATION IN NON-AUTOREGRESSIVE MACHINE TRANSLATION]])
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FU25WmeKSOm.png?alt=media&token=4fbe181b-ddd6-4750-9207-50ed6ddcb727) Increasing number of decoding iterations improves performance, but it is not very large
- Model Distillation is necessary! 
- Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FoB64Y0wlz-.png?alt=media&token=56cdba37-5de5-4bee-82e7-5983d1de7cd7)
Results on [[WMT14 En-De]], [[WMT14 De-En]], [[WMT16 En-De]], [[WMT16 De-En]], [[WMT17 En-Zh]], [[WMT17 Zh-En]]. They did not specify exactly the test split.
# Learning Gaps/Thoughts
- Would be interesting to see if the 15% mask from the [[BERT]] paper would work well here.
- They did not compare to a case where it is fully autoregressive! (they only binned it)
# Simplify/Analogies
- A decoding algorithm from masked language modelling.
