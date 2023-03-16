### [[mixup - BEYOND EMPIRICAL RISK MINIMIZATION]]
Done by

$$
\tilde{x} = \lambda x_i + (1-\lambda)x_j
$$
$$
\tilde{y} = \lambda y_i + (1-\lambda)y_j
$$

where $x_i,x_j$ are random raw input vectors and $y_i, y_j$ are one hot label encodings, both taken from training data