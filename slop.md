


# The Fine-Structure Constant from Categorical Self-Description

## Abstract

We derive the integer $p = 69$ from a finite self-description problem governed by two principles — Naturality (full permutation invariance) and Parsimony (elimination of anonymous multiplicity) — applied at two layers: categorical structure and symbolic encoding. At the structural layer, the principles yield the codiscrete category $C_p$: exactly one morphism per ordered pair. At the encoding layer, the same principles yield an alphabet-bijective serialization of the first compositional nerve data $(p^2, p^3)$. The unique solution at minimal base is $p = 69$, $b = 10$. We then conjecture that the inverse fine-structure constant equals the stabilized inverse Euler–Maclaurin defect of the canonical $69$-point mesh:

$$\alpha^{-1} = \frac{1}{\mathrm{Td}(1/69) - 1} - (1 - e^{-1}) + \frac{\pi}{69^2} - \frac{\pi^2}{3 \cdot 69^3} - \cdots$$

The three-term truncation gives $137.036\,0$; CODATA 2022 reports $137.035\,999\,177(21)$. The formula has zero adjustable parameters.

---

## 1. Introduction

A single motif drives this paper: **anonymous multiplicity is redundancy**. When full permutation symmetry renders copies indistinguishable, parsimony collapses their count to one. We call this the **exact-once principle** and apply it at two layers:

| Layer | Anonymous entities | Exact-once consequence |
|:------|:------------------|:----------------------|
| Structure | Parallel morphisms between symmetric objects | One arrow per ordered pair (codiscrete category) |
| Encoding | Digit symbols in a homogeneous alphabet | One occurrence per symbol (alphabet-bijective word) |

The structural layer produces an exponent pair $(2,3)$ from categorical compositionality. The encoding layer converts this into a Diophantine fixed-point problem whose unique minimal solution is $p = 69$. Category theory supplies the **form**; number theory supplies the **content**.

**Stage 1 (§2)** is a theorem within stated principles and a motivated framework choice (finite categories).

**Stage 2 (§3)** conjectures that $\alpha^{-1}$ equals the stabilized inverse Todd defect comparing the $69$-point discrete mesh to its continuum envelope — a striking numerical identification within a framework that remains to be derived. Every choice is flagged; falsification criteria are given.

**Self-description.** Throughout, a *self-description* of a structure means a finite serialization of its native low-level invariants in a homogeneous alphabet such that the code is self-sizing (length equals alphabet size), self-validating (admits an internal consistency check), and free of anonymous redundancy. This doctrine privileges nativeity over compressibility: the code serializes what the structure canonically exposes, not what an external classifier might abbreviate.

---

## 2. Stage 1: Deriving $p = 69$

### 2.1 Principles

**Principle 1 (Naturality).** All constructions on a finite set $S$ are invariant under $\mathrm{Sym}(S)$. No anonymous element is distinguishable from any other.

**Principle 2 (Parsimony).** Anonymous multiplicity is redundancy. When symmetry or absence of internal structure renders $k$ copies of a datum indistinguishable, set $k = 1$. More generally: among constructions, formulations, and encodings compatible with the structural constraints, choose the one with least unexploited capacity.

*Remark.* These are not independent. Naturality identifies what is indistinguishable; Parsimony eliminates the resulting redundancy. Their conjunction is the exact-once principle: each structurally distinct role is filled exactly once.

### 2.2 Framework

A self-encoding requires: (i) finiteness — the code is a finite string; (ii) composition — there must be an internal operation to encode; (iii) multiple anonymous objects — a single-object structure (monoid) has no inter-object morphisms to witness. **Finite categories** are the minimal algebraic setting satisfying all three: a set of objects, morphism sets between pairs, and an associative unital composition. Monoids lack (iii); groups and groupoids add invertibility structure beyond what is required; operads add multi-arity. This is a motivated framework choice, not a derivation from the Principles alone.

### 2.3 The Codiscrete Category

