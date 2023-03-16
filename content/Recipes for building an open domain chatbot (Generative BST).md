Author(s): [[Stephen Roller]], [[Emily Dinan]], [[Naman Goyal]], [[Da Ju]], [[Mary Williamson]], [[Yinhan Liu]], [[Jing Xu]], [[Myle Ott]], [[Kurt Shuster]], [[Eric Michael Smith]], [[Y-Lan Boureau]], [[Jason Weston]]
Tags: #Conversational_Dialogue_Systems, #academic_papers, #Dialogue_Modelling, #Facebook_AI_Research
Read on: [[June 23rd, 2020]]
URL: https://arxiv.org/abs/2004.13637
Models: http://parl.ai/projects/recipes
# Main Contribution(s)
- Show that large scale models can learn good conversational skills when given appropriate training data and choice of generation strategy.
- Show that small models using [[Blended Skill Talk]] can match or outperform larger models that do not.
- Show that choice of decoding algorithm is of critical importance.
- Introduce Generative BST of 3 parameter sizes: 90M, 2.7B, 9.4B
# Summary
- Conversational models still display:
    - A lack of in-depth knowledge
    - Tendency to stick to simpler language
    - Tedency to repeat often used phrases
- ## Models architectures
    - ### 1. Retriever
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FLtQ-tvOOTh.png?alt=media&token=f5154a68-fb2a-4c83-b034-3e2d13881b78)
            - Encodes global features of the context using multiple representations
    - ### 2. Generator
        - Standard seq2seq [[Transformer]]
        - 3 sizes: 90M, 2.7B, 9.4B
    - ### 3. Retrieve and Refine
        - Try to combine a retrieval step before generation to try to alleviate the problems mentioned {{[[embed]]: ((jdH--jIoo))}}
        - Try to use a retrieval-based model in "1. Retriever" to perform dialogue retrieval and knowledge retrieval
- ## Training Objectives
    - Minimize cross-entropy loss, and use other responses in the batch for negatives
    - Standard MLE approach for generation
    - For Retrieve and Refine, use `α-blending` to use the retrieved utterance instead of the gold label 
    - [[Unlikelihood Training]] for generation to help fix mismatches between human and model distributions. Effects: decrease repetition, mitigate issue of underrepresented vocabulary tokens
- ## Decoding
    - Beam Search
        - Generating with a beam tends to produce short generations that ==do not match the length of human utterances==
            - Force a minimum length
            - Predict the length using and 4-class classifier and binning them
    - Top-k sampling
    - [[Sample-and-Rank]] 
    - Subsequence blocking of `n=3`
- ## Training details
    - Used [[Fairseq]] for pretraining, [[ParlAI]] for fine-tuning
    - [[Adafactor]] allowed for larger batch sizes, but converged worse than [[Adam]]
- ## Training Data
    - Pre-training
        - **pushshift.io Reddit** with many filters/condition. Of note:
            - Longer than 128 BPE tokens or 2048 characters removed
    - Fine-tuning
        - [[Conversational Intelligence Challenge 2]] - dataset helps provide more **engaging **dialogue
        - [[Empathetic Dialogues]] - To introduce more **empathy **in data
        - [[Wizard of Wikipedia]] - Goal to engage partner as well as display expert **knowledge**
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FXogUGFYaT5.png?alt=media&token=02dcf799-6836-483d-a7ff-8faec0746afc)[[Blended Skill Talk]] - Blend the above 3 tasks
- ## Safety Characteristics
    - Toxic or biased language from human-human data
        - Use classifier at test time to check for toxic language, but not infallible
- ## Evaluation Methods
    - [ACUTE-eval]([[ACUTE-EVAL - Improved Dialogue Evaluation with Optimized Questions and Multi-turn Comparisons]]), both self-chat and human-machine
- ## Results and Analysis
    - ### Automatic Evaluations
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fa4SbWOclZk.png?alt=media&token=21a848a8-84e3-4130-abd2-369f04659066) Retriever
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FRnNr-saj_Z.png?alt=media&token=96d370fb-c24a-4766-97cf-4b8de34ecfa8) ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FLhJtndjtml.png?alt=media&token=a5ceedde-6986-44c3-9255-201f9ddb1395) Generator. Note that 2.7B and 9.4B parameters models are not directly comparable to that of the 90M parameter model due to an unshared dictionary
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fi87-A3aWmH.png?alt=media&token=115ef9ac-f101-477f-8f36-df37b70c37d7)Retrieve and Refine. Small increase in perplexity relative to the standard generator model. Cannot rely on automatic evaluations alone to assess the relative performance
    - ### Self-chat Evaluations
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F696OpJenUg.png?alt=media&token=b503a977-323e-4bd2-93cd-388ffd1264a0)Retrieve And Refine outperforms the pure generation approach, but with retrieval outperforming both. **In order for generation methods to do better, we need to improve their recipe**
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FyITv5z-gC6.png?alt=media&token=5bd35c6f-fbd1-434c-9cd0-1a9330591037) Both methods improve significantly. For all future experiments, ==minimum beam length of 20 BPE tokens==
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FKZmH1f0JUc.png?alt=media&token=6abf0d1a-bb6e-4b34-9b1f-fc09c1b43bb3)Larger model indicates improvement at the cost of increased computational resources being required
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FRIOR4Jc4y5.png?alt=media&token=a6ceaaed-a5c2-442f-a7e0-8c11af106673)Large improvements from the [[Blended Skill Talk]] fine-tuning
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Ff6tnYTEBtJ.png?alt=media&token=a5be73b5-d03c-4e5f-91a4-607d5d633ef6) Small win for employing personas
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FR3Q3q_Q9bW.png?alt=media&token=8f35bfea-75b1-4697-8d61-79ee29fce253)[[Unlikelihood Training]] does have the intended effect of making generation less dull. Effect would likely be larger with longer or repeated sentences. Small gain against likelihood model, both not statistically significant 
    - ### Human-Bot Chat Evaluations
        - 100 conversations per model via crowdworkers
        - Comparison to [[Meena]]
            - Meena generally tends to fare better at the humaness question than the engagingness question
            - With the generation length constraint of 20, Generative BST 2.6B has average response length of around 21 tokens. Meena has 10.4 and humans in human-human chats is 18.0
                - However, humans speaking to models will often match response length 
    - ### Failure cases
        - 1. Vocabulary usage is too common, rare words used too infrequently
        - 2. Nontrivial Repetition - Agreeing because it is easier to do so.
        - 3. Contradiction and Forgetfulness - Occasionally contradict themselves, with larger models occurring less
        - 4. Knowledge and Factual correctness - tend to hallucinate knowledge, or using knowledge when not needed
        - 5. Conversation Length and memory - evaluation done by very short one-shot conversations. Hard limit of 128 BPE tokens also limits how much the model is able to elaborate
        - 6. Deeper Understanding. Not totally able to understand puns
    - ==**The 9.4B model does not have a clear win in human evaluations over our 2.7B model, despite having lower perplexity**==
        - Indicating limiting factor not being model size anymore? Time to focus on data, optimizers, decoding strategies?
# Learning Gaps
- The "3. Retrieve and Refine" part, haven't read their paper
- [[Sample-and-Rank]]
# Simplify/Analogies
- Trains models on conversational data, which is able to have strong coherency when conversing
- Limitations as noted in {{[[embed]]: ((ZBaROBfEN))}}
- Hard to evaluate for longer conversations due to time, manpower and computational constraints
