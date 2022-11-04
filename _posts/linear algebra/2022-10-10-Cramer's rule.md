---
category: linear algebra
---

Cramer's rule is used when solving the system

$$Ax = b$$

As seen in [Determinant][determinant_link], determinants can be viewed as area(or volume) of a matrix.

$$x = \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}, \: b = \begin{bmatrix} b_1 \\ b_2 \end{bmatrix}$$

$$det( \begin{bmatrix} 1 & x_1 \\ 0 & x_2 \end{bmatrix} ) = Area(\begin{bmatrix} 1 & x_1 \\ 0 & x_2 \end{bmatrix}) = x_2 $$

As linear transformation $$A$$ multiplicates the area of a matrix by $$det(A)$$, the above equation can be adjusted as

$$ det(A \begin{bmatrix} 1 & x_1 \\ 0 & x_2 \end{bmatrix} ) =
det(
\left[ \begin{array}{c|c}
A \begin{bmatrix} 1 \\ 0 \end{bmatrix} & 
A \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}
\end{array}\right]
) =
det(A)x_2$$

which yields 
$$
x_2 = \dfrac{det(\left[ \begin{array}{c|c}
A \begin{bmatrix} 1 \\ 0 \end{bmatrix} & 
\begin{bmatrix} b_1 \\ b_2 \end{bmatrix}
\end{array}\right] )}{det(A)}
$$


Note that 
$$
det(\left[ \begin{array}{c|c}
A \begin{bmatrix} 1 \\ 0 \end{bmatrix} & 
\begin{bmatrix} b_1 \\ b_2 \end{bmatrix}
\end{array}\right] )
$$
 is matrix $$A$$, with it's $$2nd$$ column replaced by $$b$$.


Similarly,
$$
x_1 = \dfrac{det(\left[ \begin{array}{c|c}
\begin{bmatrix} b_1 \\ b_2 \end{bmatrix} & 
A \begin{bmatrix} 0 \\ 1 \end{bmatrix}
\end{array}\right] )}{det(A)} 
$$


The generalized cramer's rule in $$n$$-dimensional space is


$$x_j = \dfrac{det(B_j)}{det(A)} \\ where \: B_j = 
\begin{bmatrix}
a_{11} & \cdots & b_1 & \cdots & a_{1n} \\
a_{21} & \cdots & b_2 & \cdots & a_{2n} \\
\vdots & \ddots & \vdots & \ddots & \vdots \\
a_{n1} & \cdots & b_n & \cdots & a_{nn}
\end{bmatrix}
$$

[determinant_link]: https://ppumang.github.io/linear algebra/Determinant "Go google"