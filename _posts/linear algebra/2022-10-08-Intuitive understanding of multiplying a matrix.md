---
category: linear algebra
---

> Multiplying matrices can be seen as change of basis 

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

$$x=x_1\begin{bmatrix}1 \\ 0\end{bmatrix}
+ x_2\begin{bmatrix}0 \\ 1 \end{bmatrix}$$

$$Ax = x_1 \times A\begin{bmatrix}1 \\ 0\end{bmatrix} 
+ x_2 \times A\begin{bmatrix}0 \\ 1\end{bmatrix}
= 
x_1\begin{bmatrix}
a_{11} \\
a_{21}
\end{bmatrix} + x_2\begin{bmatrix}
a_{12} \\
a_{22}
\end{bmatrix}$$

> Applying matrices several time can be seen as applying linear transformations several time

$$A = \begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix} \quad 

B = \begin{bmatrix}
b_{11} & b_{12} \\
b_{21} & b_{22}
\end{bmatrix} \quad $$
   

$$BAI = BA = B \times 
\begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix}
 = \left[ \begin{array}{c|c}
   B \begin{bmatrix} a_{11} \\ a_{21} \end{bmatrix} & 
   B \begin{bmatrix} a_{12} \\ a_{22} \end{bmatrix}
\end{array}\right]$$
        
$$BAx = x_1 \times B \begin{bmatrix} a_{11} \\ a_{21} \end{bmatrix} + x_2 \times B \begin{bmatrix} a_{12} \\ a_{22} \end{bmatrix}$$

> If $$A$$ is non-squared, it transforms a vector to another dimension.

$$ A \in \mathbb{R}^{n\times m} \quad x \in \mathbb{R}^m $$

if $$ n < m $$, then $$A$$ squeezes $$m$$-dimensional vector in to $$n$$-dimensinal vector

if $$ n = 1 $$ and $$ m = 3 $$, multiplying $$A$$ squeezes $$3$$-dimensional vector into scalar. Generally, in this case, a plane squeezes into a scalar.

else if $$ n > m $$, $$A$$ puts $$m$$-dimensional space in $$n$$-dimensional space

if $$ n = 3 $$ and $$ m = 1 $$, generally, multiplying $$A$$ puts a scalar into $$3$$-dimensional space.