Speaker(s): [[Amit Sharma]], [[Susan Athey]], [[Elias Bareinboim]], [[Cheng Zhang]]
Tags: #seminar
Held on: [[July 21st, 2020]]
URL: [event page](https://www.m2icrosoft.com/en-us/research/event/frontiers-in-machine-learning-2020/#!tuesday-july-21), [youtube](https://www.youtube.com/watch?v=wYVptiGkmQM&feature=emb_logo)
- [[Amit Sharma]]: You need causality for building robust out-of-domain models
- Talk 1: Causal Inference, Consumer Choice, and the Value of Data, by [[Susan Athey]]
- Two Big Challenges for Estimation of Counterfactuals
- Prediction vs Causal Inference
- Statistical Power  
- Approach Matrix Factorization and Nested Logits
- Conclusions
- Counterfactual inference differs from prediction
- Evaluate value of personalized targeting, how it varies with alternative data sizes
- Talk 2: On the Causal Foundations of AI (Explainability and Decision-Making), by [[Elias Bareinboim]]
- Definition: A [[structural causal model]] is a tuple $$(V, U, F, P(u))$$ where $$V$$ are endogenous variables, $$U$$ are exogenous variables, $$F$$ are functions determining V, and $$P(u)$$ is a distribution over $$u$$
- [[Pearl Causal Hierarchy]]
- Level 1: Associational $$P(y|x)$$. [[Bayes Network]], [[Decision Trees]], [[Subject Vector Machines]],
- Level 2: Interventional $$P(y | do(x), c)$$. [[Reinforcement Learning]]
- Level 3: Counterfactual $$P(y_x|x', y')$$. Imagining, Retrospection
- Why is the causal problem "non-trivial"?
- [[structural causal model]]s are almost never observed
- Conclusions:
- Causal Inference and AI are fundamentally intertwined and novel learning opportunities emerge when this connection is fully understood
- Failure to acknowledge distinct features of causality almost always lead to poor decision-making and superficial types of explanations
- Talk 3: A Causal View on Robustness of Neural Networks, by [[Cheng Zhang]]
- Humans are good at causal reasoning, ie we can discern properties that cause a prediction. Models not so.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F0Tkp0xi4CC.png?alt=media&token=973e42a6-5c34-4dfc-9ff9-49ef4330d043) [[Deep Causal Manipulation Augmented Model]] is a [[Variational Auto-Encoder]] to generate data which is more robust
