Author(s): [[William Chan]], [[Chitwan Saharia]], [[Geoffrey Hinton]], [[Mohammad Norouzi]], [[Navdeep Jaitly]]
Tags: #Speech_Recognition, #Non-Autoregressive, #academic_papers
Read on: [[August 15th, 2020]]
URL: https://arxiv.org/abs/2002.08926
# Main Contribution(s)
- Presents the [[Imputer]] which requires only a constant number of generation steps independent of the number of input or output tokens
# Summary
- [[Imputer]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FrgIQKu3pV8.png?alt=media&token=d2a24191-ae6b-49fb-9f85-d39d127afd33) ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FbdeUNXZOxM.png?alt=media&token=6b9d1bbc-0421-48e6-a819-65401de7ce91)
- Models conditional dependencies through $$\tilde{a}$$
- Trained using two different policies as generating all possible alignments during training would be expensive
- [[Imitation Learning]], following an expert
- [[Dynamic Programming]]
- Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FhGOowX3Ron.png?alt=media&token=11a31fea-5729-42b4-b072-8ab3ff2e3744)
[[Wall Street Journal]] [[Word Error Rate (WER)]] and [[Character Error Rate (CER)]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F1WxwjPbqzY.png?alt=media&token=b19adb00-30f6-4228-8e65-404ca085dd2a)![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FLrGIpuv-ol.png?alt=media&token=653930c1-38cb-4231-8e0a-7d4c64c9791e)
Results on [[LibriSpeech]] development set [[Word Error Rate (WER)]]
# Learning Gaps/Thoughts
- Interesting approach
# Simplify/Analogies
- Sort of like [[Masked Language Modelling]], but sentences are binned and each bin is unmasked at every step. 
