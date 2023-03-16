Author(s): [[Su Lin Blodgett]], [[Solon Barocas]], [[Hal Daumé III]], [[Hanna Wallach]]
Tags: #bias, #critique, #academic_papers
Read on: [[May 30th, 2020]]
URL: https://arxiv.org/abs/2005.14050
# Main Contribution(s)
- Survey 146 papers analyzing bias, and finds motivations vague inconsistent, and lacking in normative reasoning.
- Proposes 3 recommendations to guide work analyzing 'bias'
# ELI5
- Different papers use different criteria to judge different models for bias. Authors also don't use expertise from other fields which are more informed about bias
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F3amdaP-gyM.png?alt=media&token=a8f2cf9a-70eb-484b-a83e-e3d95bfbbc76)
- Bias are often not explicitly expressed and defined in papers. Different people often have different definitions of bias, be it social, racial, demographic. Different authors also check for bias in different things, embeddings, conference resolution, etc.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FHdFMsIAF7-.png?alt=media&token=2aad9921-a727-485b-b898-dd953cc6a038)
- The authors of this paper thus recategorize the 146 papers into a previously developed taxonomy of harms by Barocas et al and Crawford et al as shown in table 2.
- ### Motivations
- Papers state a wide range of motivations, multiple motivations, vague motivations, and sometimes no motivations at all. This makes it hard to discern how an NLP system 'discriminates', what are 'systematic biases', or how NLP systems contribute to 'social injustice' (from the example in the paper)
- Papers usually include no normative reasoning. Authors usually focus on system performances and corelates it with bias
- Even when papers do state clear motivations, they are often unclear about why the 'biased' system behaviors described are harmful **in what ways, and to whom.**
- Papers about NLP systems developed for the same task often conceptualize 'bias' differently.
- Papers conflate allocational and representation harms (lump them into one category). They also use imagined downstream effects to justify focusing on particular system behaviors, even when said downstream behavior are not measured. This is prevalent in 'embeddings' papers
- ### Techniques
- Papers do not refer to relevant literature outside NLP, staying within only computational science.
- Papers' techniques are poorly matches to their motivations. Wrong solutions for different types of bias
- Papers focus on a narrow range of potential source of bias ie most papers focus on bias in data. However there are other sources of bias like development and deployment lifecycle.
- ### Recommendations
- Use ground work analyzing 'bias' in NLP systems in the relevant literature outside of NLP. Treat representational harms as harmful in their own right
- Computer scientists are ill equipped to deal with this field, and risk measuring only what is convenient to measure
- Provide and define explicitly reasons, assumptions of behaviors, in what ways and to whom.
- Many authors assume that descriptions and definitions of bias are self evident, but this is not the case
- Examine language use by engaging with lived experiences of members of communities
# Learning Gaps
- None
# Simplify/Analogies
- Basically, future authors who want to write a paper about bias should properly use research from relevant fields, and clearly define terms, biases, notions.