We derive the codiscrete category in two steps: first determining where morphisms exist (support), then how many occupy each position (multiplicity).

**Theorem 1A (Support).** *Let $S$ be a finite set with $|S| = p \geq 2$. Let $G \subseteq S \times S$ be a binary relation satisfying:*

- *(Nat) $G$ is $\mathrm{Sym}(S)$-invariant,*
- *(N) $\exists\,(i,j) \in G$ with $i \neq j$,*
- *(C) $G$ admits a category structure: $\Delta \subseteq G$ (identities) and $G$ is closed under the induced composition.*

*Then $G = S \times S$.*

*Proof.* The diagonal action of $\mathrm{Sym}(S)$ on $S \times S$ has exactly two orbits: the diagonal $\Delta = \{(i,i)\}$ and the off-diagonal $\Delta^c = \{(i,j) : i \neq j\}$. Every $\mathrm{Sym}(S)$-invariant subset is a union of orbits, giving four candidates: $\emptyset,\; \Delta,\; \Delta^c,\; S \times S$.

| Candidate | Nat | N | C |
|:----------|:---:|:-:|:-:|
| $\emptyset$ | ✓ | ✗ | ✗ |
| $\Delta$ | ✓ | ✗ | ✓ |
| $\Delta^c$ | ✓ | ✓ | ✗ |
| $S \times S$ | ✓ | ✓ | ✓ |

$\Delta^c$ fails (C): for distinct $a, b \in S$ with $p \geq 2$, the pair $(a,b)$ composed with $(b,a)$ requires $(a,a) \in G$, but $(a,a) \notin \Delta^c$. $\square$

*Remark.* The proof is a two-orbit collapse: one nontrivial activation plus compositional closure forces total activation. This is the structural heartbeat of the derivation.

**Theorem 1B (Multiplicity).** *Among all finite category structures on object set $S$ with morphism support $S \times S$, the Parsimony-minimal one has exactly one morphism per ordered pair: the codiscrete category $C_p$.*

*Proof.* By Naturality, $|\mathrm{Hom}(i,j)|$ depends only on whether $i = j$: write $|\mathrm{Hom}(i,i)| = a$ and $|\mathrm{Hom}(i,j)| = b$ for $i \neq j$, with $a, b \geq 1$ (since support is total). Within a hom-set $\mathrm{Hom}(i,j)$, the framework provides no primitive internal labels — morphisms carry only source, target, and their behavior under composition. With no internal structure to distinguish parallel arrows in the same hom-set, multiplicity beyond one is anonymous redundancy. Parsimony sets $b = 1$. For endomorphisms: the identity $\mathrm{id}_i$ is structurally distinguished, but any further endomorphism is anonymous. Parsimony sets $a = 1$.

With $|\mathrm{Hom}(i,j)| = 1$ for all $i,j$, composition is uniquely determined: the composite of the unique arrow $i \to j$ with the unique arrow $j \to k$ is the unique arrow $i \to k$. Associativity is automatic. This is the codiscrete category $C_p$. $\square$

*Remark.* Theorem 1A is a theorem of combinatorics. Theorem 1B applies Parsimony to a framework in which morphisms carry no primitive internal labels beyond source, target, and identity status. Together they give $C_p$ as the unique exact-once natural category: one morphism per ordered pair, no more, no less.

### 2.4 The Nerve and Its Cardinal Profile

The nerve $N(C_p)$ is the simplicial set with

$$|N_k| = p^{k+1}.$$

By the Segal condition, all levels $k \geq 3$ are determined by levels $0, 1, 2$. These three independent levels have distinct categorical content:

| Level | Content | Count | Role |
|:------|:--------|:------|:-----|
| 0 | Objects | $p$ | Identities |
| 1 | Morphisms | $p^2$ | Arrows (one-step interactions) |
| 2 | Composable pairs | $p^3$ | Composition witnessed (two-step processes) |

