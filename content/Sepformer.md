### [[ATTENTION IS ALL YOU NEED IN SPEECH SEPARATION]]
![[Pasted image 20220205000313.png]]
![[Pasted image 20220205000323.png]]
![[Pasted image 20220205000444.png]]The encoder is basically a convolutional layer to learn the [[Short-Time Fourier Transform]] representation of the time input
The masking network predicts the mask for each speaker (for reconstruction)
The sepformer block is just a transformer block
And the decoder is just a transposed convolutional layer to reconstruct the speeches