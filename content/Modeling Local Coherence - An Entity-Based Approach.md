Author(s): [[Regina Barzilay]], [[Mirella Lapata]]
Tags: #academic_papers, #Machine_Learning, #Features
Read on: [[July 6th, 2020]]
URL: https://people.csail.mit.edu/regina/my_papers/coherence.pdf
# Main Contribution(s)
- Propose a novel framework, the [[Entity Grid]] for representation and measuring local coherence
# Summary
- Another type of feature extraction which relies on a little bit of dependency parsing (subject verb object)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F8aXn9HiuRg.png?alt=media&token=732bde3c-81b1-4f36-b1f2-fdabf5629d94)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F-Yn4yG8kyY.png?alt=media&token=525c1e53-8fa7-4a40-a429-d73041f86000)
- Creates a sparse matrix, with their grid cells corresponding to grammatical roles: subjects (s), objects (o), or neither (x) 
- There is a simplified version of the matrix with only present (x) and not present (-)
- This allows us to encode a sequence with entity occurrences like a one-hot vector. 
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FXzOfn3An_E.png?alt=media&token=da5e3869-b75d-42d0-bebf-1804146b5a46) We can also compute the probabilities of transitions by calculating the number of transitions of that type/total number of transitions of length
- but this doesn't scale well as the data size increases?
# Learning Gaps
- Almost all the older methods and datasets
# Simplify/Analogies
