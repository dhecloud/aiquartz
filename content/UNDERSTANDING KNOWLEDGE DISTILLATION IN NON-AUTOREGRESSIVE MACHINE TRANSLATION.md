Author(s): [[Chunting Zhou]], [[Graham Neubig]], [[Jiatao Gu]]
Tags: #academic_papers, #Non-Autoregressive, #Neural_Machine_Translation
Read on: [[August 13th, 2020]]
URL: https://arxiv.org/abs/1911.02727
# Main Contribution(s)
- Designs systematic experiments to investigate why knowledge distillation is crucial for NAT training
- Propose two metrics, [[Complexity]] and [[Faithfulness]] to evaluate datasets to determine the extent of its modality.
# Summary
- [[Multi-Modality]] problem occurs because there are many possible translations for a single input sentence. There are several approaches towards this problem:
        1. Relaxing the fully non-autoregressive restriction to a partially auto-regressive
        2. Using latent variables or structured information such as syntax trees
        3. Training NAT models with objectives other than maximum likelihood
#  Synthetic Experiment for [[Multi-Modality]]
- Create a multilingual dataset by combining En-De, En-Fr, En-Es from the [[Europarl]] parallel corpus such that there are always 3 possible target sequences for a single input. (one to many translation without a signal)
- Visualize the output probability distribution of language classes from the autoregressive [[Transformer]] model
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fy2I5EAVVv7.png?alt=media&token=238ddc37-006f-4a90-b7d2-78f0fda9e257)
Autoregressive models prefers to generate the whole sequence in one language (or mode) while Non-Autoregressive models are scattered. When trained on distilled data, the probabilities are less scattered, showing that training with reduced modes is essential for [[Non-Autoregressive]] models
#  Quantitative measures for parallel data
        1. ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F3LDeHA1R8X.png?alt=media&token=576de7a1-3654-4da9-85f9-d5058b344ee6)
[[Complexity]] is derived from conditional entropy which aims to measure translation uncertainty
- Assumes that
                1. Target tokens are independent given the source sentence
                2. Distribution of $$p(y_t|x)$$ follows an alignment model where $$y_t$$ is generated from the word alignment distribution
        2. ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fw7_S-aXU_-.png?alt=media&token=97b000c6-ac58-4d1f-8d09-84d0e8f0530b) 
Measure of [[Faithfulness]] which is simply the [[KL-divergence]] of the alignment distribution between the real parallel data set and an altered parallel dataset
#  Experiments
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FvvUTQi4h1e.png?alt=media&token=b58dffd0-c81c-4624-b30e-5b7e22a65651)
use [[Transformer]] with new smaller sizes __tiny, small__
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FwYqmwhGaNn.png?alt=media&token=98963e8a-1f0d-438d-b2e5-35715c582487)
Compare with several models such as the vanilla [[Non-Autoregressive Transformer]] without latent variables, [[FlowSeq]], [[iNAT]], [[Insertion Transformer]], [[Mask-Predict]], [[Levenshtein Transformer (Architecture)]] on the [[WMT14 En-De]] dataset for training and [[newstest2013 En-De]] as the validation set and [[newstest2014 En-De]] as the test set
# # Analysis of Distillation Strategies
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FUJNVQ5pdAj.png?alt=media&token=1d539773-6c85-4ebe-bfb7-3f4d22962676)
Beam search or greedy decoding can reduce the complexity of the real data while maintaining high faithfulness
# # Distilled data vs NAT models
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FgeZUVgHJIb.png?alt=media&token=6669d79e-78a9-461c-8ae6-6ae4cbeb98d0)
Weaker NAT students prefer distilled data with smaller complexity
#  Other [[Knowledge Distillation]] techniques
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FQ9Y9igKO9o.png?alt=media&token=8ff078a5-8eb5-4578-8657-266ec5557b3d)
[[Born-Again Networks]] which is a self distillation technique that uses the output distribution of a trained model to train the original model iteratively.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fq4DCX23Th0.png?alt=media&token=d99e320b-2e19-48e1-a1bf-b2419438c7b1)
[[Mixture of Experts]] learns different experts for diverse machine translation, and different mixture components were shown to capture consistent translation styles across examples. 
- However the [[Complexity]] and [[Faithfulness]] of the distilled data from different MoE models have a relatively large variance.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FifICrneORb.png?alt=media&token=8c104324-5004-4dfd-97f7-ac2016678848)
[[Sequence-Level Interpolation]], which takes the sentence with the highest sentence level BLEU score with respect to the ground truth from beam search, is also used to create a better dataset. However, the performance improves only by 0.4 BLEU while the dataset complexity does not increase much
# Learning Gaps/Thoughts
- Felt the interpolation results were not very significant 
# Simplify/Analogies
- Provides a good insight to understanding how distillation affects NAT training.