The clean power-law profile $p^{k+1}$ is itself a consequence of exact-once multiplicity: with one arrow per ordered pair, $k$-chains through $C_p$ biject with $(k+1)$-tuples of objects.

### 2.5 The First Compositional Pair

**Theorem 2.** *The first self-validating compositional truncation of the nerve is $(|N_1|, |N_2|) = (p^2, p^3)$.*

This rests on three properties, all required:

*(i) Compositional visibility.* Composition is the operation distinguishing a category from a directed graph. It first appears at level 2: $N_2$ records composable pairs and their composites. Any truncation omitting level 2 certifies the underlying graph, not the category. Therefore the truncation must include level 2.

*(ii) Nativeity and parsimony.* In the arrows-only formulation of category theory (Freyd), the primitive sort is morphisms; objects arise as identity morphisms: $\mathrm{Ob}(C) = \{e \in \mathrm{Mor}(C) : e \circ f = f \text{ whenever defined}\}$. The object count $p = p^3/p^2$ is arithmetically recoverable from levels 1 and 2. Parsimony among equivalent formulations selects arrows-only (one primitive sort rather than two), and parsimony within the certificate removes data derivable from included levels. Therefore level 0 is omitted.

*(iii) Self-validation.* The pair $(p^2, p^3)$ satisfies $(p^2)^3 = (p^3)^2$, an algebraic consistency check certifying that both entries arise from a common root. This cross-verification is what makes the pair a certificate rather than raw data: the code carries its own verifier. A single number $p^2$ alone lacks this internal check.

*Conclusion.* The pair $(|N_1|, |N_2|) = (p^2, p^3)$ is the shortest truncation of the nerve that (a) witnesses composition, (b) uses only the primitive sort, and (c) self-validates. The exponents $(2, 3)$ are not chosen but forced: they are the degrees of the first adjacent nerve levels at which exact-once compositionality is visible. $\square$

### 2.6 Alphabet-Bijective Serialization

The certificate $(p^2, p^3)$ must be serialized as a finite string. We fix the encoding in three steps.

**Step 1: Numeral system.** Base-$b$ positional notation is the canonical bridge between non-negative integers and finite strings over a uniform alphabet $\Sigma_b = \{0, \ldots, b{-}1\}$. Among numeral systems, it is the unique one satisfying completeness (every non-negative integer representable), homogeneity (all positions use the same symbol set), and shift-invariance (prepending zero preserves value; left-shifting multiplies by a fixed radix). See Appendix A.

**Step 2: Serialization format.** The certificate is serialized by concatenation without delimiters:

$$w = d_b(p^2) \,\|\, d_b(p^3),$$

where $d_b(n)$ is the standard base-$b$ representation without leading zeros. Concatenation is the free monoidal product on strings — the simplest sequential combination respecting order. The algebraic relation $(p^2)^3 = (p^3)^2$ enables recovery of the split point: one searches factorizations of $w$ for the unique split satisfying this identity. The code carries its own delimiter.

**Step 3: Symbol homogeneity and self-sizing.** The digit alphabet $\Sigma_b$ consists of homogeneous primitive tokens: each can appear in any position, and no token is structurally privileged over any other. By the exact-once principle applied to the encoding layer:

- **Equal multiplicity.** Absent any structural reason to prefer one digit over another, each digit should appear with equal frequency — the only anonymous-neutral distribution. This mirrors the structural layer, where Naturality forces equal hom-set sizes across equivalent pairs.
- **Minimal multiplicity.** Parsimony sets the common count to $1$: the minimum positive value.

Therefore each digit in $\Sigma_b$ appears exactly once in $w$, giving $|w| = b$. This is the **self-sizing fixed point**: the string's length equals its alphabet size. Equivalently, $w$ is a permutation of $\Sigma_b$.

*Remark.* The exact-once principle operates identically at both layers:

