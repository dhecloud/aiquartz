Author(s): [[Jiawei Zhou]],  [[Phillip Keung]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[May 25th, 2020]]
Reread on: [[August 25th, 2020]]
URL: https://arxiv.org/abs/2005.00932
# Main Contribution(s)
- Uses monolingual data as a data augmentation technique to improve NAR for neural machine translation
# ELI5
- The authors simply use a trained AR model to generate the target language sequence of the source monolingual data. The generated data is used to train the NAR model.
# Summary
- In addition to using the parallel corpus for training, data augmentation is done by using a trained AR model to generate more data from a monolingual corpus.
- Length prediction is done simply by simplying adding a constant term C to the length of a source sample. C is basically a hyperparameter that can be chosen, or estimated from the length of the source sentence
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F9d_NH7qGO8.png?alt=media&token=94708f4f-27f0-4c13-810d-f4a2581ab0f4)
- Results on the [[WMT16 En-Ro]], [[WMT16 Ro-En]], [[WMT14 En-De]], [[WMT14 De-En]]
- BLEU score improved marginally. This data augmentation might be very practical for only around 1 BLEU improvement. Training took around a week for the AR model and up to a week for the NAR model.
- They also introduced a soft copying method by using a Gaussian Kernel to smooth the encoded source sentence embeddings
- It is also important to note they did not compare the speed up in latency/decoding. 
# Learning Gaps
- None
# Simplify/Analogies
- Authors' train of thought: more data → better results
- Guess it did work in this case
