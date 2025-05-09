An implementation of Shampoo optimizer in PyTorch.
https://arxiv.org/abs/2002.09018

This implementation is not optimized to work well in the distributed setting or run fast in the single GPU setting. The optimizer operations are not parallelized well. The more efficient version of Shampoo is the JAX version and recommended in practice.

However, it should be straightforward to add many of the features mentioned in the paper, including CPU-based inverses that run every K steps, especially useful for training language models. And parallelizing the updates across GPUs in the data-parallel setting.

A parallelized distributed version called 3D-Shampoo is available in this repo: https://github.com/noabauma/3d-shampoo. It works with the DeepSpeed library.

Another parallelized version without the need of DeepSpeed is in this library: https://github.com/kazukiosawa/asdl
