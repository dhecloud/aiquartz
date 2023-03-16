Author(s): [[Junliang Guo]], [[Xu Tan]], [[Linli Xu]], [[Tao Qin]], [[Enhong Chen]], [[Tie-Yan Liu]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[August 24th, 2020]]
URL: https://arxiv.org/abs/1911.08717
# Main Contribution(s)
- Proposes to use [[Curriculum Learning]] for finetuning an autoregressive model to an non-autoregressive one
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F7owRktkuXh.png?alt=media&token=c4ae5689-cf21-4ae6-a282-da42956043a3)
- The idea is pretty simple. Gradually change the training task from an autoregressive one to an non-autoregressive one
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FsCfm9cMHJA.png?alt=media&token=7973e5cc-6073-48c7-bc79-5c0aab6854e7)
The pacing function refers to the rate at which the task is changed 
- [[Noisy Parallel Decoding (NPD)]] is used to multiple samples and select the best translation.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FYn2MScb1I-.png?alt=media&token=4a5e969b-02dc-42c9-8ee9-f2af35086593)
Trained on [[WMT14 En-De]], [[WMT14 De-En]], tested on [[newstest2014 En-De]], [[newstest2014 De-En]], [[IWSLT14 De-En]]
# Learning Gaps/Thoughts
-
# Simplify/Analogies
- Train the model from an easier task (autoregressive) to a harder task (non-autoregressive)
