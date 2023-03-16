Author(s): [[Lam Pham]], [[Ian McLoughlin]], [[Huy Phan]], [[Ramaswamy Palaniappan]]
Tags: #academic_papers, #audio_tagging 
Read on: [[31-May-2021]]
URL: [\[2002.04502\] Robust Acoustic Scene Classification using a Multi-Spectrogram Encoder-Decoder Framework (arxiv.org)](https://arxiv.org/abs/2002.04502)
# Main Contribution(s)
Problem: Distinct features do not appear in different types of scenes, hence the model does not do well when these features are absent
Solution: Use 3 different types of front-end time freqeuncy features: [[Gammatone]], [[Constant-Q-transform]], [[Mel Spectrograms]]
# Summary
3 types of spectrogram, [[Gammatone]], [[Constant-Q-transform]], [[Mel Spectrograms]], is used along with [[Mixup]]. Idea is each type contains different information. [[Gammatone]] is inspired by cochlea activation response of the human inner ear, [[Mel Spectrograms]] simulates the overall frequency selectivity of the human auditory system, and [[Constant-Q-transform]] is based on the geometric relationship of pitch, which is useful when comparing natural and artifical sounds.

![[Pasted image 20210531205255.png]] Concatenation of the 3 features performed the best single model wise
# Learning Gaps/Thoughts
# Simplify/Analogies