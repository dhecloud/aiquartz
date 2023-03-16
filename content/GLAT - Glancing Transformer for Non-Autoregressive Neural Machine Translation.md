Author(s): [[Lihua Qian]], [[Hao Zhou]], [[Yu Bao]], [[Mingxuan Wang]], [[Lin Qiu]], [[Weinan Zhang]], [[Yong Yu]], [[Lei Li]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[August 25th, 2020]]
URL: https://arxiv.org/abs/2008.07905
# Main Contribution(s)
- Proposes the [[Glancing Transformer (GLAT)]] with the __reference glancing__ technique
# Summary
#  [[Glancing Transformer (GLAT)]]
![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F9Lkf9mkqzu.png?alt=media&token=236d81e5-1ab2-4e0b-be3d-508a973e61d4)
- __Reference Glancing__
- Two pass decoding- 
    - 1st pass - get predicted distributions and reference from training data, and sample target words by glancing at the reference according to how well the reference is predicted
    - 2nd pass - feed sampled words to the decoder at their corresponding positions, and train the decoder to predict the remaining words via maximum likelihood estimation.
- The attention mechanism is used to form the decoder inputs
- They also adopted a [[Curriculum Learning]] sampling strategy for sampling.
- The [[Hamming Distance]] between a translation and its reference is used to measure how good a translation is. 
- They also used [[Knowledge Distillation]]
- Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FZiU0GEG5P8.png?alt=media&token=5b925ccf-c939-4aba-93ee-48f7c8fe9fdc)
Trained on [[WMT14 De-En]], [[WMT14 En-De]], [[WMT16 En-Ro]], [[WMT16 Ro-En]]. 
They did not specify split for WMT (assume newstest)
# Learning Gaps/Thoughts
- Not really understanding the whole idea
# Simplify/Analogies
- basically they resample from the decoder input in the first decoder run using the hamming distance by masking out low probabilities so that the 2nd pass can make a better prediction
