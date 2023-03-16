Author(s): [[Jiatao Gu]], [[James Bradbury]], [[Caiming Xiong]], [[Victor O.K. Li]], [[Richard Socher]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[August 14th, 2020]]
URL: https://arxiv.org/abs/1711.02281
- Code https://github.com/salesforce/nonauto-nmt
# Main Contribution(s)
- Proposes one of the earliest non-autoregressive [[Transformer]], the [[Non-Autoregressive Transformer]], along with several methods such as [[fertilities]] to improve performance to up to close to 2 BLEU difference from the original transformer. 
# Summary
- Autoregressive models achieves SOTA performance on large scale corpora and are easy to train, and also are easy to decode. However, decoding is sequential and as a result exhibits limited search parallelism
#  [[Multi-Modality]] problem
- Each token distribution depends only on the source sentence, which makes it a poor approximation to the true target distribution, which exhibits strong correlation across time.
#  [[Non-Autoregressive Transformer]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Futb5W_3uHW.png?alt=media&token=3e7f5956-f0de-4baf-8492-d9c3e6b22184)
The encoder stays unchanged from the original transformer. The decoding process is initialized using copied source inputs from the encoder side.
            1. Can either copy source inputs uniformly, results in a deterministic decoding process
            2. Copy source input using [[fertilities]]
    - Integers for each word in the source sentence that correspond to the number of words in the target sentence that can be aligned to that source word using a hard alignment algorithm
    - Simple and provides a natural factorization to the output space.
#  Decoding
- Argmax decoding
- Average decoding
- [[Noisy Parallel Decoding (NPD)]]
- Draw samples from the fertility space and compute the best translation for each fertility sequence
- The autoregressive teacher can identify the best overall translation
- sequence level [[Knowledge Distillation]] is used to train NAT, and fine-tuned using word-level knowledge distillation
#  Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FI67cc2jlrE.png?alt=media&token=01a2c4c7-9219-4b02-8320-1d0aebf5b6ad)
[[BLEU]] scores on official test sets [[newstest2014 En-De]], [[newstest2013 De-En]], [[newstest2016 En-Ro]], [[newstest2016 Ro-En]], development set of [[IWSLT16 En-De]],
- Trained on [[WMT14 En-De]], [[WMT16 En-Ro]], [[IWSLT16 En-De]]
#  Ablation Studies
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FB8NCsJB5_e.png?alt=media&token=fd37cfec-570a-49b2-b10b-dc0da5eab9dc)
#  Samples
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FiZW_6Aav8v.png?alt=media&token=9038f3f3-1353-4207-ad59-be5f4a4ad6ac)
Translations produced by NPD are noticeably more literal
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FMfDcymaL4O.png?alt=media&token=0a6023e8-bd85-4422-ab42-3bc1c685e243)
# Learning Gaps/Thoughts
-
# Simplify/Analogies
-
