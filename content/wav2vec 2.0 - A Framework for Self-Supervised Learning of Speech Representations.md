Author(s): [[Alexei Baevski]], [[Henry Zhou]], [[Abdelrahman Mohamed]], [[Michael Auli]]
Tags: #academic_papers, #self_supervised_learning
Read on: [[April 27th 2021]]
URL: https://arxiv.org/abs/2006.11477
# Main Contribution(s)
Problem: Speech recognition systems require thousands of hours of transcribed speech to reach acceptable performance. This is not available for nearly 7000 languages spoken worldwide
Proposes a framework for [[Self-Supervised Learning]], similiar to [[Masked Language Modelling]].
# Summary
### Model
![[Pasted image 20210427161627.png]]
1. **Feature encoder**: Temporal convolution followed by layer norm and GELU activation function. This is meant to act as a relative [[Positional Encodings]].
2. **Contextualized representations**: The transformer architecture is used.
3. **Quantization module**: discretize the output of the feature encoder to a finite set of speech representation via [[Product Quantization]].

### Training
A proportion of the ==feature encoder outputs== are masked before passing to the transformer. The model is trained to solve a constrastive task which is to identify the true quantized latent speech representation for a masked time step within a set of distractors. Distrastors are uniformly sampled from other masked time steps of the same utterance. 

The [[LibriSpeech]] corpus without transcriptions, and the audio data from [[LibriVox]] is used for pretraining
### Finetuning
CTC loss is used to fine-tune after training on [[Phoneme Recoginition]] on the [[TIMIT dataset]]

### Ablations
![[Pasted image 20210427174600.png]]
Continuous inputs with quantized targets performs the best. Continuous targets reduce the effectiveness of self-supervised  training as targets can capture detailed artifacts of the current sequence.

# Learning Gaps/Thoughts
# Simplify/Analogies