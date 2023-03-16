Author(s): [[Huy Phan]], [[Oliver Y. Chen]], [[Philipp Koch]], [[Lam Pham]], [[Ian McLoughlin]], [[Alfred Mertins]], [[Maarten De Vos]]
Tags: #academic_papers, #audio_tagging 
Read on: [[May 18th 2021]]
URL: https://arxiv.org/abs/1811.01095
# Main Contribution(s)
Problem: Common length snippets are often used in the literature, but different characteristics of audio scenes allow certain scenes to be recognized earlier than others
Solution: Determine which scenes can be reliably recognized in a few seconds, and which scenes require significantly longer durations. 
# Summary
They ran a suite of experiments using [[Convolution Neural Network|CNN]]s and [[Recurrent Neural Networks|RNNs]] on different audio segments.
![[Pasted image 20210518142905.png]] [[Accuracy]] and [[F1 score]] on the [[LITIS-Rouen dataset]].
### When is model fusion useful?
They find that model fusion works the best when test signal is small, <20 seconds

### What is the appropriate length of time to recognize a scene?
Several categories can be reliably recgonized even with a very short signal length. For example, “avion”, “kidgame”, and “poolhall” can be recognized within 4, 12, and 16 seconds. Some other scenes, such as “car”, “metro-rouen”, “restaurant”, “train-ter”, and “train-tgv”, can also be recognized reliably within 16 seconds. In contrast, scenes such as “cafe”, “quitestreet”, “ruepietonne”, and “shop” require much longer test signal lenghts (e.g. 30 seconds) to achieve good performance.
# Learning Gaps/Thoughts
# Simplify/Analogies