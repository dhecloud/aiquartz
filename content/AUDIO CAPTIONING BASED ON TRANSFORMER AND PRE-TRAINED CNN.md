Author(s): [[Yusong Wu]], [[Kun Chen]], [[Ziyue Wang]], [[Xuan Zhang]], [[Fudong Nian]], [[Shengchen Li]], [[Xi Shao]]
Tags: #academic_papers, #Automated_Audio_Captioning 
Read on: [[February 14th 2021]]
URL: http://dcase.community/documents/challenge2020/technical_reports/DCASE2020_Wu_136_t6.pdf
# Main Contribution(s)
Proposes a new architecture for [[Automated Audio Captioning]]
# Summary
Uses a [[Convolution Neural Network|CNN]] for encoder, and 2 layer [[Transformer]] decoder for decoder.

Introduces a pretraining classification task, training to train the whole model, and fine-tuning pineline where only the decoder is frozen.
![[Pasted image 20210214211646.png]][[BLEU]] on [[Clotho dataset]]
# Learning Gaps/Thoughts
Just a new pipeline and architecture
# Simplify/Analogies