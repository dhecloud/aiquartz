Author(s): [[Jean-Bastien Grill]], [[Florian Strub]], [[Florent Altche]], [[Corentin Tallec]], [[Pierre H. Richemond]], [[Elena Buchatskaya]], [[Carl Doersch]], [[Bernado Avila Pires]], [[Zhaohan Daniel Guo]], [[Mohammad Gheshlaghi Azar]], [[Bilal Piot]], [[Koray Kavukcuoglu]], [[Remi Munos]], [[Michal Valko]]
Tags: #academic_papers
Read on: [[01-Jun-2021]]
URL: [\[2006.07733\] Bootstrap your own latent: A new approach to self-supervised Learning (arxiv.org)](https://arxiv.org/abs/2006.07733?fileGuid=WyYwxqq8kWjKdWgd)
# Main Contribution(s)
Problem: [[Contrastive Loss]] depends on careful treatment of negative pairs, either by relying on large batch sizes, memory banks, or customized mining strategies to select the negative sample.
Solution: Propose [[Bootstrap Your Own Latent]] which is mroe robust to the choice of image augmentation than contrastive methods
# Summary
![[Pasted image 20210601200612.png]][[Bootstrap Your Own Latent|BYOL]]'s goal is to learn a representation that can be used for downstream tasks. It makes use of two networks:
1. Online Network. Consists of an encoder, projector and predictor
2. Target Network. Same architecture as the online network but its parameters are an **exponential moving average** of the online parameters.

### Ablations
 ![[Pasted image 20210601201840.png]]
* Batch size: [[Bootstrap Your Own Latent]] remains stable over a wide range of batch sizes
* Image Augmentation: [[Bootstrap Your Own Latent|BYOL]] works well even when augmentation is removed
* Bootstrapping: There is a trade-off between updating the targets too often and updating them too slowly.
# Learning Gaps/Thoughts
# Simplify/Analogies