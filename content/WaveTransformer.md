### [[WaveTransformer - A Novel Architecture for Audio Captioning Based on Learning Temporal and Time-Frequency Information]]
![[Pasted image 20210209171421.png]]
Encoder consists of three learnable processes $E_{temp}(\cdot)$, $E_{tf}(\cdot)$, $E_{merge}(\cdot)$.

"Wave-blocks" are used to learn $E_{temp}(\cdot)$, and consists of 7 1D [[Convolution Neural Network|CNN]], kernel size 3, padding and dilation 2, stride 1. This is based on the [[WaveNet]] architecture. All [[Convolution Neural Network|CNN]]s operates along the time dimension.

$E_{tf}(\cdot)$ uses "2DCNN-blocks", consisting of 2D [[Convolution Neural Network|CNN]]s, a [[LeakyReLU]], and a 2D [[Convolution Neural Network|CNN]]. These blocks arm to learn spatial time-frequency information

$E_{merge}(\cdot)$ consists of a 2D [[Convolution Neural Network|CNN]], and a [[Feed-forward]] network. 

The Decoder is the decoder of the [[Transformer]].
