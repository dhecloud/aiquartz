Author(s): [[Tom B. Brown]], [[Benjamin Mann]], [[Nick Ryder]], [[Melanie Subbiah]], [[Jared Kaplan]], [[Prafulla Dhariwal]], [[Arvind Neelakantan]], [[Pranav Shyam]], [[Girish Sastry]], [[Amanda Askell]], [[Sandhini Agarwal]], [[Ariel Herbert-Voss]], [[Gretchen Krueger]], [[Tom Henighan]], [[Rewon Child]], [[Aditya Ramesh]], [[Daniel M. Ziegler]], [[Jeffrey Wu]], [[Clemens Winter]], [[Christopher Hesse]], [[Mark Chen]], [[Eric Sigler]], [[Mateusz Litwin]], [[Scott Gray]], [[Benjamin Chess]], [[Jack Clark]], [[Christopher Berner]], [[Sam McCandlish]], [[Alec Radford]], [[Ilya Sutskever]], [[Dario Amodei]]
Tags: #language_model, #meta-learning, #GPT-3, #academic_papers
Read on: [[June 3rd, 2020]]
URL: https://arxiv.org/abs/2005.14165
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FPvhlyf49oH.png?alt=media&token=93173d89-3b3f-4e9a-9873-998d54d25eff)
- [[GPT-3]], the latest iteration of [[GPT-2]], follows the same architecture as [[GPT-2]] but with a lot more parameters and trained a lot more data. This aim of this paper is to compare the performance of [[GPT-3]] in various settings: **zero shot, one shot, and multi-shot.**
- As noted in the paper, there were bugs in the filtering process to remove test data from training data.
- ## Language Modeling, Cloze, Completion Tasks
#  [[LAMBADA]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FBLyHjGgiZo.png?alt=media&token=4030ada4-74c1-4060-a203-81f27ff72f1e)
- Lambada is formulated as a cloze task where the model has to fill in the last word of a paragraph.
- Few Shot: Performance improves strongly with model size
- One Shot: Not effective, performs worse than zero shot.
- Overlap of training and testing data, but analysis suggests negligible impact.
#  Closed book QA
- There has been research that a large LM can perform well directly answering the questions without conditioning on auxiliary information.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FbbgQZMut1p.png?alt=media&token=d025ba59-87ab-47b8-b8d8-fba29f350333)
- Results on [[TriviaQA]]
- Performance scales very smoothly with model sizes, suggesting increasing capacity to encode knowledge in parameters (like in T5)
- ## Translation
- [[GPT-3]] training data consist of 93% English, 7% foreign language content
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FlbCF20-EyK.png?alt=media&token=39ae3522-8d1a-43eb-b78f-e1c0d30230bc)
- Results on [[WMT14 Fr-En]], [[WMT14 En-Fr]], [[WMT16 De-En]], [[WMT16 En-De]], [[WMT16 Ro-En]], [[WMT16 En-Ro]]
- Zero shot performs badly. Single shot performs near competitive performance, and few shots is competitive.
- There is a noticeable skew in performance; does well when translating to english, but badly in the other direction.
- As noted in the paper, this could be because the byte-level BPE tokenizer of [[GPT-2]] which was almost entirely in English was reused for [[GPT-3]].
- ## Winograde-Style Tasks
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FeQOVwBy0LR.png?alt=media&token=1fc8d659-73bb-4c1e-9863-10c3856bbff9)
- Results on both [[Winograd]] and [[Winogrande]]
- For all shot settings GPT-3 performs similarly, demonstrating no in-context learning
- For the [[Winogrande]] dataset, there is in-context learning and performance does improve with more examples
- ## Commonsense reasoning
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FtcUMD8n7tk.png?alt=media&token=29e38b1c-b151-4b1b-8c20-42141b488531)
- [[PIQA]] (Physical QA) shows relatively shallow scaling with model size, but still outperforms SOTA. [[ARC]] (3rd-9th grade science exams) perform very badly, which might suggest that GPT-3 is still bad at understanding jargon, scientific terms and prefer layman English more.
- ## Reading Comprehension
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FKD4n4frEZh.png?alt=media&token=f8324e96-cd63-49a4-99f7-d1f3a9099e89)
- Results on [[CoQA]], [[DROP]], [[QuAC]], [[SQuADv2]], [[RACE]]
- GPT-3 is generally still unable to exceed SOTA, but performance does come close on the CoQA dataset. For the others those, there is catastrophic performance drop.
- The performance variability could be due to the answer formats.,
- ## SuperGLUE
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fp0aWi80Gw5.png?alt=media&token=39ca3fe8-13c0-439e-9ee7-2467d637e3e1)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FeU1UfOH4EH.png?alt=media&token=3e6bb432-dc4d-440c-a0a2-ae560dc4bc3b)
- Results on [[SuperGLUE Benchmark]]
- Another benchmark where GPT-3 performs inconsistently. [[WiC]] (Word in Context) is a notable weak spot. GPT-3 seems to be bad at settings where it needs to decide if the same word mean the same thing in two sentences or snippets.
- ## Natural Language Inference
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FyF2Xqr4xqd.png?alt=media&token=2f98399e-c1a7-4751-bfd8-f427046f9561)
- Results on [[ANLI]]
- GPT-3 performs very badly, suggesting that NLI is still a very difficult task for language models. It is worrying that the 175B model in few shot settings performed a lot better, which might entice openAI to build an even bigger model.
- ## Synthetic and Qualitative Tasks
- Tests for ability to do symbolic reasoning, arithmetic.
# # Arithmetic
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FCMhFbLzCMU.png?alt=media&token=0d4c8cf0-4e98-4041-9038-32bdbc0d167e)
- GPT-3 displays strong proficiency on small digits; 100% on 2 digit addition, 98.9% on 2 digit subtraction, 80.2% at 3 digit addition, 94.2% at 3 digit subtraction.
- However, it does not do as well on 4 and more digits; 25-26% on 4 digit operations, 9-10% on 5 digit operations.
- On single digit combined operations, GPT-2 has a performance of 21.3%
- One-shot and zero shot are degraded compared to few-shot, suggesting that adaption is essential to performing these computation correctly.
- Mistakes makes were often like not carrying a '1', **suggesting that computation is actually attempted and just not done in a look up table.**
# # News Article Generation
- Humans abilities to detect model generated text decrease as model size increases. Humans also spend more time considering each text as the model size increases.
# # Learning and Using Novel Words
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FR-5EHO3UsW.png?alt=media&token=045df80d-81b2-4b9b-95ab-2643e43ef378)
- It can generate a pretty good sentence containing the new word. However, the paper notes that GPT-3 appears to be the least proficient at the task.
# # Correcting English Grammar
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FJHT_G1nk2c.png?alt=media&token=d0799148-32ec-4828-93f4-0ae2ed72183d)
- GPT-3 does pretty well.
- ## Limitations
- GPT-3 seems to have special difficulty with common sense physics.
- Authors note that a large bidirectional model would be stronger at fine-tuning than GPT-3. The approach to GPT-3 is 'meta-learning' as in zero to few shot learning as opposed determining fine-tuning performance like in BERT.
- Pretraining objective weighs every token equally → lacks notion of what is most important to predict.
- Promising directions to tackle this: RL, multimodal, function from humans.
- Poor sample efficiency during pre-training
- GPT-3 sees more text than a human in his lifetime.
- Needs a lot of data to work better.
- Uncertainty if GPT-3 learns new tasks from scratch at inference time, or simply recognizes tasks learnt during training.
- Inconvenient and expensive to perform inference on
- Not easily interpretable decisions; high variance of performance compared to humans
