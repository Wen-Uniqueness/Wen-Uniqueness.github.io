---
title: Holomorphic for zero of a holomorphism
date: 2023-04-01
tags:
  - notes
---

## Problem
> 待补充

We first prove $z_\epsilon$ is continuous.
$\forall \epsilon_0 \in D$,for any $r > 0$ such that $\overline{B(z_0, r)} = \{z : |z - z_0| \le r\}$ contained in $D$.
Denote $M =\sup_{z \in \overline {B(z_0,r)}} |g(z)|$, $m = \sup_{|z-z_0| = r}|f(z)|$, let $\delta = \frac{mr}{2M}$ 
for any $|\epsilon - \epsilon_0| < \delta$,  we have $|f(z)| > |\epsilon g(z)|, \forall |z - z_0| = r$.
then $f(z) + \epsilon g(z)$ have only one simple zero in $\overline{B(z_0, r)}$, that is $|z_\epsilon - z_{\epsilon_0}| < r$.
Hence, $z_\epsilon$ is continuous.

Now, we prove that $z_\epsilon$ is holomorphic on $D$.
对于$\epsilon \to z_\epsilon$，我们有如下恒等式
$$
f(z_\epsilon) + \epsilon g(z_\epsilon) \equiv 0
$$
$\forall \epsilon_0 \in D$，consider$f_{\epsilon_0} = f + \epsilon_0 g$. Since $f_{\epsilon_0} = f + \epsilon_0 g$ has only one simple zero in D.
Then, we can rewrite $f_{\epsilon_0}$ as$f_{\epsilon_0} = (x-z_{\epsilon_0})h_{\epsilon_0}(x)$, $h_{\epsilon_0}$ is holomorphic and nowhere vanish on $D$, and only depend on $\epsilon_0$. Then,
$$
\begin{eqnarray}
f(z_\epsilon) + \epsilon g(z_\epsilon) \equiv 0\\
f_{\epsilon _0} (z_\epsilon) + (\epsilon - {\epsilon _0}) g(z_\epsilon)\equiv0\\
(z_{\epsilon}-z_{\epsilon _0})h_{\epsilon _0}(z_\epsilon )+({\epsilon }-{\epsilon _0}) g(z_{\epsilon })\equiv0\\
\frac{z_{\epsilon}-z_{\epsilon _0}}{{\epsilon }-{\epsilon _0}} \equiv-\frac{g(z_\epsilon )}{h_{\epsilon _0}(z_\epsilon )} 

\end{eqnarray}
$$
Using continuity of $z_\epsilon$,
$$
\lim_{\epsilon \to \epsilon_0} \frac{z_{\epsilon}-z_{\epsilon _0}}{{\epsilon }-{\epsilon _0}} = \lim_{\epsilon \to \epsilon_0}-\frac{g(z_\epsilon )}{h_{\epsilon _0}(z_\epsilon )} =-\frac{g(lim_{\epsilon \to \epsilon_0}z_\epsilon )}{h_{\epsilon _0}(lim_{\epsilon \to \epsilon_0}z_\epsilon )}=-\frac{g(z_{\epsilon_0} )}{h_{\epsilon _0}(z_{\epsilon_0} )}
$$
That is, $z_{\epsilon}$is holomorphic at $\epsilon_0$.
Hence, $z_{\epsilon}$is holoporphic.