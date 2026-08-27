## Summary Linalg Lucas Winter



### Definition:
Let C and C' be \(r \times s\) matrices with finitely many entries in F, C and C' are row equivalent if C' cna be obtained by finitely many elementary row operations on C.

---

### Definition:

A \(m \times n\) matrix A is called row-reduced if the folowing two conditions hold:

- The 1'st non-zero entry in each non-zero row of A is 1
- Each colomn of A which contains the leading non-zero entry of some row has all it's other entries 0.


\[
A=
\begin{pmatrix}
0&0&0&1&2\\
0&1&-3&0&\tfrac12\\
0&0&0&0&0
\end{pmatrix}
\]

✓ **Row reduced**

---

\[
B=
\begin{pmatrix}
1&0&0&0\\
0&1&-1&0\\
0&0&1&0
\end{pmatrix}
\]

✗ **Not row reduced**

---

\[
C=
\begin{pmatrix}
0&2&1\\
1&0&-3\\
0&0&0
\end{pmatrix}
\]

✗ **Not row reduced**

---

\[
D=
\begin{pmatrix}
0&0&1&1\\
1&0&0&2\\
0&1&0&5
\end{pmatrix}
\]

✓ **Row reduced**

---

### THM

Every matrix can be transformed, using elementary row operations, into a row-reduced matrix. <=> No matter what matrix you start with, Gaussian elimination will eventually produce a row-reduced form.

---

### Definition

An \(m \times n\) matrix \(A\) is called **row-reduced echelon** if the following hold:

- \(A\) is row reduced.
- Every row of \(A\) whose entries are all \(0\) appears below every row with a nonzero entry.
- If rows \(1,\ldots,r\) are the nonzero rows of \(A\), and if the leading nonzero entry of row \(i\) occurs in column \(k_i\) (\(i=1,\ldots,r\)), then \(k_1 < k_2 < \cdots < k_r\).

\[
I=
\begin{pmatrix}
1&*&*&*\\
0&1&*&*\\
0&0&1&*
\end{pmatrix}
\]

---

### THM 

Every \(m \times n\) matrix can be transformed into a row-reduced echelon matrix using elementary row operations.

---

### Definition

A vector space over a field \(K\) is a set \(V\), endowed with two operations:

- \(+ : V \times V \to V,\quad (v_1,v_2)\mapsto v_1+v_2\)
- \(\cdot : K \times V \to V,\quad (a,v)\mapsto a\cdot v\)

such that the following conditions (axioms) hold:

- **(V1)** For all \(v_1,v_2,v_3\in V\): \(v_1+(v_2+v_3)=(v_1+v_2)+v_3\).
- **(V2)** There exists an element \(0\in V\) such that \(0+v=v\) for all \(v\in V\).
- **(V3)** For every \(v\in V\), there exists \(v'\in V\) such that \(v+v'=0\).
- **(V4)** For all \(v_1,v_2\in V\): \(v_1+v_2=v_2+v_1\).
- **(V5)** For all \(a,b\in K\) and \(v\in V\): \(a\cdot(b\cdot v)=(ab)\cdot v\).
- **(V6)** For every \(v\in V\): \(1\cdot v=v\).
- **(V7)** For all \(a\in K\) and \(v_1,v_2\in V\): \(a(v_1+v_2)=av_1+av_2\).
- **(V8)** For all \(a_1,a_2\in K\) and \(v\in V\): \((a_1+a_2)v=a_1v+a_2v\).

---

### Definition

Let \(V\) be a vector space over \(K\). A subset \(W \subseteq V\) is called a **linear subspace** of \(V\) (or simply a **subspace** of \(V\)) if the following hold:

- **(LSS1)** \(W \neq \varnothing\).
- **(LSS2)** For all \(w_1,w_2 \in W\), we have \(w_1+w_2 \in W\).
- **(LSS3)** For all \(a \in K\) and \(w \in W\), we have \(a\cdot w \in W\).

<=>

\- **(LSS1)** \(0_V \in W\).

\- **(LSS2)** For all \(a_1,a_2 \in K\) and \(w_1,w_2 \in W\), we have \(a_1w_1 + a_2w_2 \in W\)

---

### Definition of Span

Let \(S \subseteq V\).

The **span** of \(S\), denoted \(\operatorname{Sp}(S)\), is the smallest subspace of \(V\) that contains \(S\).

Equivalently,

\[
\operatorname{Sp}(S)
=
\bigcap
\{\,W \subseteq V
\mid
W \text{ is a subspace of } V
\text{ and }
S \subseteq W
\,\}.
\]

$$
\operatorname{Sp}(\varnothing) = 0_v
$$

