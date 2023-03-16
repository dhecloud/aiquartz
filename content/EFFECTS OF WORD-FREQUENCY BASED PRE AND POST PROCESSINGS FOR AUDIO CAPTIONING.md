Author(s): [[Daiki Takeuchi]], [[Yuma Koizumi]], [[Yasunori Ohishi]], [[Noboru Harada]], [[Kunio Kashino]]
Tags: #academic_papers, #Automated_Audio_Captioning, #dcase2020_task6
Read on: [[May 11th 2021]]
URL: https://arxiv.org/abs/2009.11436
# Main Contribution(s)
Problem: how to augmented limited data, how to decide the best description for given audio, and if post-processing such as beam search is effective in [[Automated Audio Captioning|AAC]]
Solution: Uses a pipeline of models for predition
# Summary
![[Pasted image 20210511141918.png]]
They find that:
1. Data Augmentation and Post-processing significantly improved the performance of [[Automated Audio Captioning|AAC]]
2. [[Multi-task Learning]] did not improve performance, but it did with pretrained models
3. [[Mixup]] was effective for [[Audio Tagging]]
4. [[Beam Search]] was effective for [[Automated Audio Captioning|AAC]] and any other text generation task like [[Image Captioning]].
# Learning Gaps/Thoughts
Not a fan of the architecture
# Simplify/Analogies