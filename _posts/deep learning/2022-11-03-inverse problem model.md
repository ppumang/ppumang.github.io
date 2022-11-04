---
category: deep learning
---

In _Inverse Problem_, we wish to recover a signal $$X_{true}$$ given measurements $$Y$$.

$$
\mathcal{A}[X_{true}] + \epsilon = Y
$$

The goal of inverse problem is to find $$\mathcal{A^{-1}}$$.

Most denoising models are based on deep learning.

We use neural network to approximate
$$f_\theta \approx \mathcal{A^{-1}}$$
