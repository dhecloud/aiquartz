Author(s): [[Ho-Hsiang Wu]], [[Magdalena Fuentes]], [[Juan P. Bello]]
Tags: #academic_papers, #audio_tagging,
Read on: [[08-Jun-2021]]
URL: [\[2106.01149\] Exploring modality-agnostic representations for music classification (arxiv.org)](https://arxiv.org/abs/2106.01149)
# Main Contribution(s)
Problem: Systems thus far exclusively focus on single modality recognition
Solution: Learn joint representations from different modalities when they represent the same concepts
# Summary
Authors investigate the use of pre-trained audio and image embeddings in combination with training translation models to obtain a joint representation, in a self-supervised setting. Translation models refers to learning a shared embedding space between modes. 

The model is trained to perform cross-modal retrieval. Their idea is that emebddings should be close to each other in the joint emebdding space.
![[Pasted image 20210608021113.png]] Translation scores pretty well, but fails to keep up when enough data from both modalities is available. 

![[Pasted image 20210608021240.png]] Interestingly, the pairwise distance between the centroids of each classes show that translation is bringing together audio and image embeddings. however, there are blocks where some classes that should not be brought together were brought together. The author hypothesize that this is becayse of the bias of label distribution
# Learning Gaps/Thoughts
Pairwise distance analysis was pretty interesting
# Simplify/Analogies