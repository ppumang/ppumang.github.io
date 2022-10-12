---
category: linear algebra
---

As we saw in [Intuitive understanding of multiplying a matrix][matmul_link], matrix multiplication can be seen as change of basis, preserving a vector's coefficients.

In this point of view, a single vector can be represented differently according to what basis you choose.

If a vectorspace $$\mathbb{A}$$ chooses $$\begin{bmatrix} a_{11} \\ a_{21} \end{bmatrix}$$ and $$\begin{bmatrix} a_{12} \\ a_{22} \end{bmatrix}$$ as it's basis,


$$\begin{bmatrix} a_{11} \\ a_{21} \end{bmatrix}_{\mathbb{R}} = \begin{bmatrix} 1 \\ 0 \end{bmatrix}_{\mathbb{A}} $$
and
$$\begin{bmatrix} a_{12} \\ a_{22} \end{bmatrix}_{\mathbb{R}} = \begin{bmatrix} 0 \\ 1 \end{bmatrix}_{\mathbb{A}}$$



In $$\mathbb{R}$$, $$90^\circ$$ rotation of $$\begin{bmatrix} a_{11} \\ a_{21} \end{bmatrix}_{\mathbb{R}}=\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}_{\mathbb{R}} \begin{bmatrix} a_{11} \\ a_{21} \end{bmatrix}_{\mathbb{R}}$$


In $$\mathbb{A}$$, $$90^\circ$$ rotation of 
$$\begin{bmatrix} 1 \\ 0 \end{bmatrix}_{\mathbb{A}}
=\begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix}^{-1} 
\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} 
\begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix} 
\begin{bmatrix} 1 \\ 0 \end{bmatrix}_{\mathbb{A}}$$


So, if you want to perform linear transformation $$P_{\mathbb{R}}$$ to $$ \begin{bmatrix} x \\ y \end{bmatrix}_{\mathbb{A}} $$, you can do 

$$ A^{-1}PA \begin{bmatrix} x \\ y \end{bmatrix} $$

[matmul_link]: https://ppumang.github.io/linear algebra/Intuitive-understanding-of-multiplying-a-matrix