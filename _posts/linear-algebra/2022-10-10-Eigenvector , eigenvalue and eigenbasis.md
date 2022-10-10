---
categories: linear-algebra
---

$$Ax = \lambda x$$


Then $$\lambda$$ is the eigenvalue of $$A$$, and $$x$$ is the eigenvector of $$A$$.


Geometrically, $$x$$ stays in the same direction after linear transformation $$A$$, with it's length multiplied by $$\lambda$$.

Since $$\lambda x = \lambda I x$$, $$Ax = \lambda x \Leftrightarrow (A - \lambda I)x = 0$$.

$$A - \lambda I$$
is also a linear transformation.

$$ \exists x \quad s.t \quad (A - \lambda I) x = 0 \Leftrightarrow det(A - \lambda I) = 0 $$ 

In order to squeeze a vector into zero through linear transformation $$A$$, $$A$$ has to squeeze a vectorspace into lower dimension, which means it's determinant is zero.

> Eigenbasis

If every basis vectors are eigenvectors they are called $$eigenbasis$$.

$$A = \begin{bmatrix} -1 & 0 \\ 0 & 2 \end{bmatrix}$$
transforms $$\begin{bmatrix} 1 \\ 0 \end{bmatrix}$$ to $$\begin{bmatrix} -1 \\ 0 \end{bmatrix}$$, and $$\begin{bmatrix} 0 \\ 1 \end{bmatrix}$$ into $$\begin{bmatrix} 0 \\ 2 \end{bmatrix}$$

Eigenbasis is useful because it's coresponding matrix is diagonal. Diagonal matrices are useful because it's easy to multiply.

$$ D = \begin{bmatrix} d_1 & 0 \\ 0 & d_2 \end{bmatrix} \rightarrow D^n = \begin{bmatrix} d_1^n & 0 \\ 0 & d_2^n \end{bmatrix} $$

Suppose you have to compute $$A^{100}$$. It's a very hard problem. But if you can find eigenvectors of $$A$$, you can easily compute $$A^{100}$$ by changing basis to $$A$$'s eigenvectors.

If you choose $$A$$'s basis, it becomes eigenbasis of that vectorspace because only their length changes after multiplying $$A$$.

In this new vectorspace's perspective, $$A$$ is a diagonal matrix.

So, in order to compute $$A^{100}$$, you can move the coordinate system to which has $$A$$'s eigenvectors as basis, compute $$A_{\mathbb{A}}^{100}$$ (which is diagonal), and change the basis back to standard basis.

$$
A = \begin{bmatrix} 3 & 1 \\ 0 & 2 \end{bmatrix} \rightarrow 
\lambda_1 = 3, 
v_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix},
\lambda_2 = 2, 
v_1 = \begin{bmatrix} -1 \\ 1 \end{bmatrix} 
$$


$$
\begin{bmatrix} 1 & -1 \\ 0 & 1 \end{bmatrix}^{-1} A \begin{bmatrix} 1 & -1 \\ 0 & 1 \end{bmatrix} 
= \begin{bmatrix} 1 & -1 \\ 0 & 1 \end{bmatrix}^{-1} \begin{bmatrix} 3 & 1 \\ 0 & 2 \end{bmatrix} \begin{bmatrix} 1 & -1 \\ 0 & 1 \end{bmatrix} 
= \begin{bmatrix} 3 & 0 \\ 0 & 2 \end{bmatrix}
= A_{\mathbb{A}}
$$