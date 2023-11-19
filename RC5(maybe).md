# Norms, Convergence, and Derivative

Dear all, nice to meet you! This is my first RC, and maybe many of you still don't know me. I'm Yang Mo, a sophomore student majoring in ECE. In my view, VV285 is one of the most useful and interesting course among all the courses in JI. Hope you can enjoy this course!

Also, I believe different TAs will hold different styles of RC. Some may focus on advanced techniques, some on basic concepts, some on proof, etc. For me, I hope you can "visualize" all the calculations on high dimensions. So my RC will more focus on helping you to understand what happened in the high dimension space. The exercise I choose might be easy, but they can help you understand what happened.

And I know some of you are very good at math, much better than me. So you can simply do something more interesting rather than reading the slide. If you want to learn all the things in a VV186 way, it is recommended to read textbooks from the math department or look at the RC slides provided by Pingbang Hu, a previous TA who works on TCS at UIUC:

https://github.com/sleepymalc/VV285-2021SU

If you think you didn't have enough exercise or you think my exercises are too obvious, you can look at the RC slides from another previous TA, Yuxiang Chen:

[AlaricRFF/AlaricRFF-VV285_SU2022_Yuxiang-Chen (github.com)](https://github.com/AlaricRFF/AlaricRFF-VV285_SU2022_Yuxiang-Chen)



## Norms

The most common norm that we're familiar with is on $\R^n$
$$
||(x_i)||_2 = \sqrt{\sum_i x_i^2}
$$

$$
||(x_i)||_\infin = max \{|x_i|:1\le i \le n\}
$$
Suppose $||\cdot||$ is a norm on $V$, then for any element $x,y$ belongs to vector space $V$, it follows:

- $||x|| \ge 0$
- $k\cdot ||x|| = ||k\cdot x||$
- $||x+y|| \le ||x|| + ||y||$
- 







In VV186, you are required to study some norms in Assignment 7. Do you still remember them?

![image-20230602205837556](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230602205837556.png)

I've put all the things about this exercise in the appendix and we can discuss about it.



## Open and Close Set

**Open Set**
For every $x$ in $A$, there exists $ε > 0$ such that $B(x, ε) ⊆ A$, where $B(x, ε)$ denotes the open ball of radius ε centered at $x$.

**Closed Set**
Formally, a set $A$ is said to be closed if it contains all of its accumulation points.

### Excercise

Prove:  A bounded infinite sequence of points on $\R^2$ always has a convergent subsequence.



















Suppose X is a complete normed space and $S_1$, $S_2$, ..., $S_n$ is a finite collection of subsets of $X$. Judge $T$ or $F$:  

- If $S_i$ ’s are open, then $\cup_i S_i$ is open. 

- If $S_i$ ’s are open, then $\cap_ i S_i$ is open.  

- If $S_i$ ’s are closed, then $\cup_i S_i$ is closed. 

- If $S_i$ ’s are closed, then $\cap_i S_i$ is closed. 

- If $Y$ is a normed space and $f : X → Y$ is continuous, then $f (O)$ is open whenever $O ⊆ X$ is open. 

- Suppose $K ⊆ X$ is compact and $X$ is a normed space. Any continuous functions $f : K → X$ is uniformly continuous.





















Let X be a complete normed vector space. Then the set: 
$$
GL(X) := \{L ∈ \mathcal{L} (X, X): L^{−1} exists\}
$$
Show that this set is open. Further more, show that if $∥L∥ ≤ 1$, then $\mathcal{1} − L ∈ GL(X)$ and
$$
(\mathcal{1} − L) ^{−1} = \sum _{n=0}^{\infin} L^n
$$
 where $L^0 := \mathcal{1}$ which is the identity.







































## Derivatives

Suppose $A ∈ Mat(n × n : F)$, calculate their first derivatives:

- $f (x) = ⟨x, Ax⟩$

- $g(A) = tr(A^2 )$



















## Appendix: The Exercise in VV186

### 1. About what is required to be a normed vector space

A vector space, or a linear space, is a set of objects which can be added and multiplied by scalars. The operation of addition and multiplication should follow a set of specific rules. For more detailed information, you can visit https://en.wikipedia.org/wiki/Vector_space.

For normed vector space, some additional requirements should be added. For a space, of course, we want to measure the distance between two elements. But, how can we measure? And is there any requirement for our method to measure?

In a normal way, we can define a distance for a 3-dimension space like that the distance between (a,b) and (c,d) is 
$$
\sqrt{(a-c)^2+(b-d)^2}
$$
However, this can be easily changed if I want to invent a new way to measure distance. Using the same example, I can also set my distance like this:
$$
\sqrt[3]{(a-b)^3+(c-d)^3}
$$
No one can say this is problematic. So, what is distance, or what should it be like?

Well, mathematicians say that you can define a "distance" as long as it meets 3 requirements: (We denote distance as ∥ · ∥， and said V and U to be elements of the vector space)

1. ∥V∥ ≥ 0 and ∥V∥ = 0 if and only if V = 0;
2. For all the scalars a, ∥a · V∥ = |a| · ∥V∥
3. ∥U + V∥ ≤ ∥U∥ + ∥V∥

We can discover that the third one is the hardest to be satisfied. However, there's an interesting discovery: For all p belonging to natural numbers, these distances always meets the requirements: (U and V can be respectively written as (u1,u2,···, un) and (v1,v2,···,vn))
$$
\sqrt[p]{(u_1-v_1)^p+(u_2-v_2)^p+······+(u_n-v_n)^p}
$$
This is even true when p goes to infinity. What happens and why?

### 2. Start from Jensen Inequality

When a function is convex, we can apply Jensen's Inequality to it. It estimates the properties of convex functions by assuming they behave linearly. 

Jensen's Inequality tells us that, for a convex function f(x) (whose domain is [a,b]), and x1,x2,...,xn∈[a,b], we can know that
$$
\frac{f(x_1)+f(x_2)+···+f(x_n)}{n}\ge f(\frac{x_1+x_2+···+x_n}{n})
$$
Similarly, you can get the reverse result if f(x) is a concave function.

The detailed information can be viewed at https://en.wikipedia.org/wiki/Jensen_inequality.

![](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fbkimg.cdn.bcebos.com%2Fpic%2Fcdbf6c81800a19d80b555b4c38fa828ba61e4621&refer=http%3A%2F%2Fbkimg.cdn.bcebos.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1643369034&t=0888ef54e6e33ed7507b21564795b34d)

### 3. From Jensen's inequality to Hölder's inequality

First, we need to know what's Hölder's inequality. Hölder's inequality can be written as:
$$
\sum_{i=1}^n |x_jy_j| \le (\sum_{j=1}^n |x_j|^p)^{\frac{1}{p}}(\sum_{j=1}^n |x_j|^q)^{\frac{1}{q}}
$$
p and q should satisfy that p∈N and 1/p +1/q =1.

#### Proof:

let 
$$
\widetilde x_i=\frac{|x_i|}{\sqrt[p]{\sum_{j=1}^n |x_i|^p}},\space\space\space\widetilde y_i=\frac{|y_i|}{\sqrt[p]{\sum_{j=1}^n |y_i|^p}}
$$
We can discover for Jensen's inequality that
$$
\prod_{i=1}^n a_i^{\lambda_i} \le \sum_{i=1}^n \lambda_ia_i\space\space\space\space\space\space	(\sum\lambda_i=1)
$$
(which is easy to be proved by applying a log function on the RHS. Note that log function is concave and you can apply Jensen's inequality to it)

According to the upward formula, we can deduce that
$$
\widetilde x_i · \widetilde y_i \le \frac{\widetilde x_i^p}{p} +\frac{\widetilde y_i^q}{q}\space\space\space\space\space\space (As \space \frac{1}{p}+\frac{1}{q}=1)
$$
This can be transfered as
$$
\frac{|x_i||y_i|}{\sqrt[p]{\sum_{j=1}^n |x_i|^p}\sqrt[q]{\sum_{j=1}^n |y_i|^q}}\le \frac{|x_i|^p}{p\sum_{j=1}^n |x_i|^p}+\frac{|y_i|^q}{p\sum_{j=1}^n |y_i|^q}
$$
Add all the different *i*s  up
$$
\frac{\sum_{j=1}^n |x_i||y_i|}{\sqrt[p]{\sum_{j=1}^n |x_i|^p}\sqrt[q]{\sum_{j=1}^n |y_i|^q}} \le \frac{\sum _{i=1}^n|x_i|^p}{p\sum_{j=1}^n |x_i|^p}+\frac{\sum _{i=1}^n|y_i|^q}{p\sum_{j=1}^n |y_i|^q}
$$
As
$$
\frac{\sum _{i=1}^n|x_i|^p}{p\sum_{j=1}^n |x_i|^p}+\frac{\sum _{i=1}^n|y_i|^q}{p\sum_{j=1}^n |y_i|^q}=\frac{1} {p}+\frac{1} {q}=1
$$
It can be shorted as
$$
\frac{ \sum_{ j=1 }^n |x_i||y_i| } { \sqrt[p]{\sum_{j=1}^n |x_i|^p}\sqrt[q]{ \sum_{j=1}^n |y_i|^q} } \le 1
$$
So we can move the denominator to the RHS. This is the same as
$$
\sum_{j=1}^n |x_jy_j| \le (\sum_{j=1}^n |x_j|^p)^{ \frac{1} {p} }(\sum_{j=1}^n |x_j|^q)^{\frac{1}{q}}
$$
Now we've got Hölder's inequality!

### 4. From Hölder's inequality to Minkowski’s inequality

Let's move on from Hölder's inequality to Minkowski’s Inequality.

Also, Minkowski’s Inequality can be written like this:
$$
(\sum_{i=1}^n |x_i+y_i|^p)^\frac{1}{p} \le (\sum_{i=1}^n |x_i|^p)^\frac{1}{p}+(\sum_{i=1}^n |y_i|^p)^\frac{1}{p}
$$

#### Proof

The LHS can be written as
$$
(\sum_{i=1}^n |x_i+y_i|^{p-1}·|x_i|+\sum_{i=1}^n |x_i+y_i|^{p-1}·|y_i|)^\frac{1}{p}
$$
Applying Hölder's inequality, we can know that
$$
\sum_{i=1}^n |x_i+y_i|^{p-1}·|x_i| \le (\sum_{i=1}^n|x_i+y_i|^p)^\frac{p-1}{p}(\sum_{i=1}^n|x_i|^p)^\frac{1}{p}\space\space\space\space\space(As \space\space\space \frac{1}{p}+\frac{p-1}{p}=1)
$$
Similarly, we can have
$$
\sum_{i=1}^n |x_i+y_i|^{p-1}·|y_i| \le (\sum_{i=1}^n|x_i+y_i|^p)^\frac{p-1}{p}(\sum_{i=1}^n|y_i|^p)^\frac{1}{p}
$$
Add the two inequalities together, and we can get
$$
\sum_{i=1}^n |x_i+y_i|^{p-1}·|x_i|+\sum_{i=1}^n |x_i+y_i|^{p-1}·|y_i| \le (\sum_{i=1}^n|x_i+y_i|^p)^\frac{p-1}{p}(\sum_{i=1}^n|x_i|^p)^\frac{1}{p}+(\sum_{i=1}^n|x_i+y_i|^p)^\frac{p-1}{p}(\sum_{i=1}^n|y_i|^p)^\frac{1}{p}
$$
We can know that
$$
\sum_{i=1}^n |x_i+y_i|^p \le (\sum_{i=1}^n|x_i+y_i|^p)^\frac{p-1}{p}\space\space ((\sum_{i=1}^n|x_i|^p)^\frac{1}{p}+(\sum_{i=1}^n|y_i|^p)^\frac{1}{p})
$$
Finally, we can move the extra part on the RHS to the LHS, and we can get


$$
(\sum_{i=1}^n |x_i+y_i|^p)^\frac{1}{p} \le (\sum_{i=1}^n |x_i|^p)^\frac{1}{p}+(\sum_{i=1}^n |y_i|^p)^\frac{1}{p}
$$
Now we've got Minkowski’s inequality!

### 5. What these inequalities mean when combined with normed vector space

Brilliant readers may have noticed that all these inequalities can be used to deal with vectors. We can rewrite the inequality in a vector-like way by assuming vectors X and Y to be like
$$
X=(x_1,x_2,···,x_n),\space\space\space Y=(y_1,y_2,···,y_n)
$$
So we discover that we can define a new way to measure the distance like
$$
∥X∥_p=(\sum_{i=1}^n|x_i|^p)^\frac{1}{p}
$$
Note that ∥X∥p is only a way to note this is a different way of calculating distance instead of the traditional |X|.

According to Minkowski’s inequality
$$
∥X+Y∥_p \le ∥X∥_p +∥Y∥_p
$$
We can discover that this definition of distance works!

### 6. When p goes to infinity...

Well, in many cases, things get much more different when something goes to infinity. However, this definition still works when p goes to infinity!

We can prove that when p goes to infinity


$$
∥X∥_\infty = max \{ x_1,x_2,···.x_n \}
$$
This can be done quite easily using the X tilde.

#### Proof

We can put the distance into the limit
$$
\lim_{p\to\infty}∥X∥_p=\lim_ {p\to \infty} (\sum_{ i=1 } ^n|x_i|^p)^ \frac {1} {p}
$$
Then we introduce X tilde
$$
\widetilde x_i=\frac{ |x_i| } { \sqrt[p] {\sum_{j=1}^n |x_i|^p } }
$$
We can know that
$$
\lim_{ p\to\infty } ∥\tilde X∥ _p = \lim_{p\to \infty}(\sum_{ i=1 } ^n|\tilde x_i|^p)^\frac{ 1 } { p }
$$
And we know that, when 
$$
x_i< max \{ x_1,x_2,···,x_n \}
$$
then
$$
\tilde x_i<1
$$
So
$$
\lim_{ p\to \infty }(|\tilde x_i|^p)=0
$$
As
$$
\lim_{p\to \infty}(\sum_{ i=1 } ^n|\tilde x_i|^p)^\frac{ 1 } { p }=\lim_{p\to \infty}(\sum_{i=1}^n\lim_{p\to \infty}|\tilde x_i|^p)^ \frac { 1 } { p }
$$
And as
$$
\sum_{ i=1 } ^n\lim_{ p\to \infty } |\tilde x_i|^p \le n\space\space\space\space\space\space\space(As\space|\tilde x_i| \le1)
$$
And we can know a fact that
$$
\lim_{m\to\infty}\sqrt[m]{y}=1\space when\space y>0
$$
As
$$
0\le\sum_{i=1}^n\lim_{p\to \infty}|\tilde x_i|^p\le n
$$
Then applying the fact
$$
\lim_{p\to \infty}(\sum_{i=1}^n|\tilde x_i|^p)^\frac{1}{p}=\lim_{p\to \infty}(\sum_{i=1}^n\lim_{p\to \infty}|\tilde x_i|^p)^\frac{1}{p}=1
$$
So we can change tilde back to the normal form and finally get
$$
∥X∥_\infty=max\{ x_1,x_2,···.x_n \}
$$





## References

- VV285, slide. Horst Hohberger
- RC, slides. TA-Pingbang Hu
- RC, slides. TA-Chen Yuxiang

For further questions, you can contact me on wechat.

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230515231252742.png" alt="image-20230515231252742" style="zoom: 33%;" />

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20230605200315120.png" alt="image-20230605200315120" style="zoom:33%;" />
