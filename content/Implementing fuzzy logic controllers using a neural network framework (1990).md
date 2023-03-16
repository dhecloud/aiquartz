Author(s): [[Ronald R. Yager]]
Tags: #Fuzzy_Logic, #academic_papers
Read on: [[September 23rd, 2020]]
URL: https://www.sciencedirect.com/science/article/abs/pii/S0165011499800098
# Main Contribution(s)
- Implements [[Fuzzy Logic Controllers]] using [[Neural Network]]s
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F5t3s3BzRjJ.png?alt=media&token=6f60f91c-830a-437f-a0af-c51117f2716d)
![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FCaDGO5pWVq.png?alt=media&token=e7a97616-1c43-43b0-b32f-735554196c51)
[[Fuzzy Logic Controllers]] takes in specific settings and readings and outputs a specific crisp value. The fuzzy values and relationships are completely contained inside the fuzzy controller itself. The fuzzy logic controller can be made up of a Control rules and inference mechanism and a defuzzier unit
- The first block takes the input and provides an output $$D$$ which is a ==fuzzy subset==
- The second block takes the fuzzy values $$D$$ and converts them to crisp values
#  Membership Neural Module
#  ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FvAf7Xg3Vqn.png?alt=media&token=2019dae5-20e8-42dd-967a-70f5fb200201) ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F7H4-CsCfR3.png?alt=media&token=397add56-af4f-4297-996c-a86dd5a2b9e4)

- There are **two approaches**
- the functional link type (standard mathematical functions like sin, cos ie Fourier series estimation)
- neural network type. 
- Both give similar approximations for $$F$$, but functional type learns a lot faster.
- This is the ==first part== of the [[Fuzzy Logic Controllers]] which expresses the rule. 
- The membership neural module takes a value and outputs the membership grade $$F(x)$$. $$F$$ is a general function sketched by an expert and an subset of $$X$$ is selected by the system designer
#  Inverse Membership Neural Module
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FiX1j_d0f7L.png?alt=media&token=6ff8165e-58f1-4fe7-aa17-04cf07fef7e4) 
The inverse membership neural model takes a membership grade number and provides the level set in terms of its end point. The inverse membership neural model is used to output a range $$[a,b]$$. We can obtain $$D^{-1}$$ by using $$D$$ to give us values to create a subset of membership grades which can be used to generate a curve which can be used to train $$D^{-1}$$ 
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fz9KpJYHv7Y.png?alt=media&token=d655e7d8-6ed9-4ee0-ab30-c4dc68915327)
The second way to train $$D^{-1}$$ is to take the output of $$D(x)$$ and train via back-propagation.
- This is used to output each rule as a range $$[a,b]$$ (by design).
#  Rule Neural module
#  ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FZL5Pge6XNs.png?alt=media&token=58f3d37f-68e6-49ab-a746-4b583e193ad1) ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FfarRZDFOV9.png?alt=media&token=9fe1dbc2-5181-4313-9db7-676ee83e58b3)![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FF3ImKfaeNV.png?alt=media&token=bb192949-a506-4c5e-9452-beb4a4f2cd7e)
- $$V_n$$ is from the controller's sensors. 
            1. These values are sent to the "Membership Neural Module" of the rule which outputs $$A_j(V_j)$$ which are then sent to the combiner module. 
            2. The output of the combiner module is then sent to the  FJcU-Dm8O to provide an output as a range $$[b,a]$$. 
            3. ==The grand output of this module is a triple containing the outputs of the combiner module, and the 2 output of the ((FJcU-Dm8O))==. These triple(s), depending on number of rules, goes into the defuzzier
- The knowledge base is a collection of rules modules.
- Consists of a combiner module, which can be a simple $$min(\alpha)$$ function or a $$\prod(\alpha)$$. They are referred to as 'anding' nets
#  Action Selection/Deffuzzifier Unit
#   ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FNYGTikR7SO.png?alt=media&token=4f4c488f-037e-426f-a45b-4ea5257711a8)
- The output of the "Rule Neural module" becomes the input to this defuzzifier unit. The output of the defuzzifier unit becomes the input to the plant
- The weights $$\alpha$$ are initialized to be equal to 1 and modified according to a generalized delta rule.
# Learning Gaps/Thoughts
-
# Simplify/Analogies
- Modular fuzzy logic network for controllers.
