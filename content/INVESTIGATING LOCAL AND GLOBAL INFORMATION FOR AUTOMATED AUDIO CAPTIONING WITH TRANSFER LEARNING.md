Author(s): [[Xuenan Xu]], [[Heinrich Dinkel]]
Tags: #academic_papers, #Automated_Audio_Captioning 
Read on: [[May 3rd 2021]]
URL: https://arxiv.org/abs/2102.11474
# Main Contribution(s)
Problem: Encoder has to learn all concepts for audio captioning 
Solution: proposes to use two source tasks to train for audio captioning
# Summary
Proposes to use [[Audio Tagging]], and [[Acoustic Scene Classification]] which can help the model learn local audio topic and global audio topics

![[Pasted image 20210503164559.png]]
They used a CNN10 for audio encoder and [[Gated Recurrent Unit]] for text decoder.

![[Pasted image 20210503164636.png]] Results on [[AudioCaps]] and [[Clotho dataset]]
# Learning Gaps/Thoughts
# Simplify/Analogies