---

### Definition

Let \(V\) be a vector space over \(K\) and \(S \subseteq V\). We say that \(S\) **generates** (or **spans**) \(V\) if \(\operatorname{Sp}(S)=V\). In this case, \(S\) is called a **generating set** of \(V\).

More generally, if \(\operatorname{Sp}(S)=W\), where \(W \subseteq V\) is a subspace of \(V\), then we say that \(S\) **generates** (or **spans**) \(W\).

---

### Definition

A vector space \(V\) is called **finite-dimensional** if there exists a finite set \(S \subseteq V\) such that \(\operatorname{Sp}(S)=V\).

Otherwise, \(V\) is called **infinite-dimensional**.

---

### Definition

Let \(v_1,\ldots,v_n\) be a list of \(n\) vectors in \(V\). We say that \(v_1,\ldots,v_n\) are **linearly independent** if the only linear combination of \(v_1,\ldots,v_n\) that gives \(0 \in V\) is the one with \(0\)-coefficients.

Equivalently: if \(a_1v_1+\cdots+a_nv_n=0\), then \(a_1=\cdots=a_n=0\).

---

### Definition

Let \(v_1,\ldots,v_n\) be a list of \(n\) vectors in \(V\).

We say that \(v_1,\ldots,v_n\) are **linearly independent** if the only linear combination of \(v_1,\ldots,v_n\) that gives \(0 \in V\) is the one with \(0\)-coefficients.

Equivalently: if \(a_1v_1+\cdots+a_nv_n=0\), then \(a_1=\cdots=a_n=0\).

---

### Convenvention

the empty set is linearly independent.

---

### Definition

A subset \(S \subseteq V\) is called a **basis** of \(V\) if:

1. \(S\) is linearly independent.
2. \(S\) spans / generates \(V\), i.e. \(\operatorname{Sp}(S)=V\).

---

### Proposition

A subset \(S \subseteq V\) is called a basis of \(V\) iff every \(v \in V\) can be written in a unique way as a linear combination of vectors in \(S\).

---

### Theorem

Let \(V\) be a finite dimensional vector space over \(K\). Then \(V\)  has a basis with finitely many elements. Moreover, every basis of \(V\) is finite and has the same number of elements.

---

### Definition

Let \(V\) be a finite-dimensional vector space over \(K\). The **dimension** of \(V\) is the number \(n \in \mathbb{Z}_{\ge 0}\) of elements in any basis of \(V\). We write \(\dim(V)=n\). If \(V\) is not finite-dimensional, we write \(\dim(V)=\infty\).

**Remark:** \(\dim\{0\}=0\), because \(\varnothing\) is a basis of the zero vector space \(\{0\}\), and \(|\varnothing|=0\).

---

### Definition

Let \(A \in M_{m\times n}(K)\). Let \(u_1,\ldots,u_m \in K^n\) be the rows of \(A\), and \(v_1,\ldots,v_n \in K^m\) be the columns of \(A\).
\[
A=
\begin{pmatrix}
- u_1 -\\
\vdots\\
- u_m -
\end{pmatrix}
=
\begin{pmatrix}
| & & |\\
v_1 & \cdots & v_n\\
| & & |
\end{pmatrix}.
\]

**Row space.** \(\mathrm{RowS}(A):=\mathrm{Sp}(u_1,\ldots,u_m)\subseteq K^n\), where vectors are viewed as row vectors.

**Column space.** \(\mathrm{ColS}(A):=\mathrm{Sp}(v_1,\ldots,v_n)\subseteq K^m\), where vectors are viewed as column vectors.

---

### Lemma 

If \(A,B\in M_{m\times n}(K)\) are row-equivalent matrices, then
\[
\mathrm{RowS}(A)=\mathrm{RowS}(B).
\]
**Remark:** the Lemma does not hold for Cosl.

---

### Definition

Let \(A\in M_{m\times n}(K)\).

**Row rank.** \(\operatorname{row\text{-}rank}(A):=\dim(\operatorname{RowS}(A))\).

**Column rank.** \(\operatorname{col\text{-}rank}(A):=\dim(\operatorname{ColS}(A))\).

**Remark.** Later we will prove that \(\operatorname{row\text{-}rank}(A)=\operatorname{col\text{-}rank}(A)\).

---

### Corollary

The number of pivots that one obtains after applying the Gauss elimination procedure, is independant from the chosen steps in the procedure.

---

### Some simple properties

For every \(A,B \in M_{m\times n}(K)\), \(\lambda \in K\), we have:

