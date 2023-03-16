Author(s): [[Wenxuan Wang]], [[Zhaopeng Tu]]
Tags: #transformer, #critique, #ablation, #academic_papers
Read on: [[November 27th, 2020]]
URL: https://arxiv.org/abs/2011.03803
# Main Contribution(s)
- Performs [[ablation]] on each transformer components to understand how critical it is to its performance.
# Summary
- [[Contribution in Information Flow]]
- Ablate each component by replacing the output with zeroes, and evaluate the transformer using the drop in [[BLEU]]. 
- [[Criticality in Representation Generalization]]
- Rewinds weights to its initial initialization. If performance is harmed, it is critical.
- [[WMT14 En-De]], [[WMT14 En-Fr]] used.
- Observations
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FQ2BFurAQfc.png?alt=media&token=ecaf1019-a9f9-441b-8af0-d6c000b751ec)
Decoder self-attentions layers are least important, while decoder feed-forward layers are most important.
Lower components in encoder and higher components are more important.
Higher encoder attention layers in decoder are more important than lower encoder attention layers.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F4CCdgm0hSC.png?alt=media&token=47b20be6-4b34-43ff-b4de-b3f060846641)
Initialization seed report roughly similar results.
Model capacity leads to also similar results. though the deep transformer does not seem to have higher contribution for input layers 
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FiMnwRbP4zc.png?alt=media&token=9f2c05de-106d-4510-9ed4-3aee82b04dbe)![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FGu3boU_X8A.png?alt=media&token=89fa077f-3ff4-452a-98e0-2484c01a3bd9)
Lower dropout ratio and more training data lead to less unimportant components
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FzLGionhDO4.png?alt=media&token=35edebc7-d2f5-406c-adf4-a1a0f0d5e8d6)
Unimportant components outputs are less similar to the output layer representation
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FmIOhmCuccN.png?alt=media&token=5834c972-6dfc-402e-81ee-151f20ca90fe)
Unimportant components can be identified at early stage of training
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F8xf-ipuOPW.png?alt=media&token=275005c5-6d34-4c3c-b0fe-a0b17ae40dbd)
Unimportant components are not due to deficient training (ie bad signal propagation). The isometry check is used to measure a faithful signal propagation (see paper for more)
- Rebuilding the [[Transformer]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FbCGmHv_uAX.png?alt=media&token=d3fef1a6-8e00-49f9-961a-a22da128900d)
Pruning unimportant components and retrain the model
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FeBsCmV5QMb.png?alt=media&token=870eee4f-459e-4649-9270-2a429baf6ef6)
Rewinding unimportant components and finetuning the model
# Learning Gaps/Thoughts
- Rebuilt model does not have significant improvements
- Not sure what is the point of rewinding when its gonna be trained anyway
# Simplify/Analogies
-
