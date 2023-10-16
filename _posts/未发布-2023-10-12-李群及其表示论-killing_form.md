
$g$ a f.d. Lie algebra over $\mathbb C$
The adjoint representation 
$$
\begin{eqnarray}
g &\to& \mathrm{End(g)}\\
x& \mapsto& \mathrm{ad}_x : y \mapsto [x,y]
\end{eqnarray}
$$

The Killing form $B(x,y) = \mathrm{Tr} (\mathrm {ad}_x \mathrm {ad}_y)$
it is a symmetric bilinear pairing, satisfying the "invariance property"
$$
B([z,x],y) + B(x,[z,y]) = 0
$$

**Recall.**
[sovable]() Lie algebra
[nilpotent]() Lie algebra

>**Lemma.**
>$g$ a f.d. complex Lie algebra,
>Then, $g$ has a unique maximal solvable ideal and a unique maximal nilpotent ideal

*proof.*
Obs 1: if $a,b \subset g$ are solvable ideals then $a+b$ is solvable

Obs2: If $a,b$ are nilpotent ideals of maximal dimension
$a+b$ is solvable and a solvable Lie algebra has a unique maximal nilpotent ideal, which contais both $a$ and $b$


---
>**Def.**
>$g$ a f.d. complex Lie algebra
>$g$ is called *s.simple* if $\mathrm{rad} g = 0$
>*simple* if it has nontrival ideal

**Remark.**
if $g$ is a nontrival simple Lie algebra, then $[g,g]=g$

Let $g$ be a f.d. complex Lie algebra, then $g/\mathrm{rad}g$ is s.simple.
It can be proved later that there is aa Lie subalgebra $h\simeq g/\mathrm{rad}g$ s.t. $g\simeq \mathrm{rad} g \oplus h$ as v.s


>**Thm.**
>let $g$ be a f.d. complex Lie algebra
>Then
>1 $g$ is solvable iff $[g,g] \subset \mathrm{rad}B:=g^{\bot } = \{x \in g : B(x,u)=0,\forall u \in g\}$
>1' $[g,g]^\bot = \mathrm{rad}g$
>2 $g$ is s.simple $\Leftrightarrow$ $b$ is non-degenerate

As a consequence, $g$ is s.simple iff it's the direct sum of nontrival simple Lie algebras

*proof.*
1 $\Rightarrow$: suppose $g$ is solvable, we will


---
>**Lemma.**
>$g$ a f.d. complex Lie algebra
>(1) if $a \subset g$ is an ideal, then $a^\bot$ is an ideal and $B_g|_{a\times a} = B_a$
>(2) if $a,b$ are ideals of $g$ and $g=a\oplus b$, then $B_g=B_a\oplus B_b$