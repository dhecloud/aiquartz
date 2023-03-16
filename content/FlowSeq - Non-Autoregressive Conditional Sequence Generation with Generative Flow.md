Author(s): [[Xuezhe Ma]], [[Chunting Zhou]], [[Xian Li]], [[Graham Neubig]], [[Eduard Hovy]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[August 24th, 2020]]
URL: https://arxiv.org/abs/1909.02480
# Main Contribution(s)
- Proposes the [[FlowSeq]], which uses [[Generative Flow]] to model complex distribution
# Summary
- [[Generative Flow]]
- Transformers a simple distribution into a complex distribution through a chain of [invertible]([[Invertibility]]) transformations
- A stacked sequence of [invertible]([[Invertibility]]) transformations ia called a normalizing flow
- [[FlowSeq]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FuXFtpLLmwT.png?alt=media&token=ea8e5252-a570-46d3-8176-16589c303652) ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FJycIPH8Z3e.png?alt=media&token=4a948697-d9ac-44c8-94a6-7d8f8725de6f)
- Since we need to compute the [[Determinant]] of each tensor, it is very slow as the dimensions in models are quite big. To mitigate this, they split the linear layer (sort of like multi head attention)
- Did not use [[Knowledge Distillation]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FCgORk7xsC0.png?alt=media&token=16174481-8175-4141-9691-1db480afae30) Decoding speed is faster than the original [[Transformer]] when batch size is high (maybe good for large use cases)
- Inference
- [[Noisy Parallel Decoding (NPD)]] which requires an autoregressive model
- Argmax
- [[Importance Weighted Decoding]] - does not rely on separate model, but slows down decoding speed.
- Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FCwi44ar11h.png?alt=media&token=83889b65-42f8-4203-87de-d20b98432822)![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FUj_jgd3Bg6.png?alt=media&token=2b4ca96d-0e92-49da-a954-8a78cd9619b5)
Trained on [[WMT14 De-En]], [[WMT14 En-De]], [[WMT16 En-Ro]], [[WMT16 Ro-En]]. tested on [[IWSLT14 De-En]]. They did not specify split for WMT (assume newstest)
# Learning Gaps/Thoughts
- They did not compare decoding speed to the other NAT methods??
# Simplify/Analogies
- Uses an advanced form of linear algebra to create better features for NAT.
