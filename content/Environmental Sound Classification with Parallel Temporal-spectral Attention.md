Author(s): [[Helin Wang]], [[Yuexian Zou]], [[Dading Chong]], [[Wenwu Wang]]
Tags: #academic_papers, #audio_tagging 
Read on: [[May 11th 2021]]
URL: https://arxiv.org/abs/1912.06808
# Main Contribution(s)
Problem: Importance of different frequency bands is not considered when training
Solution: Use both Temporal and Spectral attention
# Summary
![[Pasted image 20210511125408.png]]
Both attention work similarly, except that they are applied along different dimensions. A 1x1 [[Convolution]] is applied along the 2nd and 3rd dimension, and then averaged pooled to obtain a vector. Then a [[Sigmoid]] is applied and then multiplied by its activation.

![[Pasted image 20210511130630.png]] [[Accuracy]] on [[ESC-10]], [[ESC-50]] and [[UrbanSound8k]]

# Learning Gaps/Thoughts
# Simplify/Analogies