---
category: linear algebra
---

>Intuitive understanding of determinant

<ol type="I">
    <li> Area(Volume) of a matrix </li>
    <li> How much a matrix modifies the area(volume) of a target matrix through linear transformation </li>
</ol>


The first meaning and the second are basically the same if you set identity matrix as the target matrix.

If $$det(A) > 0$$, it changes the area(volume) of target matrix, preserving it's direction.

If $$det(A) < 0$$, it inverts the order of target matrix's column vectors through linear transformation.

If $$det(A) = 0$$, it squeezes some vectors to zero.

For example, Let $$A=\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$$

Then $$A$$ transforms $$2$$-dimensional space into a line $$y=0$$. In this case, $$det(A) = 0$$


> Characteristics of determinant

- commutative : \\
$$det(AB) = det(A)det(B) \: where \: A, B \in \mathbb{R}^{n\times n}$$


- cofactor : \\
$$det(A) = \sum_{j} a_{ij}A_{ij} \: where \: A_{ij} = (-1)^{i+j}det(M_{ij})$$


- decomposition : \\
$$det(A) = det(P^{-1}LU) = \pm (products \: of \: pivots)$$


- permutation : \\
$$
det(A) = \sum_{\sigma}a_{1\sigma_{1}}a_{2\sigma_{2}}\cdots a_{n\sigma_{n}}det(P_{\sigma}) \\ det(A) = a_{11}a_{22} - a_{12}a_{21}$$ comes from this rule.
- if $$A$$ is inversible : \\
$$
A^{-1} = \dfrac{adj(A)}{det(A)}
$$


- cramer's rule : \\
$$x_j = \dfrac{det(B_j)}{det(A)} \\ where \: B_j = 
\begin{bmatrix}
a_{11} & \cdots & b_1 & \cdots & a_{1n} \\
a_{21} & \cdots & b_2 & \cdots & a_{2n} \\
\vdots & \ddots & \vdots & \ddots & \vdots \\
a_{n1} & \cdots & b_n & \cdots & a_{nn}
\end{bmatrix}
$$


- Sylvester's determinant identity : \\
$$det(I_m + AB^T) = det(I_n + B^TA) \\
where A,B \in \mathbb{R^{m \times n}}
$$


- Schur complement :

$$
A = \begin{bmatrix} A_{11} & A_{12} \\ A_{21} & A_{22} \end{bmatrix} \Rightarrow A^{-1}=\begin{bmatrix}
A_{11}^{-1} + A_{11}^{-1}A_{12}S^{-1}A_{21}A_{11}^{-1} & -A{11}^{-1}A_{12}S^{-1} \\
-S{-1}A_{21}A_{11}^{-1} & S^{-1} 
\end{bmatrix} \\
$$


$$
where \: S = A_{22} - A_{21}A_{11}^{-1}A_{12}
$$

- Sherman-Woodbury-Morfison identity : \\
$$
(A + BD^{-1}C)^{-1} = A^{-1} -A^{-1}B(D + CA^{-1}B)^{-1}CA^{-1}
$$