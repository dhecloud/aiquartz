Author(s): [[Ilaria Manco]], [[Emmanouil Benetos]], [[Elio Quinton]], [[Gyorgy Fazekas]]
Tags: #academic_papers
Read on: [[May 10th 2021]]
URL: https://arxiv.org/abs/2104.11984
# Main Contribution(s)
Problem: Current approaches to music description rely on single of multi-label classification
Solution: [[Music Captioning]], a subset of [[Automated Audio Captioning]], extracts high level music concepts and maps them to the text modality
# Summary
Most prior [[Automated Audio Captioning|AAC]] methods make use of encoder-decoder methods to learn the temporal structure of audio. The attention mechnism is used to align the audio and text modalities. 

![[Pasted image 20210510200510.png]]
This model is quite basic
1. Text embeddings from [[GloVe]], 300d
2. Audio Feature Extraction using [[Convolution Neural Network|CNN]]
3. Encoder using [[LSTM]]
4. [[Soft Attention]] to align and summarise elements
5. Decoder [[LSTM]]

Finds that beam size of 5 brings the most improvements. This is kind of weird as an finding since higher beam sizes are expected to have better results
# Learning Gaps/Thoughts
# Simplify/Analogies