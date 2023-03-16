Author(s): [[Francisco J. Gonzalez-Serrano]], [[Aníbal R. Figueiras-Vidal]] , [[Antonio Artés Rodríguez]]
Tags: #Cerebellar_Model_Articulation_Controller_(CMAC), #academic_papers
Read on: [[November 2nd, 2020]]
URL: https://ieeexplore.ieee.org/document/728400
# Main Contribution(s)
- Proposes a [[Generalized CMAC (GCMAC)]] network that considers different degrees of generalization for each input.
# Summary
- [[Cerebellar Model Articulation Controller (CMAC)]] can represent a set of functions in a bounded, connected and discrete space. However, it has difficulties representing functions that are products of its input variables, or functions that contain edges in certain directions.
-  ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F1v5GwE9-Kj.png?alt=media&token=e9281e0e-ccc4-4d91-8803-45f13b1e8236)
            1. The input variables first has to be discretized, which allows for a finite number of elements in the interger lattice. 
            2. The input space are divided into square regions by the linear manifolds. 
            3. The given input x activates $$\rho$$ basis functions
            4. The output of these basis functions are arranged into an activation vector $$a(x)$$ 
            5. The output is then computed according to $$f_{CMAC}(x) = a^T(x)w$$
    - Once this process finishes, only the scalar $$\rho$$ controls the representation and generalization capabilities, which varies from function to function.
- [[Generalized CMAC (GCMAC)]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fbe_FxeD9CX.png?alt=media&token=e73f1aec-a833-404b-84da-cb13d8b19452)
Replaces the generalization scalar with a generalization vector. The number of available basis functions is thus given by ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FXGkci70V6_.png?alt=media&token=b1fcf06e-9f1e-41af-b5b4-4fcc85413dde) and the output is given by ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FcO82c4G9q-.png?alt=media&token=57754751-1d8b-4f7a-8199-1ac18c10c0fb)
- The network structure is determined by 3 parameters: 1) the generalization vector, 2) the displacement vector 3) the basis functions
- The generalization vector determines how much these regions expands
- The displacement vector determines the positions of the regions
- Growth
            1. Initialization of new structure from the old one. The weights of the old network can set up the new ones by splitting the old networks into smaller domains
            2. Modification of the Generalization parameter by reducing the appropriate components of the initial generalization vector.
- Comparisons
- The number of basis functions of a [[Generalized CMAC (GCMAC)]] is less or equal to the number of basis function of a [[Cerebellar Model Articulation Controller (CMAC)]] having a generalization parameter equal to $$\rho_{min}$$ and greater or equal to the number of basis functions of a [[Cerebellar Model Articulation Controller (CMAC)]] network having a generalization parameter equal to $$\rho_{max}$$
- The [[Generalized CMAC (GCMAC)]] is computed using $$\rho_{max}$$ basis functions, and hence is equivalent to a [[Cerebellar Model Articulation Controller (CMAC)]] with a generalization parameter equal to $$\rho_{max}$$
- Both [[Generalized CMAC (GCMAC)]] and [[Cerebellar Model Articulation Controller (CMAC)]] can be trained using the same training procedures
- The [[Generalized CMAC (GCMAC)]] is similar, not necessarily higher, to the complexity of its equivalent [[Cerebellar Model Articulation Controller (CMAC)]].
# Learning Gaps/Thoughts
# Simplify/Analogies
