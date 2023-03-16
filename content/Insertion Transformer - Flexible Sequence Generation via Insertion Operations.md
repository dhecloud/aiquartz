Author(s): [[Mitchell Stern]], [[William Chan]], [[Jamie Kiros]], [[Jakob Uszkoreit]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[August 18th, 2020]]
URL: https://arxiv.org/abs/1902.03249
# Main Contribution(s)
- Introduces the [[Insertion Transformer]] which allows for a [[Binary Tree]] traversal form of generation.  
# Summary
- [[Insertion Transformer]]
- Only insertions and no reordering operations, so every generation must be a sub-sequence of the final output
- Remove causal [[self-attention]] mask
- Uses n+1 vectors for slot representation by adding a special marker token at the beginning and the end of the decoder input to extend the sequence length by 2. Then concatenate each adjacent pair to get n+1 slots representation.
- To model the content location distribution, they either model the joint distribution or use a factorization
- They also introduce a [[Mixture of Softmaxes]] output layer to try to circumvent the [[Softmax]] bottleneck
- Maximizes parallelism by using a balanced binary tree ordering
- Generation is terminated by
- Slot finalization: when all slots predict an end of slot
- Sequence finalization: Generate entire sequence over empty spans
- Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FYX8w7q0DVw.png?alt=media&token=4024c831-a1d6-4338-9330-7831217c016e)
![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FLwtSRciHah.png?alt=media&token=fcb17378-5b46-4250-860f-f7d7a01fe86d)
![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FN-JJHoUTCG.png?alt=media&token=e0b79afa-14f4-4190-a545-253fea11ba23)
Results on [[WMT14 En-De]] for training, [[newstest2013 En-De]] for development, and [[newstest2014 En-De]] for testing
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FYXj24Uz5XA.png?alt=media&token=6c2e0e8b-2066-4af3-ad33-45296a589d14)
# Learning Gaps/Thoughts
# Simplify/Analogies
