Author(s): [[Xuenan Xu]], [[Heinrich Dinkel]], [[Mengyue Wu]], [[Kai Yu]]
Tags: #academic_papers, #Automated_Audio_Captioning 
Read on: [[February 14th 2021]]
URL: https://arxiv.org/abs/1905.13448
# Main Contribution(s)
Uses a encoder-decoder model with a sentence level loss for [[Automated Audio Captioning]] **in a car setting**
# Summary
Uses the previously utilized GRU encoder-decoder model.
The setence level loss refers to [[Pooling]] the hidden states of all timesteps to get a single representation of the prediction. Then this sentence level loss is calculated by the difference in representation between the output embedding and the embedding of the annoted sentences.
# Learning Gaps/Thoughts
Gave me an idea about using reconstruction loss
# Simplify/Analogies