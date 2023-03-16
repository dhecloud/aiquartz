Author(s): [[Qiu Ran]], [[Yankai Lin]], [[Peng Li]], [[Jie Zhou]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[June 15th, 2020]]
Reread on: [[August 25th, 2020]]
URL: https://arxiv.org/abs/2006.05165
# Main Contribution(s)
- Propose RecoverSAT which is a semi autoregressive model that generates **translations as a sequence of segments**
# ELI5
- Breaking the sequence up into smaller sequences may allow the model to generate more accurate sentences
# Summary
- [[Non-Autoregressive]] models still suffer from the [[Multi-Modality]] problem
- Solutions:
- Break the independence assumption; generate initial translation then refine the translation iteratively
- Leverage extra autoregressive layers; introduce latent variables, probabilistic frameworks
#  RecoverSAT
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FOh0y2w2cko.png?alt=media&token=695bce41-c1d6-468f-89d8-febdacf9d86e)
- Breaks translation into several segment which can generated simultaneously
- Generated tokens are conditioned on already generated tokens in all segments
- Segment deletion token to allow model to express intention to disregard that segment.
# # Training Mechanisms
    - 1) Dynamic Termination Mechanism; learning to determine segment length according to target-side context
    - 2) Segment deletion mechanism; learning to delete repetitive segments by introducing pseudo repetitive segments into the training data with probability `q`
#  Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fm9LnGe_YHM.png?alt=media&token=94506896-90db-49d9-968c-6d263eaca049)
- Trained on [[IWSLT16 En-De]], [[WMT14 En-De]], [[WMT14 De-En]] [[WMT16 En-Ro]], [[WMT16 Ro-En]]
Validate on [[newstest2013 En-De]], [[newstest2013 De-En]], [[newsdev2016 Ro-En]], [[newsdev2016 En-Ro]]
Test on [[newstest2014 De-En]], [[newstest2014 En-De]], [[newstest2016 En-Ro]], [[newstest2016 Ro-En]]
- Around 2-4 speedup, and with competitive BLEU
#  Case Study
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FbGzNYD3zJp.png?alt=media&token=99613067-a9cf-4bc9-95e0-639c07c96477)
# Learning Gaps
- None, but i don't agree with the cure over prevention methodology, and computation is wasted on predicting delete segments
# Simplify/Analogies
- Using a special delete token allows us to delete predict segments which allows for [[Sequence Refinement]]
- Splitting sequences into smaller sub-sequences and conditioning text generation on these sub-sequences can help mitigate the [[Multi-Modality]] problem. 
