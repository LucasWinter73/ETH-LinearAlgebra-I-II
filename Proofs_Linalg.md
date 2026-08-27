## Theorem (Rank Theorem) (15.b.9)

Let $T:V\to W$ be a linear map, where $V$ is finite-dimensional. Then $\dim\ker(T)+\dim\operatorname{Im}(T)=\dim V$.

### Proof

Write $n:=\dim V$. Let $u_1,\ldots,u_k$ be a basis for $\ker(T)$.

(Since $\ker(T)$ is a subspace of $V$, it is also finite-dimensional.)

Extend $u_1,\ldots,u_k$ to a basis $u_1,\ldots,u_k,v_1,\ldots,v_{n-k}$ of $V$.

By Lemma **(15.b.8)** we have $\operatorname{Im}(T)=\operatorname{Sp}(Tu_1,\ldots,Tu_k,Tv_1,\ldots,Tv_{n-k})=\operatorname{Sp}(Tv_1,\ldots,Tv_{n-k})$, since $Tu_1=\cdots=Tu_k=0$.

We claim that $Tv_1,\ldots,Tv_{n-k}$ form a basis for $\operatorname{Im}(T)$.

Indeed, we have just proved that $Tv_1,\ldots,Tv_{n-k}$ span $\operatorname{Im}(T)$, so it remains to show that they are linearly independent.

Let $a_1,\ldots,a_{n-k}\in K$ and assume $\sum_{i=1}^{n-k}a_iTv_i=0$.

Since $T$ is linear, $T\left(\sum_{i=1}^{n-k}a_iv_i\right)=\sum_{i=1}^{n-k}a_iTv_i=0$.

Hence $\sum_{i=1}^{n-k}a_iv_i\in\ker(T)$.

Since $u_1,\ldots,u_k$ is a basis of $\ker(T)$, there exist $b_1,\ldots,b_k\in K$ such that $a_1v_1+\cdots+a_{n-k}v_{n-k}=b_1u_1+\cdots+b_ku_k$.

Therefore $a_1v_1+\cdots+a_{n-k}v_{n-k}-b_1u_1-\cdots-b_ku_k=0$.

But $u_1,\ldots,u_k,v_1,\ldots,v_{n-k}$ is a basis of $V$, hence linearly independent.

Therefore $a_1=\cdots=a_{n-k}=0$ and $b_1=\cdots=b_k=0$. This proves that $Tv_1,\ldots,Tv_{n-k}$ form a basis for $\operatorname{Im}(T)$.

Hence $\dim\operatorname{Im}(T)=n-k=\dim V-\dim\ker(T)$.

Therefore $\dim\ker(T)+\dim\operatorname{Im}(T)=\dim V$.

## Lemma (18.a.7)

The elements $v_1^*,\ldots,v_n^*\in V^*$ form a basis for $V^*$. This basis is called the **dual basis** to $\mathcal B$.

We denote this basis by $\mathcal B^*=(v_1^*,\ldots,v_n^*)$.

Moreover, for every $f\in V^*$,

$f=\sum_{i=1}^n f(v_i)\,v_i^*$.

### Proof

Let $f\in V^*$. We claim that $f=\sum_{i=1}^n f(v_i)\,v_i^*$. (1)

Or, in other words, we claim that for every $v\in V$,

$f(v)=\sum_{i=1}^n f(v_i)\,v_i^*(v)$. (2)

Indeed, both sides of (1) are linear maps $V\to K$, so it is enough to check that (2) holds for $v=v_1,v=v_2,\ldots,v=v_n$, because $v_1,\ldots,v_n$ form a basis for $V$.

For $v=v_k$ we have

$\sum_{i=1}^n f(v_i)\,v_i^*(v_k)=\sum_{i=1}^n f(v_i)\,\delta_{ik}=f(v_k)$.

The claim just proved shows that $v_1^*,\ldots,v_n^*$ span $V^*$.

Since $\dim V^*=\dim V=n$, it follows that $v_1^*,\ldots,v_n^*$ form a basis for $V^*$.

## Lemma & Definition (18.a.9)

Let $V,W$ be vector spaces over $K$. Let $T:V\to W$ be a linear map. Define a new map $T^*:W^*\to V^*$ by $T^*(\ell):=\ell\circ T$ for every $\ell\in W^*$ (i.e. $\ell:W\to K$).

Then $T^*$ is a linear map. It is called the **dual map** to $T$.

### Proof

Let $\ell\in W^*$, i.e. $\ell:W\to K$ is linear. Clearly $\ell\circ T:V\to K$ is a linear map (because both $T$ and $\ell$ are), so $T^*(\ell):=\ell\circ T\in V^*$. This shows that $T^*:W^*\to V^*$ indeed has target $V^*$.

We now show that $T^*$ is linear.

Let $\ell\in W^*$ and $\alpha\in K$. For every $v\in V$,

$T^*(\alpha\ell)(v)=((\alpha\ell)\circ T)(v)=(\alpha\ell)(Tv)=\alpha\,\ell(Tv)=\alpha\,(\ell\circ T)(v)=\alpha\,T^*(\ell)(v)$.

Hence $T^*(\alpha\ell)=\alpha\,T^*(\ell)$.

Similarly,

$T^*(\ell_1+\ell_2)=T^*(\ell_1)+T^*(\ell_2)$.

Therefore $T^*$ is linear.

## Lemma (18.a.11)

Let $S:V\to W$ be a linear map between two finite-dimensional vector spaces over $K$. Let $\mathcal B$ be a basis for $V$ and $\mathcal C$ a basis for $W$. Consider $S^*:W^*\to V^*$ and the bases $\mathcal C^*,\mathcal B^*$ for $W^*,V^*$, respectively. Then

$[S^*]_{\mathcal B^*}^{\mathcal C^*}=([S]_{\mathcal C}^{\mathcal B})^T$.

### Proof

Write $\mathcal B=(v_1,\ldots,v_n)$ and $\mathcal C=(w_1,\ldots,w_m)$.

Let $A:=[S]_{\mathcal C}^{\mathcal B}=(a_{ij})$. Then

$Sv_j=\sum_{i=1}^m a_{ij}w_i$.

Now let $w_j^*\in\mathcal C^*$. We have

$S^*w_j^*=w_j^*\circ S=\sum_{i=1}^n(w_j^*\circ S)(v_i)\,v_i^*=\sum_{i=1}^n w_j^*(Sv_i)\,v_i^*$

by Lemma (18.a.7).

Since $Sv_i=\sum_{k=1}^m a_{ki}w_k$,

$S^*w_j^*=\sum_{i=1}^n w_j^*\!\left(\sum_{k=1}^m a_{ki}w_k\right)v_i^*=\sum_{i=1}^n a_{ji}v_i^*$,

because $w_j^*(w_k)=\delta_{jk}$.

Hence the coordinates of $S^*w_j^*$ in the basis $\mathcal B^*$ are

$(a_{j1},\ldots,a_{jn})^T$,

which is the $j$-th row of $A$, written as a column, i.e. the $j$-th column of $A^T$.

Therefore

$[S^*]_{\mathcal B^*}^{\mathcal C^*}=A^T=([S]_{\mathcal C}^{\mathcal B})^T$.