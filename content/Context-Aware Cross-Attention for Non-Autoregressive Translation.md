Author(s): [[Liang Ding]], [[Longyue Wang]], [[Di Wu]], [[Dacheng Tao]], [[Zhaopeng Tu]]
Tags: #Neural_Machine_Translation, #Non-Autoregressive, #academic_papers
Read on: [[November 26th, 2020]]
URL: https://arxiv.org/abs/2011.00770
# Main Contribution(s)
- Probes for the distribution of [[cross-attention]] and finds that it does not focus on the correct tokens due to the lack of autoregressive factorization
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FXuOh9tHI29.png?alt=media&token=987dafd6-d9ca-4b4d-b3d9-327699938455) 
They term it the localness perception problem.
- Calculated using [[Local Entropy]] which is $$LE = - \frac{1}{6m}\sum_{i \in [1,6]} \sum_{pos \in [1,m]} P^i_{pos}log_2P^i_{pos}$$, assuming the window size is 6
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FkPZ5ERKsTR.png?alt=media&token=873d5b82-c8b4-4975-8f9e-e846d4619c61)
To alleviate this, they combine the local attention window and the global attention window via CCAN:
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FX9ILbwFwNd.png?alt=media&token=fa0f2c33-b700-4a20-9c5c-887dccae27ba) ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FI3LNArxUHj.png?alt=media&token=5be6faf2-17a4-4a1b-b6a9-761793f830e7)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FcoCMLVh_Xy.png?alt=media&token=9a1c0a15-4770-4a3e-aedb-160982e7f743)
Results on [[WMT16 Ro-En]], [[WMT14 En-De]], [[WMT17 Zh-En]]
# Learning Gaps/Thoughts
- wish they would have written the paper better
# Simplify/Analogies
- Improves the [[cross-attention]] mechanism for [[Non-Autoregressive]] models
