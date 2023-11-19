# Recitation Class for Multi-variable Integration

Provided by Yang Mo, 2023/5/15

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230704182248691.png" alt="image-20230704182248691" style="zoom: 25%;" />

## About Homework 7

Let $g:\R^2 \to \R$ be defined by
$$
g(x,y) =\begin{cases}
(x^2+y^2)\sin(\frac{1}{\sqrt{x^2+y^2}}),x^2+y^2\ne 0\\
0,x^2+y^2=0

\end{cases}
$$
Verify that the partial derivatives of $g$ exist and are bounded in a neighborhood of the origin, but are not continuous at the origin. Show that g is differentiable at the origin. Is the derivative of g continuous at the origin?



















## Cuboids

Let $a_k,b_k,k=1,\ldots,n$ be pairs of numbers with $a_k<b_k$. Then the set $Q\subset\R^n$ given by

$$
Q =[a_1,b_1]\times\cdots\times[a_n,b_n] 

​      =\{x\in\R^n:x_k\in[a_k,b_k],k=1,\ldots,n\}
$$


  is called an $n$-*cuboid*. We define the volume of $Q$ to be

$$
|Q|:=\prod_{k=1}^{n}(b_k-a_k)
$$
  We will denote the set of all $n$-cuboids by $\mathcal{Q}_n$.

  Remark: Clearly, an $n$-cuboid is a compact set in $\R^n$.

Let $\Omega\subset\R^n$ be a bounded non-empty set. We define the outerand inner volume of $\Omega$ by
$$
\overline{V}(\Omega)  :=\inf\left\{\sum_{k=0}^{r}|Q_k|:r\in\N,\,

​    Q_0,\ldots,Q_r\in\mathcal{Q}_n,\Omega\subset

​    \bigcup\limits_{k=1}^rQ_k\right\},                 \\

​    \underline{V}(\Omega) :=\sup\left\{\sum_{k=0}^{r}|Q_k|:r\in\N,\,

​    Q_0,\ldots,Q_r\in\mathcal{Q}_n,\Omega\supset

​    \bigcup\limits_{k=1}^rQ_k,\bigcap\limits_{k=1}^rQ_k

​    =\emptyset\right\}.
$$
  It is easy to see that $0\leq\underline{V}(\Omega)\leq\overline{V}(\Omega)$.

We can now define Jordan Measurable based on outer and inner volume of a set.



  Let $\Omega\subset\R^n$ be a bounded set. Then $\Omega$ is said to be Jordan measurable if either

- $\overline{V}(\Omega)=0$ or

- $\overline{V}(\Omega)=\underline{V}  (\Omega)$.

  In the first case, we say that $\Omega$ has Jordan measure zero, in the second case we say that
$$
|\Omega|:=\overline{V}(\Omega)=\underline{V}

​    (\Omega)
$$
  is the Jordan measure of $\Omega$.

