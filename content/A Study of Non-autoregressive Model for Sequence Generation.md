Author(s): [[Yi Ren]], [[Jinglin Liu]], [[Xu Tan]], [[Zhou Zhao]], [[Sheng Zhao]], [[Tie-Yan Liu]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #Automatic_Speech_Recognition, #Text_to_Speech, #academic_papers
Read on: [[August 25th, 2020]]
URL: https://arxiv.org/abs/2004.10454
# Main Contribution(s)
- Introduces [[Conditional Masked prediction with Mixed-Attention (coMMA)]], to measure the target-token dependency
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F-ZpoWi8n6j.png?alt=media&token=536dcb4b-06d2-4276-a841-0ea50d8b52b0)
 [[Conditional Masked prediction with Mixed-Attention (coMMA)]]
		- Differences from the original [[Transformer]]
- Some tokens are randomly replaced by a special mask token with probability p
- Employ mix-attention mechanism
- Add Source/target embedding, and position embedding
- The target token dependency is measured by averaging the attention density ratio over all predicted tokens.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F5m1OJvuCDD.png?alt=media&token=3b7cf99b-5042-4acf-be0a-28c324eaec72)
 Apparently, NMT performs better because it is learning from source context when less context information is available from the target
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F-OOvmVCZ_h.png?alt=media&token=66030014-7a52-4305-aa47-216d0f45e299)
 Apparently, knowledge distillation works because it reduces the dependency on target context.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FCL7u6TtGmg.png?alt=media&token=1783924c-d7b1-41a7-baac-f57bf707be48)
 Apparently, an alignment constraint reduces the attention density and dependency on the target context
# Learning Gaps/Thoughts
- Basis of whole paper is based on the "attention density" idea, which the authors did not really prove to me its legitimacy
- Also they conveniently left out ASR in the knowledge distillation study   
# Simplify/Analogies
-