| Layer | Entities | Exact-once statement |
|:------|:---------|:--------------------|
| Structure | Arrows per ordered pair | $|\mathrm{Hom}(i,j)| = 1$ |
| Encoding | Occurrences per digit symbol | each digit appears once |

### 2.7 The Unique Solution

**Theorem 3 (Computational).** *The system*
$$L_b(p^2) + L_b(p^3) = b, \quad d_b(p^2) \,\|\, d_b(p^3) \text{ is a permutation of } \{0, \ldots, b{-}1\}$$
*has no solution for $2 \leq b \leq 9$. It has exactly one solution for $b = 10$:*

$$\boxed{p = 69, \quad b = 10, \quad w = 4761328509.}$$

*No further solutions exist for $11 \leq b \leq 36$.*

*Verification.* $69^2 = 4761$ (4 digits), $69^3 = 328509$ (6 digits). Concatenation: $4761328509$ — ten digits, each of $\{0,1,2,3,4,5,6,7,8,9\}$ appearing exactly once. Self-validation: $4761^3 = 328509^2 = 69^6 = 10\,790\,272\,531\,441$. ✓

**Corollary (Base Minimality).** *Under Parsimony applied to base selection — prefer the smallest base admitting an alphabet-bijective serialization — the unique solution is $p = 69$ at $b = 10$. Solutions at higher bases, if any exist, are suboptimal.*

*Proof.* Exhaustive search verifies no solutions at $b \leq 9$ and exactly one at $b = 10$. The Corollary follows. $\square$

*Remark on scope.* The expected number of solutions at base $b$ is heuristically
$$E(b) \sim \frac{b!}{b^b} \cdot \frac{b}{5\ln b} < 1 \quad \text{for } b < e^5 \approx 148,$$
since $b!/b^b \sim \sqrt{2\pi b}\,e^{-b}$ is the probability that a random length-$b$ string over $b$ symbols is a permutation, and $b/(5\ln b)$ estimates the number of candidate $p$ values with correct total digit count. This heuristic suggests no solutions exist for $11 \leq b \leq 148$, consistent with the verified range. The Corollary does not depend on this estimate.

*Remark on commensurability.* The exponents $2$ and $3$ sum to $5$. The digit-length ratio $L(p^2) : L(p^3) \approx 2 : 3$ becomes an exact integer partition only when $5 \mid b$. Base 10 is the first such base with sufficient room; base 5 is too small (the candidate range is empty). This arithmetic commensurability between the categorical exponents and the radix explains why decimal is favored without being presupposed.

### 2.8 Summary of the Logical Chain

| Step | Principle applied | Result |
|:-----|:-----------------|:-------|
| Two-orbit decomposition | Naturality on $S \times S$ | Four invariant relations |
| Compositional closure | Category axioms + Nontriviality | Support $= S \times S$ |
| Multiplicity collapse | Parsimony (no anonymous parallel arrows) | $\lvert\mathrm{Hom}\rvert = 1$: codiscrete $C_p$ |
| Nerve power law | (consequence of exact-once) | $\lvert N_k\rvert = p^{k+1}$ |
| First compositional window | Compositional visibility + arrows-only parsimony | Certificate $(p^2, p^3)$, exponents $(2,3)$ |
| Equal symbol usage | Naturality on digit alphabet | Equal digit multiplicity |
| Minimal multiplicity | Parsimony | Each digit once: $\lvert w\rvert = b$ |
| Smallest feasible base | Parsimony on base | $b = 10$ |
| Arithmetic | Exhaustive computation | $p = 69$ |

The integer 69 is the **least root of the first alphabet-bijective compositional power certificate**.

### 2.9 Alternative Certificates

The exponent pair $(2,3)$ arises from nerve levels $(N_1, N_2)$. Other choices and their outcomes:

