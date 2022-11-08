---
title: 'Symmetries of the Standard Model IV: Discrete Symmetries'

# Summary for listings and search engines
summary: The discrete symmetries $C$, $P$, and $T$, and their relation to the three-generation structure of the theory.

# Link this post with a project
projects: []

# Date published
date: "2021-09-28T00:00:00Z"

# Date updated
lastmod: "2021-09-28T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.

authors:
- admin

tags:

categories:
- Quantum Field Theory
---

## Introduction

There are three discrete 'spacetime' symmetries of importance in any quantum field theory. These are **charge conjugation** $C$, **parity** $P$, and **time-reversal** $T$. The CPT theorem states that any Lorentz-invariant local quantum field theory will be invariant under the product operation $CPT$. We will hence consider $CP$ and $T$ to be equivalent symmetry operations. None of these symmetries is anomalous nor spontaneously broken in the Standard Model. We will hence discuss in turn the sectors of the theory in which they are respected or violated.

## The Kinetic Terms

Without coupling the fermions to the $SU(2)_L \times U(1)_Y$ gauge fields, we find that the kinetic terms for the gauge fields, the fermions, and the Higgs (that is, all terms except the Yukawa terms) are invariant under all three discrete symmetries. However, since the left- and right-handed fermions couple differently under $SU(2)_L \times U(1)_Y$, these coupling terms violate both $C$ and $P$. They nevertheless preserve the combined symmetry $CP$.

Since $CP$ is the only discrete symmetry respected by the kinetic terms, we will focus on this symmetry alone in the next two sections.

## The Yukawa Terms --- Quarks

We established in Part III that the Yukawa matrices $Y_u, Y_d$ could be taken without loss of generality to be Hermitian and positive semi-definite, and were uniquely determined by this requirement. We will assume this convention henceforth.

The action of $CP$ on the Yukawa terms is a symmetry if $Y_u$ and $Y_d$ are real matrices. Generically they will not be. However, in unitarity gauge we can independently rotate (vectorially) the up-type and down-type quarks to diagonalise the Yukawa matrices: take
$u_{L,R} \to U_u u_{L,R}$ and $d_{L,R} \to U_d d_{L,R}$ so that
$$ U_u^\dagger Y_u U_u = D_u \quad \mathrm{and} \quad U_d^\dagger Y_d U_d = D_d  \ . $$
The eigenvalues of these matrices are the (real and non-negative) masses of the quarks. After such a rotation, the Yukawa terms become real and hence $CP$-symmetric, and additionally enjoy a $U(1)^6$ flavour symmetry (at the least).

This field redefinition disturbs only one other term in the Lagrangian, which is the coupling of the weak charged current to the charged $W^\pm$ bosons. In particular:
$$ \bar{u}_L \gamma^\mu d_L \to \bar{u}_L U _u^\dagger U_d \gamma^\mu d_L  \ . $$
The matrix $V = U_u^\dagger U_d$ is known as the CKM matrix. A general unitary matrix has $n_g^2$ real parameters, of which $n_g(n_g+1)/2$ are complex phases. We can use the aforementioned freedom to rephase our quarks without disturbing the Yukawa terms to reduce the number of parameters in this matrix: $V \to U^\dagger V$ or $V \to V U$ where $U = \mathrm{diag}(e^{i \alpha}, e^{i \beta}, e^{i \gamma})$. Note that the $U(1)_B$ subgroup of $U(1)^6$ has trivial action on $V$. We can thus reduce the nine parameters in $V$ down to four (not three), of which one must be a complex phase, known as the CKM phase. All four parameterers are non-zero in the Standard Model. The CKM phase violates $CP$. The other three real parameters characterise the size of the mixing between quark flavours. Since these are all non-zero, there are no global flavour symmetries in the quark sector besides the flavour-blind $U(1)_B$, as we alluded to in Part III.

We note that if $g = 0$, there is no CP violation, even if our Lagrangian originally had complex Yukawa matrices (this illustrates that whilst no discrete symmetries may be initially apparent, an appropriate field redefinition can reveal one). As such, though we began this section considering the symmetries of the Yukawa terms, we say that CP violation from the CKM phase is a *weak interaction effect*.

> *Exercise:* show that with $n_g$ generations, the CKM matrix contains $(n_g-1)(n_g-2)/2$ complex phases. Conclude that three generations is the minimum required for weak CP violation.

## The Yukawa Terms --- Leptons

The above analysis applies identically to the lepton sector. The phase in the mixing matrix is known as the PMNS phase in this case, rather than the CKM phase.

We note that if we take $Y\_\nu = 0$, so that the neutrinos are massless, then we can diagonalise the Yukawa matrices without disturbing the weak charged current (simply choose $U_\nu = U_e$). In this case $CP$ will be exact, and in addition there will be an exact $U(1)^3$ flavour symmetry, corresponding to conservation of lepton number in each generation. For a time it was thought that the neutrinos were exactly massless, and that these were indeed exact symmetries. It is now known this is not the case.

