Author(s): [[An Tran]], [[Konstantinos Drossos]], [[Tuomas Virtanen]]
Tags: #academic_papers, #Automated_Audio_Captioning
Read on: [[February 9th 2021]]
URL: https://arxiv.org/abs/2010.11098
# Main Contribution(s)
Proposes the [[WaveTransformer]] for [[Automated Audio Captioning]]
# Summary
[[Recurrent Neural Networks|RNNs]] have difficulties learning temporal information
2D-[[Convolution Neural Network|CNN]]s model time-frequency but not temporal patterns
The [[Transformer]] was not originally designed for sequences of thousand time steps.

Authors argue that combining two types of information:
1. Time-frequency information
2. High-level information on the time dimension captured by 1D dilated convolutions

![[WaveTransformer#WaveTransformer - A Novel Architecture for Audio Captioning Based on Learning Temporal and Time-Frequency Information]]
The parameters of the encoder and decoder is jointly optimized via the [[cross entropy]] loss between the target and generated sequence.

![[Pasted image 20210209172837.png]][[Clotho dataset]] is used for [[BLEU]] evaluation. Greedy decoding stops when token or when 22 words are generated.
# Learning Gaps/Thoughts
The information "learnt" in the encoder is debetable, since there is no loss function to ensure that the encoder is forced to learn those types of information.

# Simplify/Analogies
Makes uses of Time-frequency information and High-level information on the time dimension to aid in decoding.