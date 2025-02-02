Speaker(s): [[Susan Dumais]], [[Katja Hofmann]], [[Akshay Krishnamurthy]], [[Asli Celikyilmaz]], [[Dan Klein]]
Tags: #seminar
Held on: [[July 20th, 2020]]
URL: [event page](https://www.microsoft.com/en-us/research/event/frontiers-in-machine-learning-2020/#!monday-july-20), [youtube](https://www.youtube.com/watch?v=aLSmjr0fQtQ&feature=emb_logo)
- Talk 1: Learning to Adapt: Advances in Deep Meta Reinforcement Learning, by [[Katja Hofmann]]
- **Frontier**: Rapid Adaptation to New Scenarios and Players __given limited data__
- Previous success: reinforcement in imitation learning in [[MineRL competition]]
- Agents can efficiently learn complex task, but cannot adapt to new tasks
- [[Meta Reinforcement Learning]]
- Key idea: "learn to learn" new tasks in simulation, **learn to rapidly adapt to real new tasks**
- Approach: [[Variational Deep Reinforcement Learning (VariBad)]]
- Talk 2: Generalization and Exploration in Reinforcement Learning, by [[Akshay Krishnamurthy]]
- [[Reinforcement Learning]] is a sequential decision making setting in which an agent interacts with an environment to optimize some sort of long term reward function
- Applied to gaming, robotics, dialogue, where the algorithm uses raw sensory information
- Gaming is most popular as it is a **high fidelity simulation** and **sample inefficiency** is not a concern
- **Problem**: ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FuSW6Jt-4Vm.png?alt=media&token=b023a927-e61f-4f02-9217-97c1035479e8)
- Relatively underdeveloped area
- [[Representation learning]] to encode information about the environment into a latent space
- proven in [[Homer]] and [[FLAMBE]]
- Talk 3: Modeling Discourse in Long-Text Generation, by [[Asli Celikyilmaz]]
- [[Conditional Language Modelling]] has issues like [[exposure bias]], compounding errors, [[bottleneck issues]] like large vocabulary, surrogate objective function ([[cross entropy]] is used for training, but evaluated on other metrics like [[BLEU]], [[ROUGE]])
- Introduce **discourse markers** to [[GPT-2]] to indicate stylistic preference when generating new paragraph
- Open questions in long text generation:
- Text generations requires commonsense reasoning, how can we better learn commonsense information?
- Intrinsic Issues with long text generation with [[Casual Language Modelling]]. How to better manage knowledge? shared/multitask training?
- Is decoding process correct? How similar to humans
- Evaluation metric/process is crucial! 
- Talk 4: Conversational AI: A view from Semantic Machines, by [[Dan Klein]] (focus is on [[Task Oriented Dialogue Systems]])
- Standard Approach: Intents and Slots to indicate intention. Does not do well when more context/information is needed to complete a request
- Idea 1: Dialogs are programs (program synthesis)
- Problem: Combinatorial problems are often solved with enumeration, when it should be broken down instead
- Idea 2: Complex tasks are built from simpler ones (compositionality)
- Idea 3: Meanings depend on context (metacomputation)
- Memory and commonsense from previous states is often needed for queries 
- Idea 4: Things will go wrong (exception handling)
- Idea 5: Systems should tell the truth (dynamic generation)
- Panel discussion
- [[Akshay Krishnamurthy]]: much of [[Reinforcement Learning]] is still theoretical, no exact way to perform [[cross validation]] like in other facets of machine learning
- [[Asli Celikyilmaz]]: If there is a need to constrain generation it is possible to incorporate some sort of knowledge graph
- I was thinking that she was going to say finetune further on the target domain!
- New ideas for PHD students in 30 seconds:
- [[Akshay Krishnamurthy]]: For [[Reinforcement Learning]], find a problem and try to model and understand the structures that are present in that real problem and design algorithms to capture those structures
- [[Asli Celikyilmaz]]: Focus on methods where evaluation is the key. Explainability to determine why a model generates something. Ethical issues and research
- [[Dan Klein]]: Grounding. Modularity. Data
- [[Katja Hofmann]]: Think about the kinds of applications that you would like to enable and what is missing in the current research direction.
