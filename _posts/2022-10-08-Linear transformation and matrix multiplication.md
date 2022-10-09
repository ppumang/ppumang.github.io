---
categories: linear-algebra
use_math: true
katex: True
---

> Multiplying $$A$$ can be seen as change of basis
from original basis $$\hat i \ \hat j$$ to new basis 
$$
\begin{bmatrix}
a_{11} \\
a_{21}
\end{bmatrix}
\
\begin{bmatrix}
a_{12} \\
a_{22}
\end{bmatrix}
$$

$$A = \begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix} \quad 

x=\begin{bmatrix}
x_1 \\
x_2
\end{bmatrix}
\quad
\hat i=\begin{bmatrix} 1 \\ 0 \end{bmatrix}
\quad
\hat j=\begin{bmatrix} 0 \\ 1 \end{bmatrix}
$$

$$
x=x_1\begin{bmatrix}1 \\ 0\end{bmatrix}
+ x_2\begin{bmatrix}0 \\ 1 \end{bmatrix}
$$

$$
Ax = x_1 \times A\begin{bmatrix}1 \\ 0\end{bmatrix} 
+ x_2 \times A\begin{bmatrix}0 \\ 1\end{bmatrix}
= 
x_1\begin{bmatrix}
a_{11} \\
a_{21}
\end{bmatrix} + x_2\begin{bmatrix}
a_{12} \\
a_{22}
\end{bmatrix}
$$

> Applying matrices several time can be seen as applying linear transformations several time

$$
A = \begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix} \quad 

B = \begin{bmatrix}
b_{11} & b_{12} \\
b_{21} & b_{22}
\end{bmatrix} \quad 
$$

$$
BAI = BA = B \times 
\begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix}
 = \left[ \begin{array}{c|c}
   B \begin{bmatrix} a_{11} \\ a_{21} \end{bmatrix} & 
   B \begin{bmatrix} a_{12} \\ a_{22} \end{bmatrix}
\end{array}\right]
$$