### [[Receptive Field Regularization Techniques for Audio Classification and Tagging with Deep Convolutional Neural Networks]]

$$RF_n = RF_{n-1} + (k_n -1) \cdot S_n$$
$$S_n = S_n-1 \cdot s_n$$
where $s_n$, $k_n$ are stride and kernal size of layer $n$, and $S_n$ is the cumulative stride from layer $n$ to the input layer
