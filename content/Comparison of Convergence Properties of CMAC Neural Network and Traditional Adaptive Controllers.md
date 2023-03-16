Author(s): [[L.G. Kraft]], [[David P. Campagna]]
Tags: #Cerebellar_Model_Articulation_Controller_(CMAC), #academic_papers
Read on: [[November 2nd, 2020]]
URL: https://ieeexplore.ieee.org/document/70450
# Main Contribution(s)
- Compares the the [[Self-Tuning Regulator]], [[Lyapunov Model Reference (MRAC)]], and the [[Cerebellar Model Articulation Controller (CMAC)]] [[Neural Network]] method.
# Summary
- [[Self-Tuning Regulator]] is a classical feedback system with adjustable coefficients. [[Least Squares]] used to determine estimates of the parameters of the unknown system
- Convergence depends heavily on the [[Least Squares]] error. Stability is not guaranteed.
- Able to learn unknown system quickly and function well. But depended on large system inputs and did not perform well for non-linear plants
- [[Lyapunov Model Reference (MRAC)]] are designed so that the output of the plant follows the output of a desired model.
- Guaranteed stability for linear systems with sufficiently rich inputs.
- Rate of adaption is not predictable but can be used (as a hyperparameter)
- Slow to converge and sensitive to noise
- [[Cerebellar Model Articulation Controller (CMAC)]] approximates the system input-output characteristics and uses this information for feedforward control.
- Can be unstable when performing the network weight update algorithms.
- Needs small control signals and insensitive to noise, but slower to learn. Performed well when plant is non-linear 
# Learning Gaps/Thoughts
# Simplify/Analogies
