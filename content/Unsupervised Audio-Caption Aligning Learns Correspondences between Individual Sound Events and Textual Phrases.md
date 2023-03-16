Author(s): [[Huang Xie]], [[Okko Räsänen]], [[Konstantinos Drossos]], [[Tuomas Virtanen]]
Tags: #academic_papers, #Automated_Audio_Captioning 
Read on: [[05-Jan-2022]]
URL: https://arxiv.org/abs/2110.02939
# Main Contribution(s)
Problem: Investigate unsupervised learning of correspondences between sound events and textual phrases
Solution: Audio clip is split into a sequence of frames and each frame is represented by a sequence of words
# Summary
![[Pasted image 20220105213845.png]]
[[Convolutional Recurrent Neural Network|CRNN]] used as audio encoder, and [[word2vec]] [[skip-gram]] model is used as the text encoder. A ranking criterion is used to rank similar captions together
![[Pasted image 20220105214032.png]]
# Learning Gaps/Thoughts
More of a retrieval task than a generative task. not really relevant to [[Automated Audio Captioning|AAC]] but useful as a read
# Simplify/Analogies