| Nerve levels | Exponents | Compositional? | Self-validating? | Min-base solution |
|:-------------|:----------|:--------------:|:----------------:|:-----------------|
| $(N_0, N_1)$ | $(1, 2)$ | No | Yes | $p = 20,\; b = 6$ |
| $(N_1, N_2)$ | $(2, 3)$ | **Yes** | **Yes** | $p = 69,\; b = 10$ |
| $(N_2, N_3)$ | $(3, 4)$ | Yes | Yes | $p = 18,\; b = 10$ |
| $(N_0, N_1, N_2)$ | $(1,2,3)$ | Yes | Overdetermined | None $(b \leq 36)$ |

Only $(2,3)$ is the first adjacent pair witnessing composition. Earlier pairs see the graph but not the category; later pairs are non-minimal; the triple overdetermines and admits no solution.

---

## 3. Stage 2: From $p = 69$ to $\alpha$ (Conjectural)

### 3.1 Motivation

Stage 1 produced a canonical finite cardinal $p = 69$ from a self-description problem. The cardinal was extracted via a one-dimensional serialization — an ordered string of symbols. The natural continuum partner of such a serialization is the unit interval $[0,1)$, and the universal comparison between discrete summation and continuous integration on a uniform mesh is the Euler–Maclaurin formula, governed by the Todd function $\mathrm{Td}(x) = x/(1 - e^{-x})$.

The fine-structure constant $\alpha$, governing the coupling between discrete charges and a continuous gauge field, is the paradigmatic dimensionless constant of the discrete–continuum interface in physics. If any fundamental constant were to emerge from a pristine discrete–continuum comparison, $\alpha$ is a natural comparand.

**Conjecture.** *The inverse fine-structure constant is the stabilized inverse Todd defect of the canonical $p$-mesh, with $p = 69$.*

**Open Problem.** Derive the stabilization procedure (§3.4) from a single invariant or canonical transform of the pair (simplicial nerve of $C_{69}$, unit interval with exponential probe).

### 3.2 Setup

**Mesh.** The cardinal $p$ is reified as $p$ equally spaced sample points $\{0, h, 2h, \ldots, (p{-}1)h\}$ on $[0,1)$, with spacing $h = 1/p$. Uniformity follows from object anonymity: no point is distinguished. The half-open interval supports periodic completion to a cyclic $p$-lattice with first Fourier frequency $2\pi/p$.

**Probe.** $f(x) = e^{-x}$: the unique positive, monotone-decaying eigenfunction of translation on $[0,1]$ with unit decay rate and $f(0) = 1$. Under this probe, the ratio of discrete sum to continuous integral is exactly the Todd transfer:

$$\frac{h \displaystyle\sum_{k=0}^{p-1} f(kh)}{\displaystyle\int_0^1 f(x)\,dx} = \mathrm{Td}(h).$$

The integral evaluates to $1 - e^{-1}$, giving a useful exact identity: $1/\mathrm{Td}(1) = 1 - e^{-1}$.

### 3.3 Three Simplicial Levels, Three Scales

The nerve of $C_p$ has three independent simplicial levels. Each activates a canonical scale of the mesh:

| Level | Categorical content | Scale | Origin |
|:------|:-------------------|:------|:-------|
| 1 (morphisms) | One-step interactions | $h = 1/p$ | Mesh spacing |
| 0 (objects) | Global support | $1$ | Domain extent |
| 2 (compositions) | Two-step coherence | $2\pi/p$ | First Fourier mode of cyclic $p$-lattice |

*On the reappearance of level 0.* In Stage 1, level 0 was omitted from the certificate because objects are derivable in the arrows-only formulation — an economy internal to categorical self-certification. In Stage 2, embedding the discrete structure into a continuum activates the domain extent, an *external* geometric feature with no purely internal analog. The change of context (internal certification → external comparison) licenses the reappearance of the object-level datum.

### 3.4 The Formula

**Level 1 (morphisms → mesh scale $h = 1/p$):**

$$T_1 = \frac{1}{\mathrm{Td}(h) - 1} = \frac{A_{\mathrm{cont}}}{A_{\mathrm{disc}} - A_{\mathrm{cont}}}$$

