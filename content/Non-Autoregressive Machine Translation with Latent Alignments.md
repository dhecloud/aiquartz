Author(s): [[Chitwan Saharia]], [[William Chan]], [[Saurabh Saxena]], [[Mohammad Norouzi]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[August 14th, 2020]]
URL: https://arxiv.org/abs/2004.07437
# Main Contribution(s)
- Applies [[Latent Alignment Models]] like [[Connectionist Temporal Classification (CTC)]] and [[Imputer]] to non-autoregressive machine translation.
# Summary
- [[Latent Alignment Models]]
- An alignment is a mapping between a source sequence and a target sequence
- Can be constructed by infilling a special blank token over the target sequence to match the source sequence length
- Do not generate the target sequence directly, but instead generates the alignment then collapsing the target sequence 
- Do not require target length prediction (as this is implicitly done through alignments)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F8vrvtCa-Jo.png?alt=media&token=8494146b-5da4-41b5-8ca2-24a3f20d6aca)
[[Connectionist Temporal Classification (CTC)]]
- Models alignment distribution with strong conditional independence assumptions between tokens
- Uses an efficient [[Dynamic Programming]] algorithm to exactly marginalize the latent alignment
- Generates alignment in a single generation step
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FoePmL-pG-c.png?alt=media&token=3bfed10f-8009-4f2b-9570-b66ed9a8a33b)
[[Imputer]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Ft3fIR4PC9m.png?alt=media&token=7f375412-4378-4e0b-9295-5e3635dbc7c3)
Iterative generative model needing only a constant number of generation steps
- Solved using [[Dynamic Programming]]
#   Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FBEvaSwYDOk.png?alt=media&token=2065469d-20c9-460f-8b08-d861dd1e51a8)
Results on [[WMT14 En-De]], [[WMT14 De-En]], [[WMT16 Ro-En]], [[WMT16 En-Ro]]
- Beats(28.2) the original autoregressive transformer (27.8) using 8 decoding iterations. With $$O(n)$$ deocoding, 28.3 [[BLEU]] score, exceeding original performance by 0.5 
- Observes a significantly lower rate of token repetition
# Learning Gaps/Thoughts
- Not very familiar with [[Dynamic Programming]]
- Seems like training with distilled data always leads to surpassing the original state of the art
# Simplify/Analogies
- Applies popular [[Speech Recognition]] models to [[Non-Autoregressive]] [[Neural Machine Translation]]
