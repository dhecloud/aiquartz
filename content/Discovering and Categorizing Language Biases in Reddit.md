Author(s):
Tags: #critique, #academic_papers, #bias
Read on: [[August 12th, 2020]]
URL: http://arxiv.org/abs/2008.02754
# Main Contribution(s)
- Uses static embeddings like [[word2vec]] to discover language biases in subreddits
# Summary
    Identify and categorize gender bias in r/TheRedPill, r/dating_advice, religion biases in r/atheism, and ethnicity biases in r/The_Donald
    skip-gram model of 200 dimensions is trained, then clustered using [[K-means clustering]]
- The clusters are assigned labels which are either positive or negative
    ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FFNMhHwxEUo.png?alt=media&token=57c9de88-aabb-481c-bed2-2e64c30f379e)
Most female-biased words are more frequently used than male-biased words
    ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FuEYuRn7pWD.png?alt=media&token=4454bb8e-a8a6-42f0-94e8-60c028b46c7a)
Bias distribution is weaker than r/TheRedPill. More significant negative bias towards men
    ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F9leEOpCnDx.png?alt=media&token=145390d3-fa3e-42ef-994a-96207dc79f8d)
All labels are negatively biased towards Islam, except for Geographical names. On the other hand, most words in Christianity-based clusters do not carry negative connotations.
    ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FvrSRcEZ4oy.png?alt=media&token=446a2118-23c2-441c-9125-b151e904249b) Most interesting labels for Hispanic are General ethnics, Crime, law and order, General appearance and physical properties. Crime, law order are not found at all.

# Learning Gaps/Thoughts
- Authors removed "non-interesting words" like acronyms, which i disagree with, since there are many derogatory acronyms used to insult people.
- Interesting to find out how the results will be for contextual embeddings
# Simplify/Analogies
-
