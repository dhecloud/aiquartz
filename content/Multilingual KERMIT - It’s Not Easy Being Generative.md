Author(s): [[Harris Chan]], [[Jamie Kiros]], [[William Chan]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[August 21st, 2020]]
URL: https://pgr-workshop.github.io/img/PGR027.pdf
# Main Contribution(s)
- Applies the [KERMIT]([[Kontextuell Encoder Representations Made by Insertion Transformations (KERMIT)]]) to multilingual data, the [[Multi30k]] dataset
- Demonstrates unconditional multilingual generation using the joint [KERMIT]([[Kontextuell Encoder Representations Made by Insertion Transformations (KERMIT)]]) model
# Summary
- [[Multi30k]]
- 29000 parallel training sentences in English, French, Czech, German
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F5xbszH_wPy.png?alt=media&token=56531379-4278-410d-a319-e833507f7180)Trains [KERMIT]([[Kontextuell Encoder Representations Made by Insertion Transformations (KERMIT)]]) in bilingual, multi-target, joint settings.
- Evaluates using 2 metrics, [[BLEU]] (quality) and [[Self-BLEU]] (diversity/repetition)
- Lower [[Self-BLEU]] means higher diversity aka less repetition 
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FDDiD8hykGq.png?alt=media&token=c11f2c1f-647e-4bd7-b3d2-a37c8f418648)
A singlue multitarget  [KERMIT]([[Kontextuell Encoder Representations Made by Insertion Transformations (KERMIT)]]) model could apparently outperform specialized bilingual  [KERMIT]([[Kontextuell Encoder Representations Made by Insertion Transformations (KERMIT)]]) models.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F0x6A9cTWg3.png?alt=media&token=9672afb8-8c82-452d-9843-4a08542ca328)
Also tries unconditional language generation where a sequence contains 4 sub-sequence for one language each
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fn0bTEMwYYI.png?alt=media&token=4a264005-cf19-4954-bb76-79a6ae7f4213)
# Learning Gaps/Thoughts
- Interesting to see how refutes this [paper]([[UNDERSTANDING KNOWLEDGE DISTILLATION IN NON-AUTOREGRESSIVE MACHINE TRANSLATION]]) where they said that having a smaller number of modes (or languages) would help [[Non-Autoregressive]] models do better.
- The unconditional language generation part is interesting as well, but i cant really get an intuition of how good the model is since i dont understand any of the languages 
# Simplify/Analogies
- Applying an NAT to multilingual data.