More generally, we see that we can arrange for $V = I$ so long as the Yukawa matrices can be simultaneously diagonalised. For Hermitian matrices (and diagonalisable matrices more generally) this is equivalent to $[Y_e, Y\_\nu] = 0$. Thus if the Yukawa matrices commute, both $CP$ and individual lepton number will be symmetries of the theory.

However, $CP$ alone will be a symmetry under weaker requirements. Any degeneracy of eigenvalue in one of the two Yukawa matrices bestows the Yukawa terms with an additional $SU(2)$ symmetry (alongside $U(1)^6$). This is sufficient to remove the single complex phase for $n_g = 3$. Thus, with three generations, there will be no weak CP violation if there is a single pair of degenerate charged leptons *or* neutrinos (and a single pair of degenerate up-type quarks *or* down-type quarks). For $n_g = 3$, a degenerate eigenvalue implies $\det[Y_e, Y_\nu] = 0$. Thus we can claim that $\theta\_{PMNS}$ is physical if $\det[Y_e, Y_\nu] \neq 0$ (and likewise for the quark sector).

The phases $\theta\_{CKM}$ and $\theta\_{PMNS}$ are the two sources of **weak CP violation** in the Standard Model.

## The Theta Terms

There is an additional class of term one can add to the Standard Model Lagrangian that we mentioned in Part I but have ignored since then. These are the theta terms:

$$ \mathcal{L}\_\theta =  \frac{\theta g^2}{64 \pi^2} \epsilon^{\mu \nu \rho \sigma} F^a_{\mu \nu} F^a_{\rho \sigma} \ . $$

These are precisely the terms that appear on the right-hand sides of anomalous current conservation equations, as we have seen in Parts II and III. They violate both $P$ and $T$ (and so $CP$), but not $C$. In general such terms can be removed by a field redefinition corresponding to an anomalous symmetry. However, since we have made various such transformations in order to simplify the Yukawa terms, any attempts to remove the theta terms thus will appear to reintroduce symmetry-violating phases into other parts of the Lagrangian.

Indeed, having exhausted chiral rotations of the right-handed fermions to make the Yukawa matrices Hermitian, and having exhausted vectorial rotations of the fermions to diagonalise the Yukawa matrices and subsequently simplify the CKM and PMNS matrices, the only transformations which remain for us to exploit are those which are genuine symmetries of the Lagrangian. However, to introduce or remove any theta term, such a symmetry must be anomalous. There is only one such symmetry, $B + L$, and hence in general only one theta term can be removed. Since the divergence of the corresponding current contains only $SU(2)_L$ and $U(1)_Y$ gauge fields, the QCD theta term cannot be removed.

> *Exercise:* Show that if one of the quarks is massless, then $U(1)_R$ (for that quark flavour) is a symmetry of the Lagrangian. Argue that in this case, we can remove the QCD theta term. We can thus claim that $\theta\_{QCD}$ is physical if $\det(Y_u Y_d) \neq 0$.

It transpires, however, that the $U(1)_Y$ theta term is always unphysical. It can be seen that the theta terms are in fact total derivatives, and so their effects are non-perturbative. Whether they have any effect at all depends on whether there exist field configurations (that are pure gauge at infinity) such that this surface term is non-zero --- such configurations are known as **instantons**. In four spacetime dimensions instantons exist only if the third homotopy group of the gauge group is non-trivial. Since $\pi_3(U(1)) = \\{0\\}$ and $\pi_3(SU(n)) = \mathbb{Z}$ for $n \geq 2$, there exist only $SU(3)_C$ and $SU(2)_L$ instantons.

The absence of $U(1)_Y$ instantons compels us to perform a $U(1)\_{B+L}$ field redefinition that removes the $SU(2)_L$ theta term, leaving the QCD theta term as the only one with physical consequences. The phase $\theta\_{QCD}$ is the sole source of **strong CP violation** in the Standard Model (we reiterate that it also violates $P$). No effects of this term have yet been discovered, however.

## Summary

Since neither $C$, $P$, nor $T$ is anomalous nor spontaneously broken by the vacuum, we here classify these symmetries according to whether they are respected in the following three cases:

1. QCD: we set $g = g' = 0$.
2. Electroweak: we set $g_s = 0$.
3. QED: we set $g_s = 0$ and ignore the Higgs and massive gauge bosons.

| | QCD | Electroweak | QED |
| ---------- | ---------- | ---------- | ---------- |
|$C$| Yes | No | Yes |
|$P$| If $\theta_{QCD} = 0$ | No | Yes |
|$T$ or $CP$ | If $\theta_{QCD} = 0$  | If $\theta_{CKM} = \theta_{PMNS} = 0$ | Yes |
