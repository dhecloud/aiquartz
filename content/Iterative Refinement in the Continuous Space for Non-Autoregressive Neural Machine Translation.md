Author(s): [[Jason Lee]], [[Raphael Shu]], [[Kyunghyun Cho]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #Iterative_Refinement, #academic_papers
Read on: [[September 18th, 2020]]
URL: https://arxiv.org/abs/2009.07177
# Main Contribution(s)
- Proposes an efficient inference procedure for non-autoregressive machine translation that iteratively refines translation purely in the continuous (embedding) space.
# Summary
- Most models perform refinement in the discrete token space. Some perform refinement in a hybrid space, using a mixture of continuous latent variables and discrete token. 
- This work focuses on refinement in the continuous space
- Given the latent variable model, we want to find the marginal log probability of the most likely target sentence.
- There are two ways to parameterize the training objective
- using an [[Energy]] function, which is done by averaging the last hidden states across time and feeding it to a linear layer to yield a scalar energy value
- or using a score function which directly outputs the gradient of the log probability with respect to the hidden states
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FMqWaEnvlBF.png?alt=media&token=f1130239-f4bd-4a0d-a094-2db64a59b4e7) 
Results on [[WMT14 En-De]], [[WMT16 Ro-En]], [[IWSLT16 De-En]]
- Possible 6.2x speedup over the autoregressive basline with minimal degradation to translation quality
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FK7aa-Am0aZ.png?alt=media&token=a28d6818-6404-4c18-8bf2-e5dcef1ac7d0)
- Seems like there isnt really a problem of repetitive words in the original translation before refinement
# Learning Gaps/Thoughts
- Trained for 1million steps, which is a lot
- Not familiar with [[Energy]]
# Simplify/Analogies
-
