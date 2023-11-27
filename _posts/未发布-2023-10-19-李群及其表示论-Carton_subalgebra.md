
$g$ a f.d. complex Lie algebra
If $h \subset g$ is a nilpotent subalgebra, $h$ is a group representation on $g$ as the adjoint 

$$g=L_0 \bigoplus \left( \bigoplus_{\lambda_i \not = 0} L_{\lambda_i} \right)$$

Where $L_0$ is the generalized weight space associated to the $0$-weight and $L_{\lambda}$ is the generalized weight space associated to the nonzero weight $\lambda_i$.

Obviously, $h \subset L_0$.

>**Def.**
>$h \subset g$ is called a Cartan subalgebra if $h$ is nilpotent and $N(h) := \{x \in g: [x,h] \subset h\}$ is equal to $h$.

**Remark.**
$N(h)$ is called the *normaliser* of $h$.
$N(h)$ is a Lie subalgebra.

Obviously, if $h$ is a Cartan subalgebra, then $h=L_0$. Otherwise, $h \subsetneq L_0$, $L_0 / h$ is an $h$-module whose only weight is $0$ and hence has a nontrivial $0$-weight space $M/h$ where $M \subset L_0$. So, $[h,M] \subset h \Rightarrow N(h) \supset M \supsetneq h$, an contraction.
Conversely, $h=L_0$ implies $h$ is a Cartan subalgebra.


**Obs.**
$$[L_0,L_{\lambda_i}] \subset L_{\lambda_i}$$
$$[L_{\lambda_i},L_{\lambda_j}] \subset L_{\lambda_i + \lambda_j}$$

Actually, suppose $y \in L_{\lambda_i}, z \in L_{\lambda_j}$.

**Obs.**
when $h$ is a Cartan subalgebra
$$g = h \bigoplus(\bigoplus_{\lambda_i \not= 0} L_{\lambda_i})$$
for $x \in h$, the generalized eigenspace of $\mathrm{ad}x$ with eigenvalue $0$.
Thus, when all $\lambda_i(x)$ are nonzero, 

>**Def.**
>for $x \in g$
>Put $L_{0,x}$ $=$ the generalized eigenspace of $\mathrm{ad}x$ with eigenvalue $0$

>**Def.**
>$x \in g$ is called *regular* if
>$L_{0,x}=\min_{y \in g} L_{0,y}$

>**Thm.**
>$g$ a f.d. complex Lie algebra
>1. if $x \subset g$ is regular, then $L_{0,x}$ is a Cartan subalgebra.
>2. if $h$ is a Cartan subalgebra ,then $\exists$ regular element $x$ s.t. $h=L_{0,x}$
>3. if $h_1$, $h_2$ are two Cartan subalgebras then $\exists \sigma \in \mathrm{Inn}(g) \subset \mathrm{Aut}(g)$ s.t. $\sigma (h_1) = h_2$.

Obvious that $\mathrm{ad}x [y,z] = [(\mathrm{ad}x)y,z] + [y, (\mathrm{ad}x)z]$, then we add two definition.

>**Def.**
>a linear map $\delta: g \to g$ is called a derivation if $$\delta[y,z]=[\delta y , z] + [y , \delta z]$$

>**Def.**
>$\mathrm{Inn}(g) = <\exp(\mathrm{ad}x):\mathrm{ad}x \text{ is nilpotent}>$

*proof of thm*
for (1),
Suppose $x$ is regular.
Obviously, $L_{0,x}$ is a subalgebra.
Also, it's clear that $N(L_{0,x}) = L_{0,x}$.
we now check that $L_{0,x}$ is nulpotent.
By Engel's theorem, it amounts to show that $\mathrm{ad}y$ is nilpotent, $y \in L_{0,x}$. 


### C
After choosing a Cartan subalgebra $h$, we obtain a decomposition
$$g=h \oplus\left( \bigoplus_{\alpha \in \Phi}L_{\alpha} \right)$$
then we have the action $h$ on $g$ and $L_\alpha$ is the generalized weight space with weight $\alpha$. And, we have
$$[h,L_\alpha] \subseteq L_\alpha$$
$$[h,h] \subseteq h$$
$$[L_\alpha,L_\beta] \subseteq L_{\alpha+\beta}$$