(Refering to Hu Pingbang's VV285 RC)



## Some Properties about multi-variable integration

### Fubini's Theorem

Let $Q_1$ be an $n_1$-cuboid and $Q_2$ an $n_2$-cuboid so that $Q:=Q_1\times Q_2\subset\R^{n_1+n_2}$ is an $(n_1+n_2)$-cuboid. Assume that $f:Q\to\R$ is integrable on $Q$ and that for every $x\in Q_1$ the integral


$$
g(x)=\int_{Q_2}f(x,\cdot)
$$
  exists. Then
$$
\int_Qf=\int_{Q_1\times Q_2}f=\int_{Q_1}g=\int_{Q_1}\left(\int_{Q_2}f\right)
$$
Remark: This is a very powerful tool. So that we can divide and conquer a integral in $\R^n$.

### Linearity

$$
\int\int
_R
λf (x, y) + \mu g(x, y)dA = λ
\int\int_
R
f (x, y)dA + \mu
\int\int_
R
g(x, y)dA.
$$



### Area additivity

If region R can be split into two disjoint regions $D_1$, $D_2$ with $D_1 ∩ D_2 = \phi$, then
$$
\int\int_
R
f (x, y)dA =
\int\int
_{D_1}
f (x, y)dA +
\int\int
_{D_2}
f (x, y)dA
$$

### Integral mean value theorem

If $f$ is continuous on $D$, and $D$ is a connected bounded closed interval, then there exists $x_0$ that
$$
\int _D f = f(x_0) \cdot |D|
$$

 ### Comparability

If $f(x) > g(x)$ is always true on $D$, then
$$
\int\int_Df(x)dA > \int\int_D g(x)dA
$$

### Examples

1. Find the intersecting volume of $x^2 + y^2 \le a^2$  and $x^2+z^2 \le a^2$

















## Integration by substitution

![雅可比矩阵几何意义的直观解释及应用- mathinside的个人空间- OSCHINA - 中文开源技术交流社区](https://oscimg.oschina.net/oscnet/8aef9c73-f7a2-4f4e-8e08-def1671dc4eb.png)

Now we consider a 2-d problem. Suppose $x = f(u, v)$ and $y = g(u,v)$
$$
\int\int_D f(x,y) dxdy = \int\int_{D'}f(x,y)|\frac{\partial(x,y)}{\partial(u,v)}|dudv
$$
where
$$
|\frac{\partial(x,y)}{\partial(u,v)}|=|\frac{\partial x}{\partial u}\cdot \frac{\partial y}{\partial v}-\frac{\partial x}{\partial v}\cdot \frac{\partial y}{\partial u}|
$$
















### Examples

2. Find the volume of 
   $$
   \frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2} \le 1
   $$



















3. The sprinkler head used for sprinkling irrigation is shown in Figure 2-Example 3(a). Small holes with the same diameter are distributed on the spherical surface to spray water. The radius of the spherical surface is r, and the small holes are relative to the axis of symmetry. The distribution range of the polar angle $\theta$ is: $0≤\theta≤\theta _0=\pi/4$. In order to make the water injection energy sprayed to the ground evenly distributed (uniform irrigation), the distribution of the number of small holes per unit area on the spherical surface of the sprinkler is calculated, that is, the expression of the small hole number density $n$.

   ![image-20230515225234558](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230515225234558.png)

























4. Find
   $$
   \int\int_{x^2+y^2 \le R^2} e^{x^2+y^2} dxdy
   $$
   























### Cylindrical coordinates

Cylindrical coordinates in $\R^3$ are given through a map
$$
\Phi:(0,\infty)\times[0,2\pi)\times\R\to\R^3\setminus\{0\},\qquad

​        (r,\phi,\zeta)\mapsto(x,y,z)
$$
defined by
$$
x=r\cos\phi,\qquad\quad y=r\sin\phi,\qquad\quad z=\zeta
$$
In this case
$$
|\det J_\Phi(r,\phi,\zeta)|=\left|\det\begin{pmatrix}

​          \cos\phi & -r\sin\phi & 0 \\

​          \sin\phi & r\cos\phi  & 0 \\

​          0     & 0      & 1

​        \end{pmatrix}\right|=r
$$

### Spherical coordinates

Spherical coordinates in $\R^3$ are often defined through a map
$$
\Phi:(0,\infty)\times[0,2\pi)\times(0,\pi)\to\R^3\setminus\{0\},\quad

​            (r,\phi,\theta)\mapsto(x,y,z),\\

​          x=r\cos\phi\sin\theta,~y=r\sin\phi\sin\theta,~z=r\cos\theta.
$$
Of course, there is a certain freedom in defining $\theta$ and $\phi$, so there are alternative formulations. The modulus of the determinant of the

 Jacobian is given by
$$
|\det J_\Phi(r,\phi,\theta)| &=\left|\det\begin{pmatrix}

​              \cos\phi\sin\theta & -r\sin\phi\sin\theta & r\cos\phi\cos\theta \\

​              \sin\phi\sin\theta & r\cos\phi\sin\theta  & r\sin\phi\cos\theta \\

​              \cos\theta     & 0           & -r\sin\theta

​            \end{pmatrix}\right| 

​            &=r^2\sin\theta
$$




## Integration on higher dimensions

### n-dimensional Ball

Try to find the volume of the n-dimension ball, which can be defined as
$$
B_n(a) = \{ (x_1,x_2,...,x_n)| x_1^2 + x_2^2 +...+x_n^2 \le a^2 \}.
$$











































## References

- VV285, slide. Horst Hohberger
- RC, slides. TA-Pingbang Hu
- RC, slides. TA-Chen Yuxiang
- Mechanics. Jiafu Cheng

For further questions, you can contact me on wechat.

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230515231252742.png" alt="image-20230515231252742" style="zoom: 33%;" />

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230704182958102.png" alt="image-20230704182958102" style="zoom:25%;" />