where $A_{\mathrm{disc}} = h\sum f(kh)$ and $A_{\mathrm{cont}} = \int_0^1 f(x)\,dx$. This is the **inverse defect**: how many copies of the discretization error fit into the continuum integral. Its asymptotic expansion is

$$T_1 = 2p - \tfrac{1}{3} + \tfrac{1}{18p} - \tfrac{1}{270p^2} + \cdots$$

**Level 0 (objects → domain scale $1$):**

$$T_0 = -\frac{1}{\mathrm{Td}(1)} = -(1 - e^{-1}).$$

This subtracts the continuum integral itself — the Todd transfer evaluated at the domain scale. It is not a free parameter: it is $\mathrm{Td}$ at the unique remaining independent scale, and the exact identity $1/\mathrm{Td}(1) = 1 - e^{-1}$ gives its value.

**Level 2 (compositions → Fourier dual scale $2\pi i/p$):**

The Todd function at imaginary argument decomposes into amplitude and phase:

$$\mathrm{Td}(ix) = \frac{x}{2}\cot\frac{x}{2} + i\frac{x}{2}.$$

At $x = 2\pi/p$: the imaginary part $\mathrm{Im}[\mathrm{Td}(2\pi i/p)] = \pi/p$ is exact; the real part $\mathrm{Re}[\mathrm{Td}(2\pi i/p)] = (\pi/p)\cot(\pi/p)$ generates a convergent series in $1/p^2$.

The dual correction series, normalized by $1/p$ (one factor per lattice site), is:

$$\mathcal{D}(p) = \frac{\mathrm{Im}[\mathrm{Td}(2\pi i/p)] + \mathrm{Re}[\mathrm{Td}(2\pi i/p)] - 1}{p} = \frac{\pi}{p^2} - \frac{\pi^2}{3p^3} - \frac{2\pi^4}{45p^5} - \cdots$$

The leading term $\pi/p^2$ is the phase contribution (exact); subsequent terms are amplitude corrections from the cotangent expansion.

**Assembly:**

$$\alpha^{-1} = T_1 + T_0 + \mathcal{D}(p), \qquad p = 69.$$

**Evaluation at $p = 69$:**

| Term | Expression | Value |
|:-----|:-----------|------:|
| $T_1$ | $1/(\mathrm{Td}(1/69) - 1)$ | $+137.667\,47$ |
| $T_0$ | $-(1 - e^{-1})$ | $-0.632\,12$ |
| $\mathcal{D}_1$ | $\pi/69^2$ | $+0.000\,660$ |
| $\mathcal{D}_2$ | $-\pi^2/(3 \cdot 69^3)$ | $-0.000\,010$ |
| **3-term** | $T_1 + T_0 + \mathcal{D}_1$ | $\mathbf{137.036\,01}$ |
| **4-term** | $+\mathcal{D}_2$ | $\mathbf{137.036\,00}$ |
| **CODATA 2022** | | $137.035\,999\,177(21)$ |

The three-term truncation matches experiment to $0.007$ ppm. The exact sum of the convergent dual series gives $\mathcal{D}(69) = 0.000\,650$, and the complete formula yields $137.036\,00$, differing from CODATA by approximately $1 \times 10^{-6}$.

*Reciprocal consistency.* The leading approximation $\alpha^{-1} \approx 2p - 4/3 + e^{-1}$ inverts to $p \approx \frac{1}{2}(\alpha^{-1} + 4/3 - e^{-1}) = 69.0005$: the physical value pins $p$ to within $0.001$ of the integer derived independently in Stage 1.

### 3.5 Interpretation

The formula reads:

