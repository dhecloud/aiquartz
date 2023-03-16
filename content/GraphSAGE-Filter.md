Uses a pipeline to aggregate information
$$N_s(v_i) = \text{SAMPLE}(N(v_i),S)$$$$f^\prime_{N_{S{(v_i)}}} = \text{AGGREGATE}(\{F_j, \forall v_j \in N_S(v_i) \})$$ $$F^\prime_i = \sigma([F_i ,f^\prime_{N_{s(v_i)}}])  \Theta$$
There are several aggregator functions, such as element-wise mean, [[LSTM]], [[Pooling]].