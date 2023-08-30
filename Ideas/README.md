## The little theorem of RBF kernel transfer learning:
An adaptive RBF kernel with parameter $\lambda$ is equivalent to adding a single feature $\lambda' = \sqrt{-\log(\lambda)}$ to the target data and a 0 feature to the source data.

Proof:
$$k(y_{t}^{i}, y_s^j) = e^{-||y_t^i - y_s^j||_2^2} = e^{-||x_t^i - x_s^j||_2^2 + log(\lambda)} = \lambda k(x_t^i, x_s^j)$$

I proved this as I was reading about the adaptive kernel approach in transfer learning. Several recent approaches such as the DIVA (2020) model are utilizing domain-related features in their predictions, and the kernel adaptive approach also does this directly. 

The closest treatment I found to this theorem is the one in the original adaptive kernel approach paper where they proved that augmenting data with lots of features (twice the number of original features, to be exact) is equivalent to adapting the kernel directly. But for a kernel such as the RBF where the kernel calculates dot product in a space of infinite dimensions, it's not exactly clear how their result would translate. I proved that for the very special case of an RBF kernel, adding a _single feature_ suffices to adapt the kernel. 