1. \((A+B)^T = A^T + B^T\).
2. \((\lambda A)^T = \lambda A^T\).
3. \((A^T)^T = A\).
4. \(\operatorname{RowS}(A^T) = \operatorname{ColS}(A)\), and \(\operatorname{ColS}(A^T) = \operatorname{RowS}(A)\).

---

### Definition

Let \(V\) be a vector space over \(K\) and \(U \leq V\) a subspace. A subspace \(W \leq V\) is called a **complement** of \(U\) if \(U+W=V\) and \(U\cap W=\{0\}\). (Equivalently: \(V=U\oplus W\).)

---

### Good to know words:

- **Linear map** = Linear transofrmation = **homomorphisms** of vector spaces
- **bijective linear map** = **invertible** linear transformation = **isomorphism**
- linear map from \(V\) to \(V\) is called an **endomorphism** <=> \(\operatorname{End}(V) = \operatorname{Hom}(V,V)\)
- T is injective = **monomorphism**
- T is surjective = **epimorphism**

---

### Definition

Let \(V\) and \(W\) be vector spaces over \(K\). A map \(T:V\to W\) is called a **linear map** if:

1. \(T(v_1+v_2)=T(v_1)+T(v_2)\) for all \(v_1,v_2\in V\).
2. \(T(a\cdot v)=a\cdot T(v)\) for all \(a\in K\) and \(v\in V\).

We denote the set of all linear maps \(T:V\to W\) by \(\operatorname{Hom}_K(V,W)\) or \(\operatorname{Hom}(V,W)\). One also sees \(\operatorname{Lin}(V,W)\), \(\operatorname{hom}_K(V,W)\), etc.

---

### Lemma

Composition of multiple linear maps are also linear.

---

### Theorem (Rank Theorem)

Let T:V→W be a linear map, where V is finite dimensional, then:
$$
dim(Ker(T)) + dim(Im(T)) = dim(V)
$$

---

### Corollary

Let \(T:V\to W\) be a linear map, where \(V\) and \(W\) are finite-dimensional vector spaces.

1. If \(\dim(W)<\dim(V)\), then \(T\) is **not injective**.

2. If \(\dim(W)>\dim(V)\), then \(T\) is **not surjective**.

3. If \(\dim(W)=\dim(V)\), then \(T\) is bijective \(\Longleftrightarrow\) \(T\) is injective \(\Longleftrightarrow\) \(T\) is surjective.

---

### Corollary

Two finite dimensional vector spaces \(V\) and \(W\) are isomorphic iff \(dim(V) = dim(W)\)

---

### Definition

Let T:V→W be a linear map. We define the rank of \(T\) By: \(rank(T) := dim(Im(T))\)

---

### Definition

An \(n\times n\) matrix \(A \in M_{n\times n}(K)\) is called **invertible** if there exists a matrix \(B \in M_{n\times n}(K)\) such that \(AB = BA = I_n\).

---

### Lemma

Let \(A,B\) be two diagonal matrices (respectively both upper triangular, respectively both lower triangular). Then \(AB\) is of the same type.

---

### Definition

Let \(A,B\in M_{m\times n}(K)\). We say that \(A\) and \(B\) are **equivalent** if there exist \(P\in GL_m(K)\) and \(Q\in GL_n(K)\) such that \(B=PAQ.\)

Let \(A,B\in M_{n\times n}(K)\). We say that \(A\) and \(B\) are **similar** if there exists \(P\in GL_n(K)\) such that \(B=P^{-1}AP.\)

---

### Corollary

Let \(A,B\in M_{m\times n}(K)\). Then \(A\sim B\) if and only if \(\operatorname{rank}(A)=\operatorname{rank}(B)\).

Moreover, for every \(0\le r\le \min\{m,n\}\), there is precisely one equivalence class of matrices of rank \(r\).

---

### Theorem

Let \(A\in M_{m\times n}(K)\). Then \(\operatorname{colrank}(A)=\operatorname{rowrank}(A)\).

---

### Remark by Lucas

Rank is always the same as the row rank or column rank of a matrix: \(\operatorname{rank}(A)=\operatorname{colrank}(A)=\operatorname{rowrank}(A)\).

However, this does **not** mean that the column space and row space are the same: \(\operatorname{ColS}(A)\neq \operatorname{RowS}(A)\) in general. They merely have the same dimension: \(\dim(\operatorname{ColS}(A))=\dim(\operatorname{RowS}(A))=\operatorname{rank}(A)\).

---

### Proposition

Let \(A\in M_{m\times n}(K)\) and \(b\in K^m\). Then \(Ax=b\) has a solution if and only if \(\operatorname{rank}(A|b)=\operatorname{rank}(A)\).
