## Group

- **Set + one operation** (usually + or ×)
- **Requirements:**
  1. **Closure:** a*b ∈ G
  2. **Associativity:** (a*b)*c = a*(b*c)
  3. **Identity:** ∃ e such that e*a = a*e = a
  4. **Inverses:** ∀a, ∃a⁻¹ such that a*a⁻¹ = e
- **Examples:** (ℤ, +), (ℝ{0}, ×)

## Ring

- **Set + two operations** (+, ×)
- **Requirements:**
  1. **(G, +) is abelian group** (commutative)
  2. **× is associative**
  3. **Distributive:** a×(b+c) = a×b + a×c
- **May have:** × identity (1), × commutativity
- **Examples:** ℤ, matrices, polynomials

## Field

- **Set + two operations** (+, ×)
- **Requirements:**
  1. **(F, +) is abelian group**
  2. **(F{0}, ×) is abelian group**
  3. **Distributive laws hold**
- **Examples:** ℚ, ℝ, ℂ, ℤₚ (p prime)

## Vector Space

- **Set V over field K**
- **Requirements:**
  1. **(V, +) is abelian group**
  2. **Scalar multiplication:** K × V → V
  3. **8 axioms** from your PDF
- **Key:** Can add vectors, multiply by scalars
- **Examples:** ℝⁿ, polynomials, matrices

## Subspace

- **Subset W ⊆ V** where V is vector space over K
- **Quick check:**
  1. **0 ∈ W**
  2. **Closed under +:** u,v ∈ W ⇒ u+v ∈ W
  3. **Closed under ·:** a ∈ K, u ∈ W ⇒ a·u ∈ W
- **Even quicker:** Check a·u + b·v ∈ W for all a,b ∈ K, u,v ∈ W

## Memory Aid

- **Group:** One operation, all inverses
- **Ring:** Two operations, + has inverses, × may not
- **Field:** Two operations, both have inverses
- **Vector Space:** Vectors + scalars, geometric structure
- **Subspace:** Vector space within vector space

**Test for subspace:** "Can I do all vector operations here without leaving?"