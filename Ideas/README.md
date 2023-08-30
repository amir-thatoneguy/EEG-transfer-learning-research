## The little theorem of RBF kernel transfer learning:
An adaptive RBF kernel with parameter $\lambda$ is equivalent to adding a single feature $\lambda' = \sqrt{-\log(\lambda)}$ to the target data and a 0 feature to the source data.

Proof:
$$k(y_{t}^{i}, y_s('j)) = e^{-||y_t^i - y_s(j)||_2^2} = e^{-||x_t^{i} - x_s(j)||_2^2 + log(\lambda)} = \lambda k(x_{t}^{i}, x_s(j))
$$
