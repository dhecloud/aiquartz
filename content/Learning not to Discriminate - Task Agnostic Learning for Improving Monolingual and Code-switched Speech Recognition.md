Author(s): [[Gurunath Reddy Madhumani]], [[Sanket Shah]], [[Basil Abraham]], [[Vikas Joshi]], [[Sunayana Sitaram]]
Tags: #Code-switching, #Speech_Recognition, #Adversarial_Learning, #academic_papers
Read on: [[June 17th, 2020]]
URL: https://arxiv.org/abs/2006.05257
# Main Contribution(s)
- Propose strategies for fine-tuning and regularization code-switched speech on monolingual models
# Summary
- If monolingual and code-switched data are both available and a model can be retrained from scratch, regularization strategies and fine-tuning a pooled model that uses all data leads to best results across sets
- If only a monolingual model is available, and a new model cannot be retrained from scratch, the [[Learning Without Forgetting]] framework can be used to improve performance on all test sets compared to a monolingual model fine-tuned on code-switched data
#  Experimental Setup
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FOMmxV3b96f.png?alt=media&token=e70e0cf9-a192-4c5a-9d4e-c77016f772e6)
- Data: Tamil, Telugu, Gujarati
- [[Code Mixing Index (CMI)]] measures amount of code-switching in a corpus by using word frequences
- Baseline model: 2 [[Convolution Neural Network]] layers followed by 5 [[BiLSTM]] of size 1024
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FygWFLkwGwA.png?alt=media&token=5a003fda-7619-4aaf-b171-3a9c1d78a341)
- The Gradient Reversal layer acts as an identity transformer and reverses ($$ \times -1$$) the gradients during backpropagation
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F_O6s-313uX.png?alt=media&token=8b948404-7758-4a87-9ea4-02cee633896f)
- The [[Word Error Rate (WER)]] for the multi-task adversarial speech recognition model performed the best
# Learning Gaps
- Honestly, since i didn't read the previous paper that the author referenced a lot, most of the paper went over my head.
- However, the Gradient Reversal Layer is quite an interesting idea 
# Simplify/Analogies
- It is better to use a pooled model for code-switching tasks over fine-tuning on a model (**not going to link this since i am not fully confident of the accuracy of this statement from my limited understanding**)
