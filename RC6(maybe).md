# Recitation Class for Curves

Provided by Yang Mo

## Something More about Continuity

Review: Suppose $lim_{x\to x_0,y\to y_0} f(x,y) = f(x_0,y_0)$, then the function $f(x,y)$ is said to be continuous at point $(x_0,y_0)$.

### Example 1

Discuss the continuity of 
$$
f(x,y) =\begin{cases} ln(1+xy)^{\frac{1}{xy}},xy\ne 0\\
			1,\text{otherwise}
			\end{cases}
$$















Discuss the continuity of
$$
f(x,y) = \begin{cases}
\frac{2xy}{x^2+y^2},xy\ne 0\\
				0,\text{otherwise}
\end{cases}
$$


at the point where $(x,y) = (0,0)$.

















## What is Curve?

### Definition

Let ($V$; $∥ · ∥$) be a normed vector space and $I$ ⊂ $R$ an interval. 

A set $C$ ⊂ $V$ for which there exists a continuous, surjective and locally injective map $\gamma$: $I$ → $C$ is called a curve. 

The map $\gamma$‚ is called a parametrization of $C$. 

A curve C together with a parametrization $\gamma$‚, i.e., the pair ($C; \gamma$), is called a parametrized curve.

(From Horst's Slides, Page 352)

### Simple, Open and Closed Curves

![image-20230510173721887](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230510173721887.png)

(From Horst's Slides, Page 358)





## Some Characters to describe Curve

### Tangent Vector

Tangent line at $t_0: T_pC = {x ∈ V : x = γ(t_0) + γ ′ (t_0)t, t ∈ R}$

It is an approximation of  the curve!

Unit tangent vector: $T ◦ γ(t) := \frac{γ ′ (t) }{∥γ ′(t)∥}$



### Curve's Length

Suppose $C$ is a curve in $V$ and $γ : [b,s] → C$ the parameterization.
$$
L = \int_b^s ||\gamma'(t)||dt
$$
This is actually induced with the help of Lagrange's Mean Value Theory:
$$
L = \lim _ {n \to \infin}\sum _ {i=1} ^n |\gamma(t_i) - \gamma(t_{i-1})|
$$

 ### Curvature

$$
κ ◦ γ(t)  = \frac{∥(T ◦ γ) ′ (t)∥}{ ∥γ ′(t)∥}
$$

#### Example 2

Calculate the curvature of the curve with parameterization $f : [0, 1] → R, f (x) = (cos(2πx),sin(2πx))$

(From Chen YuXiang and Zhang Leyang)















#### Example 3

Calculate the curvature of the curve $y = f(x)$ (Consider the curve consist of all (x,y))

















## Line Integral and Potential Fields

### Line Integral 

line integral of a potential function:  the line integral of f along $C^*$  by
$$
\int _{C^∗} f \space d l := \int _I (f ◦ \gamma)(t) · ∥\gamma ' (t)∥ d t
$$
If we calculate the line integral using a concrete parametrization $\gamma: I → C$, we obtain 
$$
 \int _{C ^∗} F d\vec{l} = \int _{C^ ∗} ⟨F, T ⟩ dl = \int_I ⟨F ◦ \gamma(t), T ◦ \gamma(t)⟩∥\gamma'(t)∥ d t
$$

#### Example 4

Evaluate $ \int _{C^∗} x ^2 y ^2 dl$  where $C$ is the circle centered at (0, 4, 0) with radius 2. The orientation is shown in following figure.

![image-20230510195559199](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230510195559199.png)



























### Potential Fields

Condition: There exist U(x) such that $F(x) = \nabla U(x)$

In physics there is a negative sign

Conservative Field: 

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230510200315922.png" alt="image-20230510200315922" style="zoom: 67%;" />

Potential Fields are Conservative!

#### Example 5

Prove the gravity field is conservative.



















## References

- VV285, slide. Horst Hohberger
- RC, slides. TA-Pingbang Hu
- RC, slides. TA-Chen Yuxiang



For further questions, you can contact me through wechat.

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230515231252742.png" alt="image-20230515231252742" style="zoom: 33%;" />

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230627184406373.png" alt="image-20230627184406373" style="zoom: 67%;" />

The end.