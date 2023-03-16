Author(s): [[Ayşegül Özkaya Eren]], [[Mustafa Sert]]
Tags: #academic_papers
Read on: [[February 14th 2021]]
URL: https://ieeexplore.ieee.org/document/9327916
# Main Contribution(s)
Uses a pretrained audio neural network as a feature extractor.
# Summary
![[Pasted image 20210214213107.png]]
Encoder takes in audio embeddings (Wavegram-Logmel-CNN14), subject-verb embeddings which are preprocessed via the Stanford Parser, then fed through a trained [[Feed-forward]] network, and partial captions (from decoding).

Decoder uses GRU.

![[Pasted image 20210214214146.png]] [[BLEU]] on [[Clotho dataset]] and [[AudioCaps]]
# Learning Gaps/Thoughts
# Simplify/Analogies