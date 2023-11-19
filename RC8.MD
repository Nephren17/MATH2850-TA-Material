# Recitation Class for Vector Calculus

Provided by Yang Mo, 2023/5/16

## Surface

### Parameterization

A smooth parametrized m-surface in *$\R^n$* is a subset $\mathcal{S}\subset\R^n$ together with a locally bijective, continuously differentiable map (parametrization)
$$
\varphi:\Omega\to\mathcal{S},\qquad\quad

​    \Omega\subset\R^m
$$
such that
$$
\text{rank}\,D\varphi|_x=m
$$
for almost every $x\in\Omega$. If $m=n-1$, $\mathcal{S}$ is said to be a *parametrized hyper-surface*.

### Tangent Spaces of Surface

Let $\mathcal{S}\subset\R^n$ be a parametrized $m$-surface with parametrization $\varphi:\Omega\to\mathcal{S}$. Then
$$
t_k(p)=\frac{\partial}{\partial x_k}\left.\begin{pmatrix}

​      \varphi_1(x) \\

​      \vdots    \\

​      \varphi_n(x)

​    \end{pmatrix}\right|_{x=\varphi^{-1}(p)},\qquad\quad

​    k=1,\ldots,m.
$$




  is called the $k$th tangent vector of $\mathcal{S}$ at $p\in\mathcal{S}$ and

$$
T_p\mathcal{S}:=\text{ran}\,D\varphi|_x

​    =\text{span}\{t_1(p),\ldots,t_m(p)\}
$$
is called the tangent space to $\mathcal{S}$ at $p$. The vector field

$$
t_k:\mathcal{S}\to\R^n,\qquad\qquad\quad

​    p\mapsto t_k(p)
$$
is called the $k$th tangent vector field on $\mathcal{S}$.



### Flux

Let $F:\R^{n}\to\R^{n}$ be a vector field defined in a neighborhood of a hypersurface $\mathcal{S}$ with parametrization $\varphi:\Omega\to\R^{n},\Omega\subset\R^{n-1}$. Then we define the*flux of* *$F$* *through* $\mathcal{S}$ by
$$
\begin{equation*}

​    \begin{split}

​      \int_\mathcal{S}F\,d\vec{A} &:=\int_\mathcal{S}<{F},{N}>dA \qquad(=\int_\mathcal{S}<{F},{d\vec{A}}>\\

​      &=\int_\Omega<{F\circ\varphi(x)},{N\circ\varphi(x)}>\sqrt{g(x)}\,dx_1...dx_{n-1}

​    \end{split}

  \end{equation*}
$$
where
$$
g(x) = \det\begin{pmatrix}

​      <t_1,t_1>,...<t_1,t_m> \\

​      \dots,\dots,\dots    \\

​      <t_m,t_1>,...,<t_m,t_m>

​    \end{pmatrix}
$$


Especially, in $\R^3$
$$
A =
\int\int_
Ω
∥t1 × t2∥ ◦ φ(x)dx_1dx_2
$$
Where t1, t2 are the tangent vector at point (x1, x2).

Note that you don’t need to normalize the tangent vector!



Another point of view see the problem somehow similar to substitution. (Note this is only another point which is not include in slides!)
$$
\vec{n} = \frac{\vec{r_u'} \times \vec{r_v'}}{|\vec{r_u'} \times \vec{r_v'}|}\\  dS= |\vec{r_u'} \times \vec{r_v'}|dudv\\
d\vec{S} = \vec{n} dS = \det\begin{pmatrix}

​      \vec{i}\space\space \vec{j} \space\space \vec{k} \\

​      x_u'\space  y_u'\space z_u'  \\

​     x_v'\space y_v'\space z_v'

​    \end{pmatrix} = (\frac{\partial(y,z)}{\partial(u,v)}dudv)\vec{i}+(\frac{\partial(x,z)}{\partial(u,v)}dudv)\vec{j}+(\frac{\partial(x,y)}{\partial(u,v)}dudv)\vec{k}
$$
So we can define
$$
dy \wedge dz =\frac{\partial(y,z)}{\partial(u,v)}dudv\\
dx \wedge dz =\frac{\partial(x,z)}{\partial(u,v)}dudv\\
dx \wedge dy =\frac{\partial(x,y)}{\partial(u,v)}dudv\\
$$
So for $\vec{v} = (P,Q,R)$
$$
\int\int\vec{v}\cdot d\vec{S} = \int\int_S P dy\wedge dz +  Q dx\wedge dz+ R dx\wedge dy
$$

### Example

1. For  
   $$
   S = \frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2}
   $$
   Find
   $$
   \int\int_S x^3 dydz + y^3 dzdx
   $$



















