Author(s): [[Kai Keng Ang]], [[Chai Quek]]
Tags: #Cerebellar_Model_Articulation_Controller_(CMAC), #academic_papers
Read on: [[November 8th, 2020]]
URL: https://www.semanticscholar.org/paper/Improved-MCMAC-with-momentum%2C-neighborhood%2C-and-Ang-Quek/4156678b6386c35e7bed3019fa082bf572d1f83a
# Main Contribution(s)
- Improves the learning algorithm of the [[Modified CMAC (MCMAC) (Architecture)]]
# Summary
- [[Modified CMAC (MCMAC) (Architecture)]] is similar to [[Cerebellar Model Articulation Controller (CMAC)]], except that the quantized closed loop error are the indices to the memory array.
- The [[Modified CMAC (MCMAC) (Architecture)]] learns using closed loop error and plant output, rather than the plant input and output.
- Uses momentum by adding a fraction of the previous weight change to the current weight chance
- Neighbourhood learning is used to distribute the learnt information of the winning neuron to neighbouring neurons.
- The average trapezoidal output is used to improve cell recall without increasing the number of cells.
# Learning Gaps/Thoughts
# Simplify/Analogies
