---
title: 'topological entropy'
date: 2023-10-06
tags:
  - learning notes
  - dynamic system
---

（概要，待补充）
## the growth of orbit

$f: X \to X$ a map
$P_n(f)$ the total number of points for which the positive integer $n$ is a periodic
$\overline{P_n}(f)$ the total number of points for which the positive integer $n$ is the minimal periodic

## topological entropy
我们先将目光放到 紧致度量空间$(X,d)$
如何去度量一个拓扑系统的复杂度？
从直观上来说，轨道之间的差别越是接近，那么它们往往拥有相似的性质。
因此我们尝试建立拓扑熵的过程，正是在度量这个系统往微观前进时，轨道与轨道之间的差别的增长速度。如果这种速度可以被控制的话，我们也许就可以借此来了解这个动力系统的复杂度。
首先，我们需要先建立一些度量来刻画每一条轨道之间的距离
>**Def.**
>$$ d^f_n(x,y) = \max_{1 \le i \le n-1} d(f^i(x),f^i(x))$$

为了方便起见，我们记该度量下的开球
$$
B_f(x,\epsilon,n) = \{y \in X : d^f_n(x,y) < \epsilon\}
$$

>**Def.** $(\epsilon, n)$-spanning
> A set $E \subset X$ is a $(\epsilon, n)$-spanning if $X \subset \bigcup_{x \in E} B_f(x,\epsilon, n)$.
> Denote $S_d(f,\epsilon,n)$ as the minimal cardnality of a $(\epsilon, n)$-spanning

这个概念度量了给定$(\epsilon, n)$下各轨道之间分离的速度，由此可以考虑用一个函数来度量增长速度。
$$
h_d(f,\epsilon) = \overline {\lim_{n \to \infty} } \frac{1}{n} log S_d(f,\epsilon, n)
$$
注意到，$h_d(f,\epsilon)$ 并不会随着 $\epsilon$ 减小而减小，因此我们可以由此定义 topological entropy

>**Def.**
>$$h_d(f) = \lim_{\epsilon \to 0} h_d(f,\epsilon)$$

事实上，这个定义要比我们想象中更加依赖于 $f$ 本身，而对于度量 $d$ 的依赖，只是计算时的表象，事实上，并无过多关联。

>**Prop.**
>If $d'$ is another metric on $X$ which defines the same topology as $d$, then $h_{d'}(f) = h_d(f)$.

**proof.**
Consider the set $D_\epsilon = \{(x_1,x_2): x_1,x_2 \in X, d(x_1,x_2) \ge \epsilon\}$, which is a compact set.
Then, denote $\delta(\epsilon) = \min_{(x_1,x_2) \in D_\epsilon}d(x_1,x_2)$.
$\delta(\epsilon) > 0$ since $d'$ is a metric.
Thus, every $\delta(\epsilon)$-ball in matric $d'$ is contained in an $\epsilon$-ball in matric $d$.
This arguement extended to the metric $d^f_n$ and $d'^f_n$.
Then, we have $S_{d'}(f,\epsilon, n) \ge S_d(f,\epsilon, n), \forall n$.
And, $h_{d'}(f,\delta(\epsilon)) \ge h_d(f,\epsilon)$,
$$
 h_{d'}(f) \ge \lim_{\epsilon \to 0} h_{d'}(f,\delta(\epsilon)) \ge \lim_{\epsilon \to 0} h_d(f,\epsilon) = h_d (f)
$$
Similarly, we have $h_d(f) \ge h_{d'}(f)$.
Hence, $h_d(f) = h_{d'}(f)$.

由此，这种稳定性带给我们关于 topology entropy 的更加一般化的定义

>**Def.** topology entropy
>The quantity of topology $h_d(f)$ calculate on any metric on $X$ is called the *topology entropy* of $f$.
>Denoted as $h(f)$ or sometimes $h_{top}(f)$.

由于同胚会将给一个可度量化拓扑空间 “pull back” 一个新的度量，因此我们注意到，这个概念理应被同胚所保持。

>**Cor.**
>The topology entropy is an invariant of topology conjucate.

事实上，这个非常直接的构造，确实在一定程度上定义了拓扑系统的复杂程度，因为如果我们“删除”这个空间的一部分信息，拓扑熵不会增加。

>**Prop.**
>If the map $g$ is a factor of $f$, then $h_{top}(g) \le h_{top}(f)$.

**proof.**
Let $f:X \to X$, $g:Y \to Y$, $h:X \to Y$, $h \circ f = g \circ h$, $h(X) = Y$ and $d_X$, $d_Y$ are the coresponding distance function.
$h$ is uniformly continuous, so for any $\epsilon > 0$ there is $\delta(\epsilon) > 0$ such that if $d_X(x_1,x_2) < \delta(\epsilon)$, then $d_Y(h(x_1),h(x_2)) < \epsilon$. 
Thus, $$S_{d_X}(f,\delta(\epsilon),n) \ge S_{d_Y}(g,\epsilon,n)$$
Then, we obtain the result.

>**Prop.**
>(1) If $\Lambda$ is a closed $f$-invariant set, then $h_{top}(f|_{\Lambda}) \le h_{top}(f)$.
>(2) If $X = \bigcup_{i=1}^m \Lambda_i$, where $\Lambda_i$, $(i=1,\dots,m)$ are closed $f$-invriant sets, then $h_{top}(f) = \max_{1 \le i \le m} h_{top}(f|_{\Lambda_i})$.
>(3) $h_{top}(f^m) = |m|h_{top}(f)$
>(4) $h_{top}(f \times g) = h_{top}(f) + h_{top}(g)$.

Here if $f:X \to X$, $g:Y \to Y$, then $f \times g: X \times Y \to X \times Y$ is defined by $(f \times g)(x,y)=(f(x),g(y))$.

**proof.**
(1) Obvious by definition
(2) the union of covers of $\Lambda_1, \dots \Lambda_m$ by sets is also a covering of $X$. Then, we have
$$D_d(f,\epsilon,n) \le \sum_{i=1}^m D_d(f|_{\lambda_i}, \epsilon,n)$$
That is, there exist $i$ s.t.
$$D_d(f|_{\lambda_i}, \epsilon,n) \ge \frac{1}{m} D_d(f,\epsilon,n)$$
Since $m$ is finite, there must be one $i$ works for infinite $n$, then
$$\overline {\lim_{n \to \infty}}\frac{\log D_d(f|_{\Lambda_i}, \epsilon,n)}{n} \ge \overline {\lim_{n \to \infty}}\frac{\log D_d(f, \epsilon,n)- \log m}{n} = h_d(f,\epsilon)$$
which prove (2) by (1).