$$\alpha^{-1} = \underbrace{\frac{1}{\mathrm{Td}(h) - 1}}_{\substack{\text{inverse local defect} \\ \text{(morphism scale)}}} \;-\; \underbrace{\frac{1}{\mathrm{Td}(1)}}_{\substack{\text{continuum baseline} \\ \text{(object scale)}}} \;+\; \underbrace{\mathcal{D}(p)}_{\substack{\text{spectral refinement} \\ \text{(composition scale)}}}$$

The inverse fine-structure constant counts how many discretization errors fit into the continuum, stabilized by subtracting the domain baseline and refined by spectral corrections from the first Fourier mode of the finite lattice.

The magnitude hierarchy mirrors the simplicial hierarchy:

- **Morphisms** (one-step interactions) dominate at $O(p) \approx 137.7$.
- **Objects** (global support) normalize at $O(1) \approx 0.63$.
- **Compositions** (two-step coherence) refine at $O(p^{-2}) \approx 0.0007$.

The three independent categorical levels each contribute exactly once to the formula, at geometrically decreasing magnitudes. This is the exact-once principle's final echo: one term per simplicial level, one scale per term.

---

## 4. Assessment

### 4.1 What Is Proved

Stage 1 is a mathematical theorem, conditional on the framework choice of finite categories:

1. The unique natural nontrivial morphism support is total: $G = S \times S$ (Theorem 1A — combinatorics).
2. Parsimony-minimal multiplicity gives the codiscrete category $C_p$ (Theorem 1B — exact-once principle).
3. The first self-validating compositional nerve truncation is $(p^2, p^3)$ (Theorem 2 — categorical + arrows-only formulation).
4. The unique alphabet-bijective serialization at minimal base is $p = 69$, $b = 10$ (Theorem 3 + Corollary — computation + parsimony).

The exact-once principle operates identically at both layers: one morphism per ordered pair, one digit per symbol.

### 4.2 What Is Conjectured

Stage 2 conjectures $\alpha^{-1}$ equals the stabilized inverse Todd defect at $p = 69$. Three components require derivation from first principles:

1. **The continuum partner.** The unit interval as the geometry of one-dimensional serialization.
2. **The level-to-scale map.** Morphisms → $1/p$, objects → $1$, compositions → $2\pi/p$.
3. **The assembly rule.** Inverse defect, baseline subtraction, spectrally normalized dual correction.

A resolution of the Open Problem must produce all three from a single invariant or canonical transform of the pair (nerve of $C_p$, unit interval), or must demonstrate that no such invariant exists (falsifying the conjecture).

### 4.3 What Is Conditional

Even Stage 1 rests on choices that are motivated but not unique:

- **Finite categories** as the framework for compositional self-description. Alternatives (semicategories, enriched categories, operads) would alter or eliminate the result.
- **Arrows-only formulation,** which drops level 0 from the certificate. The objects-and-arrows formulation would include level 0, yielding exponents $(1, 2, 3)$ and no pandigital solution.
- **Radix concatenation** as the serialization format. Alternative encodings (e.g., prime factorization, mixed radix) would change the Diophantine problem.

Each choice is defended on parsimony grounds within §2, but the proof is conditional on these choices jointly. The reader should weigh whether the motivations constitute sufficient inevitability.

### 4.4 Falsification

**Stage 1** is falsified by:
1. A computational error in the exhaustive search (verifiable by independent implementation).
2. A logical error in Theorems 1A, 1B, or 2.
3. A demonstration that an alternative framework choice, equally or more parsimonious, yields a different $p$.

**Stage 2** is falsified by:
4. Future measurement of $\alpha^{-1}$ outside $137.036\,0 \pm 0.000\,2$ (3-term) or $137.036\,00 \pm 0.000\,05$ (exact dual series).
5. A proof that no single invariant of the pair (nerve, interval) produces the formula.
6. Discovery of a comparably precise zero-parameter formula for $\alpha^{-1}$ from a different integer, undermining the uniqueness of the $p = 69$ identification.

### 4.5 Prior Work

