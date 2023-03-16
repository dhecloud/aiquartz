Author(s): [[L.G. Kraft]]
Tags: #academic_papers, #Cerebellar_Model_Articulation_Controller_(CMAC)
Read on: [[November 2nd, 2020]]
URL: https://ieeexplore.ieee.org/document/203399
# Main Contribution(s)
- Compares 2 architectures using the [CMAC]([[Cerebellar Model Articulation Controller (CMAC)]]) neural network
# Summary
- First method learns the inverse model of the system being controlled
- The second method uses the system tracking error to adjust network weights
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FzXm7D82n8f.png?alt=media&token=f89d8391-7291-4bd2-a5fd-b8319cce25aa)
 The error driven control structures seemed to provide better tracking performance based on the rms tracking error
- The network weights are modified according to $$m_{ij}(k+1) = m_{ij}(k) + B*[u(k)-m_{ij}(k)]$$
# Learning Gaps/Thoughts
- Cant seem to find explanations about the direct inverse method
# Simplify/Analogies