## Gradient, Divergence and Rotation

### Gradient

Let's consider a function **f(x, y)** that depends on variables **x** and **y**. The gradient of **f** at a point (x₀, y₀) is defined as:
$$
∇f(x₀, y₀) = (∂f/∂x, ∂f/∂y)
$$
Here, ∂f/∂x represents the partial derivative of **f** with respect to **x** evaluated at (x₀, y₀), and ∂f/∂y represents the partial derivative of **f** with respect to **y** evaluated at (x₀, y₀).

### Divergence 

$$
\text{div}\,F:=\frac{\partial F_1}{\partial x_1}+\cdots+\frac{\partial F_n}{\partial x_n}
$$

  is called the divergenceof $F$.

  Remark: The total flux density at a point $x$ is given by the divergence of the field at $x$.

  In triangle calculus, the divergence of a vector field $F$ can be expressed as
$$
\\{div}\,F=<{{\nabla},{F}}>=\left\langle{\begin{pmatrix}

​        \frac{\partial}{\partial x_1} \\

​        \vdots             \\

​        \frac{\partial}{\partial x_n}

​      \end{pmatrix}}{\begin{pmatrix}

​        F_1   \\

​        \vdots \\

​        F_n

​      \end{pmatrix}}\right\rangle=\frac{\partial F_1}{\partial x_1}+\cdots+\frac{\partial F_n}{\partial x_n}.
$$
 In some other notations, one also uses $\nabla\cdot F$ to indicates the divergence of $F$. This type of notation is more common in a physical textbooks.

### Rotation

In triangle calculus, the rotation of a vector field $F$ can be expressed as
$$
rot F = ∇ \times F = ( ∂F_z/∂y - ∂F_y/∂z ) \vec{i} + ( ∂F_x/∂z - ∂F_z/∂x ) \vec{j} + ( ∂F_y/∂x - ∂F_x/∂y ) \vec{k}
$$
Let $\Omega\subset\R^n$ be an open set, $F:\Omega\to\R^n$ a continuously differentiable vector field and $\mathcal{C}^*$ an oriented closed curve in $\R^n$. Then
$$
\int_{\mathcal{C}^*}\langle {F},{T}\rangle ds
$$
 is called the (total) circulation of $F$ along $\mathcal{C}$. 

If a field is of no rotation, then there exists a potential.



## Stokes' theorem

Let $\Omega\subset\R^3$ be an open set, $\mathcal{S}\subset\Omega$ a parametrized, admissible surface in $\R^3$ with boundary $\partial\mathcal{S}$ and let $F:\Omega\to\R^3$ be a continuously differentiable vector field. Then
$$
  \int_{\partial\mathcal{S}^*}F\,d\vec{s}=

​    \int_{\mathcal{S}^*}\text{rot}\,F\,d\vec{A}
$$
where the orientations of the boundary curve $\partial\mathcal{S}^*$ and the surface $\mathcal{S}^*$ are chosen according to right hand law.

### Example

2. $L$ is the intersection line of $z = 3x^2 + 4y^2$ and $4x^2 + y^2 = 4y$, and is clockwise seeing from the positive side of z-axis. 

   Please find the circulation of $\vec{v} = y(z+1)\cdot\vec{i} +xz\cdot\vec{j}+(xy-z)\cdot\vec{k} $ on $L$

















![image-20230718163326319](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230718163326319.png)











## References

- VV285, slide. Horst Hohberger
- RC, slides. TA-Pingbang Hu
- RC, slides. TA-Chen Yuxiang

For further questions, you can contact me through wechat.

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230515231252742.png" alt="image-20230515231252742" style="zoom: 33%;" />

<img src="D:\sparks\Pictures\hZe32.src=http___pix2.tthumb_drama_48_652_540x303.jpg_refer=http___pix2.tvzhe.jpg" alt="hZe32.src=http___pix2.tthumb_drama_48_652_540x303.jpg_refer=http___pix2.tvzhe" style="zoom: 50%;" />