Eddington (1929) proposed $\alpha^{-1} = 136$ from representation-theoretic counting of algebraic elements, later revised to $137$. Wyler (1969) obtained $\alpha^{-1} \approx 137.036$ from ratios of volumes of bounded symmetric domains. The present construction differs in that Stage 1 makes no reference to physics or to $\alpha$, the formula has zero adjustable parameters, every framework choice is explicit, and falsification criteria are stated. Whether these features elevate the construction above sophisticated numerology depends entirely on the resolution of the Open Problem.

---

## Appendix A: Positional Notation

**Theorem (Characterization).** *Among functions mapping non-negative integers to finite strings over a finite alphabet, base-$b$ positional notation is the unique system satisfying:*

- *(Completeness) Every non-negative integer has a representation.*
- *(Homogeneity) Every position draws from the same symbol set.*
- *(Shift-invariance) Prepending a $0$ preserves the value; shifting all digits one position left multiplies the value by a fixed constant $r$.*

*Proof.* Shift-invariance with constant multiplier $r$ forces place values $1, r, r^2, \ldots$ Homogeneity forces a common digit set $D$ at every position. Completeness requires that every residue modulo $r$ be representable by a single digit, forcing $D \supseteq \{0, 1, \ldots, r-1\}$. Minimality of the digit set (no redundant representations) gives $D = \{0, \ldots, r-1\}$. Setting $b = r$ recovers standard base-$b$ notation.

*Remark.* This excludes balanced ternary (digits $\{-1,0,1\}$ violate non-negativity of the symbol set), factorial numeration (variable radix violates fixed $r$), and bijective numeration ($\{1,\ldots,b\}$ without $0$ violates the prepend-zero condition). $\square$

---

## Appendix B: Numerical Verification

| Quantity | Expression | Value |
|:---------|:-----------|------:|
| $p$ | | $69$ |
| $b$ | | $10$ |
| $h$ | $1/p$ | $0.014\,4928$ |
| $p^2$ | | $4761$ |
| $p^3$ | | $328\,509$ |
| $p^6$ | $(p^2)^3 = (p^3)^2$ | $10\,790\,272\,531\,441$ |
| $w$ | $d_{10}(4761) \,\|\, d_{10}(328509)$ | $4761328509$ |
| Digit check | | $\{0,1,2,3,4,5,6,7,8,9\}$ ✓ |
| $\mathrm{Td}(h)$ | $h/(1-e^{-h})$ | $1.007\,264$ |
| $\mathrm{Td}(h) - 1$ | | $0.007\,264$ |
| $T_1$ | $1/(\mathrm{Td}(h)-1)$ | $137.667\,47$ |
| $\mathrm{Td}(1)$ | $1/(1-e^{-1})$ | $1.581\,977$ |
| $T_0$ | $-1/\mathrm{Td}(1)$ | $-0.632\,121$ |
| $\mathrm{Im}[\mathrm{Td}(2\pi i/69)]$ | $\pi/69$ | $0.045\,534$ |
| $\mathrm{Re}[\mathrm{Td}(2\pi i/69)]$ | $(\pi/69)\cot(\pi/69)$ | $0.999\,306$ |
| $\mathcal{D}(69)$ exact | $(\pi/69 + (\pi/69)\cot(\pi/69) - 1)/69$ | $0.000\,650$ |
| $\mathcal{D}_1$ | $\pi/69^2$ | $0.000\,660$ |
| $\mathcal{D}_2$ | $-\pi^2/(3 \cdot 69^3)$ | $-0.000\,010$ |
| $T_1 + T_0$ | | $137.035\,35$ |
| 3-term $\alpha^{-1}$ | $T_1 + T_0 + \mathcal{D}_1$ | $137.036\,01$ |
| Exact $\alpha^{-1}$ | $T_1 + T_0 + \mathcal{D}(69)$ | $137.036\,00$ |
| CODATA 2022 | | $137.035\,999\,177(21)$ |
| Discrepancy | | $\approx 0.007$ ppm |
