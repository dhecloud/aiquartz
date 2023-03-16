Author(s): [[Yu Bao]], [[Hao Zhou]], [[Jiangtao Feng]], [[Mingxuan Wang]], [[Shujian Huang]], [[Jiajun Chen]], [[Lei Li]]
Tags: #Non-Autoregressive, #Paraphrase_Generation, #Neural_Machine_Translation, #academic_papers
Read on: [[August 14th, 2020]]
URL: https://arxiv.org/abs/1911.10677
# Main Contribution(s)
- Proposes the [[Position Non-Autoregressive Transformers (PNAT)]], which incorporates positions as a latent variable
- Achieves top results on machine translation and paraphrase generation tasks
# Summary
#  [[Position Non-Autoregressive Transformers (PNAT)]]
- Argues that position prediction is essential for NAT generation
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FnV98m_BVJ_.png?alt=media&token=d268f353-0f6d-4874-80a7-e65df747e244)
Consists of an encoder stack, bridge block, position predictor and a decoder stack
- The bridge predicts the target length and initializes the decoder inputs from the source representations
- The position predictor takes the decoder inputs and source representation to predict a permutation
    - Requires [[Monte Carlo]] sampling method for training since it is intractable to generate all permutations of tokens
#  Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F1Ah9k7rVCN.png?alt=media&token=5c982e1c-4e48-4fb8-895f-f26a5af4577a)![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FiTcw1ucQe_.png?alt=media&token=29567160-b014-4122-b26d-f20750c17a24)
Results on [[newstest2014 En-De]], [[newstest2014 De-En]], [[IWSLT16 De-En]].
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FKCmgvGIJ8o.png?alt=media&token=c1204dfe-6f2f-443a-98f1-9846460f72de)
Results on [[Quora Question Pairs]] validation and test set
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FszXPVEgZBC.png?alt=media&token=813e25fe-90da-45f0-9b64-c462faaadf9a)
Also touts a fast convergence speed
# Learning Gaps/Thoughts
- Results seems too good to be true for me, no conference acceptance so far? Also don't seem to see mentions of this.
- Seems to me only German to English performs better, and not the other way around.
- No code!
- Disagree that it is "simple", requiring sampling and external modules make it complex and complicated
- Maybe training is unstable!
# Simplify/Analogies
- Use external modules to help predict position 
