Author(s): [[Ciprian Chelba]], [[Mia Chen]], [[Ankur Bapna]], [[Noam Shazeer]]
Tags: #Decoding, #Natural_Language_Generation, #academic_papers
Read on: [[May 26th, 2020]]
URL: https://arxiv.org/abs/2001.04589
# Main Contribution(s)
- Truncates the attention mask for the target side window for a 2-3x speed up
# ELI5
- When we write a sentence, we only focus at a few words before the current word, and not the whole sentence. So we don't need the whole sentence for prediction
# Summary
- Truncates the target-side window used for computing self attention by making an N-gram assumption ie only the previous N-1 tokens will be used for prediction
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FFsnxaAUU-H.png?alt=media&token=01f660fd-3313-49bb-b253-3e5752997a81)
- Results on [[WMT14 En-Fr]], [[WMT18 En-De]]
- At around 6-gram, the results is comparable to the baseline, but it is interesting to note that it never surpasses it.
# Learning Gaps
- None
# Simplify/Analogies
- Basically we only focus on the local context, so that we do not have to compute attention on the whole sequence.