Obs.
$$ 0 \gets L_{-p \alpha +\beta} \gets \cdots \gets L_{-\alpha + \beta} \overset{[L_{-\alpha},\cdot]}{\leftarrow}   L_\beta \overset{[L_{\alpha},\cdot]}{\rightarrow} L_{\alpha +\beta} \to \cdots \to L_{q \alpha + \beta} \to 0$$
let $p\in N \cup \{0\}$ be such that $L_{-p \alpha + \beta}, \dots, L_\beta$ are all nonzero, and $L_{-(p+1) \alpha + \beta} = 0$.
let $q\in N \cup \{0\}$ be such that $L_{q \alpha + \beta}, \dots, L_\beta$ are all nonzero, and $L_{(q+1) \alpha + \beta} = 0$.

If $\rho(X)$ and $\rho(Y)$ have zero trace, then $\rho([X,Y])$ also have a zero trace. 
Thus, for $X \in L_\alpha, Y \in L_{-\alpha}$, 
$$Tr(\mathrm{ad}_{[X,Y]}|_V) = Tr([\mathrm{ad}_X,\mathrm{ad}_Y]|_V) = 0$$
where $V = \bigoplus_{i=-p}^q L_{i \alpha +\beta}$
That is, 
$$\sum_{i = -p}^q \left(i \alpha([X,Y]) + \beta([X,Y])\right)\dim L_{i\alpha + \beta} = 0$$
Hence, $$\beta([X,Y]) = \frac{-\sum_{i = -p}^q i \dim L_{i\alpha + \beta}}{\sum_{i = -p}^q \dim L_{i\alpha + \beta}} \alpha([X,Y])$$
Or, we can write that
$$\beta([X,Y]) = \text{(rational number)} \cdot \alpha([X,Y])$$

---
Now, suppose $g$ is s.simple, i.e. the [killing form](_posts/2023-10-12-李群及其表示论-killing_form.md) $< \, , \, >$ on $g$ is non-degenerate.

Obs 1.
$$\alpha + \beta \not = 0 \Rightarrow L_{\alpha} \perp L_{\beta}$$
For $x \in L_\alpha, Y \in L_\beta$, $<X,Y>=\mathrm{Tr}(\mathrm{ad}_X\mathrm{ad}_Y)$
When $\alpha + \beta \not=0$, $\mathrm{ad}_X\mathrm{ad}_Y$ change every conponent, that is there is a basis such that $\mathrm{ad}_X\mathrm{ad}_Y$ is $0$ on diagram.

Obs 2.
for $X,Y \in h$, 
$$\begin{eqnarray}
<X,Y> & = & \mathrm{Tr}(\mathrm{ad}_X\mathrm{ad}_Y) \\& = & \sum_{\alpha \in \Phi}\alpha (X) \alpha(Y) \cdot \dim L_\alpha
\end{eqnarray}$$
recall that w.n.t. the action of $h$ on $L-\alpha$, onr may choose a basis of $L_\alpha$ so that elements $x \in h$ act on of the form
$$
\begin{pmatrix}
 \alpha(X) & * & *\\
  & \ddots & *\\
  &  & \alpha(X)
\end{pmatrix}
$$
Since all $\alpha \in \Phi$ vanish on $[h,h]$, we have $[h,h] \perp h$. This implies $[h,h]=0$ since $<,>|_{h \times h}$ is non-degenerate, so $h$ is abelian.

Obs 3.
At this moment
$$\begin{eqnarray}
h & \simeq & h^*\\
x & \mapsto & <x, \cdot>\\
h_\alpha & & \alpha
\end{eqnarray}$$

for $\alpha \in \Phi$, let $h_\alpha '$ be the element in $h$ corresponding to $\alpha$

