Author(s): [[Lam Pham]], [[Ian McLoughlin]], [[Huy Phan]], [[R. Palaniappan]], [[Alfred Mertins]]
Tags: #academic_papers, #audio_tagging 
Read on: [[31-May-2021]]
URL: https://www.researchgate.net/publication/339228084_Deep_Feature_Embedding_and_Hierarchical_Classification_for_Audio_Scene_Classification
# Main Contribution(s)
Problem: Audio is often complicated by presence of foreground sounds and interfereing noise
Solution: Deep feature embedding learning and a hierarchical classification scheme
# Summary
![[Pasted image 20210531154728.png]]Uses a two-level Hierarchical Classification approach, where a more general category is first predicted
[[KL-divergence]] is used to train the data together with [[Mixup]]. [[Triplet Loss]] is also used to minimize the distance between positive samples and minimize negative samples

In general, meta-categories can be discriminated very well with average accuracy of 94. [[Gammatone]] seems to perform the best, while [[Constant-Q-transform]] is the worst.
# Learning Gaps/Thoughts
Another [[Scaffolding]] approach
# Simplify/Analogies