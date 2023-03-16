Author(s): [[Shawn Hershey]], [[Daniel P W Ellis]], [[Eduardo Fonseca]], [[Aren Jansen]], [[Caroline Liu]], [[R Channing Moore]], [[Manoj Plakal]]
Tags: #academic_papers, #audio_tagging 
Read on: [[07-Jun-2021]]
URL: [\[2105.07031\] The Benefit Of Temporally-Strong Labels In Audio Event Classification (arxiv.org)](https://arxiv.org/abs/2105.07031)
# Main Contribution(s)
Problem: Audio data are temporally imprecise - annotator indicates if a sound even is present within a 10 sec clip. This is very vague
Solution: Collects a 81k precise annotations which makes up 4% of the 1.8million training clips from [[AudioSet]]
# Summary
Authors release strong positive and explicit negatives for 356 of the original 527 [[AudioSet]] classes, excluding the music subclasses and other are classes.

1. Training of the weak 1.8 million examples substationally improves over training on the Strong 67k examples alone.
2. However when pretrained on the weak 1.8M and then fine-tuned on a mixture of weak and strong, we get the best results
# Learning Gaps/Thoughts
# Simplify/Analogies