claim:
$$h_\alpha' \in [L_\alpha,L_{-\alpha}]$$
$$<h_\alpha ',h_\alpha '> \not = 0$$
$$\dim L_{\alpha} = \dim L_{-\alpha} = 1$$

i)
let $e_{\alpha} \in L_{\alpha}$ be a nonzero vector of weight $\alpha$. Then, $[e_\alpha, L_{-\alpha}]$ would produce
for any $Y \in L_{-\alpha}$, 
$$<[e_\alpha, L_{-\alpha}], Z> = <Y,-[e_\alpha, Z]>=\text{(skip some step)}=<Z,h_\alpha'><Y,e_\alpha>$$
Thus, $[e_\alpha, Y] = <Y,e_\alpha>h_\alpha'$
Because $<,>|_{L_\alpha \times L_{-\alpha}}$ is perfect, $\exists Y \in L_{-\alpha}$ s.t. $<Y,e_\alpha> \not = 0$, then $h_\alpha' \in \frac{[e_\alpha,Y]}{<Y,e_\alpha>} \in [e_\alpha, L_{-\alpha}]$

ii)
Otherwise, $\alpha(h_\alpha')=0$
By Obs 0, $\beta(h_\alpha') = 0$ for all $\beta \in \Phi$.
Because $\Phi$ span $h^*$, there should be $h_\alpha'=0$.
This is a contracdiction.

iii)
Consider $U = \mathbb C \oplus [e_\alpha,L_{-\alpha}] \oplus L_{-\alpha} \oplus L_{-2 \alpha} \oplus \cdots \oplus L_{-p \alpha}$
It is invariant under the action of $\mathbb C e_\alpha$,$[e_\alpha, L_{-\alpha}]$ and $L_{-\alpha}$.
Thus, for $Y \in L_{-\alpha}$, $0=\mathrm{Tr}(\mathrm{ad}_{[e_\alpha,Y]}|_U)=\alpha([e_\alpha,Y]) + \sum_i \dim L_{-i\alpha}(-i\alpha ([e_\alpha,Y]))$.


Obs 4.
$$<h_\alpha', h_\beta'> = ?$$
$$<h_\alpha', h_\beta'> = \beta(h_\alpha')=\frac{-\sum_{i = -p}^q i \dim L_{i\alpha + \beta}}{\sum_{i = -p}^q \dim L_{i\alpha + \beta}} \alpha(h_\alpha')=\frac{p-q}{2} <h_\alpha',h_\alpha'>$$
That is, 
$$2\frac{<h_\alpha',h_\beta'>}{<h_\alpha',h_\alpha'>}=p-q$$

**Cor 1**
suppose $\alpha \in \Phi$, then $\mathbb Z \alpha \cap \Phi = \{\pm \alpha\}$

**Cor 1'**
suppose $\alpha \in \Phi$, then $\mathbb C \alpha \cap \Phi = \{\pm \alpha\}$

*proof of Cor 1*.
Suppose $c \alpha \in \Phi$ and $c \in \mathbb Z \backslash \{0\}$, then obs 4 tells $c = \frac{p-q}{2}$.  
when $c \in \mathbb Z$, it is already proved (b.c. we have shown
$$1 = \dim L_{-\alpha} + 2 \dim L_{-2 \alpha} + \cdots + p \dim L_{-p \alpha}$$
Hence, $L_{2 \alpha}, L_{3 \alpha}, \dots = 0$ )
when $c \in \frac{\text{odd integers}}{2}$, the chaim

**Cor 2**.
$<h_\alpha', h_\beta'> \in \mathbb Q, \alpha,\beta \in\Phi$

*proof.*
$$
<h_\alpha',h_\alpha'> = \sum_{\beta \in \Phi} \beta(h_\alpha')\beta(h_\alpha') \dim L_\beta
$$
Then, 
$$
\frac{1}{<h_\alpha',h_\alpha'>} = \sum_{\beta \in \Phi} \left(\frac{<h_\alpha',h_\beta'>}{<h_\alpha',h_\alpha'>}\right)^2 \dim L_\beta \in \mathbb Q
$$

Thus,