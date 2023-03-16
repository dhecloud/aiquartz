Author(s): [[Anna Rogers]], [[Olga Kovaleva]], [[Anna Rumshisky]]
Tags: #academic_papers, #critique, #BERT 
Read on: [[January 12th 2021]]
URL: https://arxiv.org/abs/2002.12327
# Main Contribution(s)
Provides a comprehensive overview on [[BERT]] and the different approaches and tasks done on [[BERT]]
# Summary
## Introduction
[[Transformer]]s have little cognitive motivation, unlike [[Convolution Neural Network|CNN]]s, and the size of these models limits us from experimenting with pre-trianing and performing ablation studies.
## What knowledge does BERT have?
1. [[BERT]] representations are hierarchical rather than linear; like a [[Syntax Tree]] 
2. Encode information about [[Part of Speech]], [[Syntax Tree]]s and syntax roles.
3. Syntactic structure is not directly encoded in self-attention weights, but can be recovered from token representations.
4. Learns some syntactic information, although it is not very similar to linguistic annotated resources
5. Takes [[Subject-Predicate Agreement]] into account when performing the [[Cloze Task]].
6. Able to detect the presence of NPIs and the words that allow their use than scope violations
7. Does not understand negative and is insensitive to malformed input. This could mean that either [[BERT]] syntactic knowledge is incomplete, or it does not rely on it for solving its tasks.
8. Has some knolwedge about semantic roles, and even displays preference for the incorrect fillers for semantic roles that are semantically related to the correct ones ie chooses the "more correct answer"
9. Struggles with representation of numbers
10. Brittle to [[Named Entity]] replacements
11. Struggles with pragmatic inference and role-based event knowledge, as well as visual and perceptual properties that are likely to be assuemd rather than mentioned ie [[Tacit Knowledge]]
12. For some relation types, Vanilla [[BERT]] is competitive with methods relying on knowledge bases
13. Cannot reason based on its world knowledge

These observations are done via [[Probing]] studies. Different methods may lead to complementary or even contradictory conclusions, which makes a single test insufficient or biased. [[Amnesic Probing]] and [[Information-Theoretic Probing]] are two main directions.

## Localizing Linguistic Knowledge
1. Distilled contextualized Embeddings into static embeddings better encode lexical semantic information. This is done by aggregating the information across multiple contexts
2. [[Isotropy]] is an interesting direction which shows to benefit static word embeddings. They also find that [[BERT]] [[Embeddings]] occupy a narrow cone in the vector space; and this effect increases from the earlier to later layers.
3. [[BERT]]'s contextual embeddings form distinct clusters corresponding to word senses, making it perfect for [[Word Sense Disambiguation]]
    * However, the representation of the same word depends on the position of the sentence in which it occurs, likely due to the [[Next Sentence Prediction]] task. This is not desirable from a linguistic point of view.
4. Heads in [[Multi-Head Self-Attention]] seem to specialize in certain types of syntatic relations.
5. No single head has the complete [[Syntax Tree]] information.
6. It is argued that attention weights are weak indicators of [[Subject-Verb Agreement]] and [[Reflexive Anaphora]].
    * Yet [[self-attention]] is extremely popular due to the ease of visualization and the idea that it has a clear meaning -> high weight for a particular word.
7. Most heads in [[Multi-Head Self-Attention]] do not directly encode any non-trivial linguistic information, at least when fine-tuned on [[GLUE Benchmark]].
    *   `[CLS]` and `[SEP]` tokens typically do not get much attention, but heads in early layers attend more to `[CLS]`, middle layers to `[SEP]`, and final layers to periods and commas.
    *   Interesting after fine-tuning, `[SEP]` gets a lot of love, depending on the task.
8. Lower layers have the most information about linear word order
9. Syntactic information is most prominent in the middle layers of [[BERT]]
10. Conflicting evidence about syntactic chunks, due to different probing tasks
11. Final layers are most task-specific
12. Semantics is spread across the entire model

## Training [[BERT]]
1. Number of heads was not as signficant as number of layers
2. Chanes in number of heads and layers appear to perform difference functions, namely about information flow. Initial layers seem to be the most task invariant, and tokens resemble the input tokens the most.
    * By this intuition, a deeper model has more capacity to encode information that is not task-specific
3. Large batch training shows improvements in training time with no performance drawback
4. Model training can be done in a recursive manner via a 'warm start'
5. Multiple training tasks, such as playing around with [[Masked Language Modelling]] to fit spans, whole words, and other [[Denoising]] objectives such as deletion, infilling, permutation and document rotation.
6. Removing [[Next Sentence Prediction]] does not hurt or slightly improves performance.
7. Some research has tried explicitly incorporating explicit linguistic information, or structured knowledge via a knowledge base completion task.
8. **However, the current consensus is that pre-training does help in most situations, but the degree and its exact contribution requries further investigation**
9. Several studies has tried exploring the possibilities of improving the fine-tuning of [[BERT]], such as taking more layers into account for prediction, two stage fine-tuning, adversarial token perturbations, adversarial regularization, [[Mixout]] regularization

## How big should [[BERT]] be?
[[BERT]]-base was 110M parameters, [[Turing-NLG]] was 17B, [[GPT-3]] is now 175B. This raises questions about computational complexity and the future of mdoels
1. All of a few [[Transformer]] heads could be pruned without significant losses in performance.
    * Head disabiling also resulted in improvement for [[Neural Machine Translation|NMT]], [[Abstractive Summarization]], and [[GLUE Benchmark]].
2. [[BERT]]-large models generally perform better, but not always. For example, [[BERT]]-base outperformed large on [[Subject-Verb Agreement]], [[Sentence Subject Detection]].
    * It is not clear why there are redundant heads and layers given the complexity and size of the training data.
3. [[Knowledge Distillation]] is often used for compression
4. [[Quantization]] decreases memory footprint by lowering precision of its weights
5. [[Pruning]] reduces computation by zeroing out parts of the large model.
6. If the goal of training large models is to compress, it is recommended to train larger models then compress them heavily, rather than compressing small models lightly.

## Directions for further research
[[BERT]] seems to rely on shallow heuristics in [[Natural Language Inference]], [[Reading Comprehension]], [[Text Classification]]. Harder [[datasets]] need to be created which is not solvable by shallow heuristics.

Methods to teach reasoning, such as quantification, conditionals, comparatives, boolean coordination.

Learning what happens at inference time is also important. Directions such as [[Amnesic Probing]] and [[Pruning]] allow us to further understand how the model derives its answer.
# Learning Gaps/Thoughts
# Simplify/Analogies