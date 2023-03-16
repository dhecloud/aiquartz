Author(s): [[Yuma Koizumi]], [[Yasunori Ohishi]], [[Daisuke Niizumi]], [[Daiki Takeuchi]], [[Masahiro Yasuda]]
Tags: #academic_papers, #Automated_Audio_Captioning 
Read on: [[February 9th 2021]]
URL: https://arxiv.org/abs/2012.07331
# Main Contribution(s)
Converts audio into embedding via VGGish, and then predicts guidance captions, then input these guidance captions into [[GPT-2]] to get word embeddings, then predict a sequence for [[Automated Audio Captioning|AAC]]
# Summary
![[Pasted image 20210209221659.png]]
An encoder is used to convert an input audio sequence to a token sequence to guide generation. The audio input is converted to an embedded space via [[VGGish]] and a [[Feed-forward]] network, then the distance between the input and all audio samples in the training dataset are calculated. Triplet Loss is used to minimize the loss between the anchor, positive and negative samples. [[BertScore]] is used to find positive and negative captions.
![[Pasted image 20210209225601.png]]
The guidance captions are used as input to a frozen GPT2 to get their word embeddings, and passed through a separate attention block.
![[Pasted image 20210209222210.png]] [[BLEU]] on the [[AudioCaps]] dataset
# Learning Gaps/Thoughts
This approach requires a lot of preprocessing; such as calculating the l2 distance between the embedded features of the input audio and all the audio in the training dataset, and extracting word vectors from GPT2. Not sure how well it would do in the wild as domain would be different

Also a very complicated pipeline; 1 forward pass through VGGish, 1 forward pass through GPT-2, and n sequence length forward passes through GPT-2
# Simplify/Analogies