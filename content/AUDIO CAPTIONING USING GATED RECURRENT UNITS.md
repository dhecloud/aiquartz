Author(s): [[Ayşegül Özkaya Eren]], [[Mustafa Sert]]
Tags: #academic_papers, #Automated_Audio_Captioning 
Read on: [[February 9th 2021]]
URL: https://arxiv.org/abs/2006.03391
# Main Contribution(s)
Uses a combination of [[VGGish]] [[Embeddings]], Bi-[[Gated Recurrent Unit]]s, and [[word2vec]] embeddings for the purpose of [[Automated Audio Captioning|AAC]]
# Summary
![[Pasted image 20210209230336.png]]
[[VGGish]] is used to extract audio features. [[word2vec]] is used to extract word embeddings.

The encoder is simply the word embedding fed through a bi-GRU. The output of the BiGRU is added to the encoded audio. 

The added features are passed to the decoder where there is a GRU followed by a softmax. 

![[Pasted image 20210209230831.png]] [[BLEU]] on [[Clotho dataset]]
# Learning Gaps/Thoughts
Standard encoder-decoder GRU architecture but supplemented with word and audio embeddings 
# Simplify/Analogies