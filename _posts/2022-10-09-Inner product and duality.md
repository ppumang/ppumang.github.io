---
categories: linear-algebra
---

_Definition of inner product_

_(symmetricity)_ : $$ <x,y> = <y,x> \forall x,y \in X $$

_(bilinearity)_ : $$ <c_1x_1 + c_2x_2, y> = c_1<x_1, y> + c_2<x_2, y> \forall x_1, x_2, y \in X \: and \: \forall c_1, c_2 \in \mathbb{R} $$

In $$n$$-dinemsional space, inner product is defined as elementwise product between $$n$$-dimensional vectors.

$$ x = \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} y = \begin{bmatrix} y_1 \\ y_2 \end{bmatrix} $$


$$x^Ty = \begin{bmatrix} x_1 x_2 \end{bmatrix} \begin{bmatrix} y_1 \\ y_2 \end{bmatrix} = x_1y_1 + x_2y_2 $$

If you see $$x^T$$ as $$1 \times 2$$ matrix, multiplying $$x^T$$ is same as performing linear transformation from $$2$$-dimensional space to $$1$$-dimensional space (scalar).

Let $$u = \begin{bmatrix} \dfrac{x_1}{\|x\|} \\ \\  \dfrac{x_2}{\|x\|} \end{bmatrix} = \begin{bmatrix} u_1 \\ u_2 \end{bmatrix} $$, which is a unit vector.

$$
u^T$$ projects $$\begin{bmatrix} 1 \\ 0 \end{bmatrix}$$ into $$u_1$$, and $$\begin{bmatrix} 0 \\ 1 \end{bmatrix}$$ into $$u_2$$. (_Note that it transforms 2d-vector into scalar_)

Let $$ p_1 $$ be the projection from $$\begin{bmatrix} 1 \\ 0 \end{bmatrix}$$ to $$u$$, and $$p_2$$ be the projection from $$\begin{bmatrix} 0 \\ 1 \end{bmatrix}$$ to $$u$$.

Then $$ \overline{Op_1} = u_1 $$ and $$ \overline{Op_2} = u_2 $$ due to similarity.

This means that a projection can also be seen as the $$length$$ of a projection vetor. (specifically, it's the _signed length_, but let's not think about that right now.)

Lets get back to the projection 

$$
xy = x^Ty = \begin{bmatrix} x_1 x_2 \end{bmatrix} \begin{bmatrix} y_1 \\ y_2 \end{bmatrix} = x_1y_1 + x_2y_2
$$.


$$
u_1y_1 + u_2y_2
$$
is the length of projection vector from $$y$$ to $$x$$.

$$ duality \: \rightarrow \: xy = \|x\|(u_1y_1 + u_2y_2) = x_1y_1 + x_2y_2$$