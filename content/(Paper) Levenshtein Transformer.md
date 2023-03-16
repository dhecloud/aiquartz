Author(s): [[Jiatao Gu]], [[Changhan Wang]], [[Jake Zhao Junbo]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #Sequence_Refinement, #academic_papers
Read on: [[August 23rd, 2020]]
URL: https://arxiv.org/abs/1905.11006
# Main Contribution(s)
- Proposes the [[Levenshtein Transformer (Architecture)]] which uses two operations: insertion and deletion
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FuwrXh-0Re3.png?alt=media&token=f33a7e78-6d62-4330-973d-9d7d41c2b3fc)
- [[Levenshtein Transformer (Architecture)]]
		- Trained using [[Imitation Learning]] and has two policies executed in an alternate manner
- The task is cast as a [[Markov Decision Process]] defined by $$(Y,A,E,R,y_o)$$
- $$Y$$ - set of discrete sequences
- $$A$$ - set of actions to perform on $$y$$
- $$R$$ - reward function. in this case, the [[Levenshtein Distance]]
- Policies
- Deletion - Binary decision on each token to delete or keep
- Insertion: 2 phrases
    - Placeholder prediction - possibility of adding 1 or more placeholders between slots.
    - Token prediction - predicts on every possible placeholder.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F8L_CtZsZ3z.png?alt=media&token=00bf2366-0c62-4feb-8892-67cf5c85e0e5)
[[Roll-in Policy]] to
- Learning to Delete
- Learning to Insert
- Inference
- Greedy decoding is done.
- [[Noisy Parallel Decoding (NPD)]] does not yield much gain, as opposed to what has been observed.
- Termination conditions
- 2 consecutive refinement iterations return the same output
- Timeout: Maximum number of iterations reached
- Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F3LPHRr004P.png?alt=media&token=ca467ee6-3bbf-4db6-9a7b-a33db9065528)
 trained on [[WMT16 Ro-En]], [[WMT14 En-De]], [[WAT2017 Small-NMT En-Ja]]. Did not specify train test split
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fe3eyJevogR.png?alt=media&token=a188aa81-e601-4955-b332-d78b1833b173)
 [[WMT17 Automatic Post-Editing (APE) Task En-De]]
# Learning Gaps/Thoughts
- Reinforcement policy jargon is still uncharted territory for me
# Simplify/Analogies
- Uses [[Levenshtein Distance]] as a policy during training to influence how similar the generated sequence is.
