---
title: 'Symmetries of the Standard Model III: The Higgs Sector'

# Summary for listings and search engines
summary: Global symmetries of the high-energy theory, including the Higgs field, the electroweak gauge bosons, and the Yukawa terms.

# Link this post with a project
projects: []

# Date published
date: "2021-09-27T00:00:00Z"

# Date updated
lastmod: "2021-09-27T00:00:00Z"

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

In this part of the series we will discuss the global symmetries of the full Standard Model Lagrangian. We will first consider the terms involving just the Higgs, then those coupling the Higgs to the fermions, and then those coupling the Higgs to the gauge bosons. Lastly, we will consider symmetries acting only on the fermion fields.

## The Higgs Potential

The Higgs Lagrangian

$$ \mathcal{L}\_\phi = |D_\mu \phi|^2 + \mu^2 \phi^\dagger \phi - \lambda( \phi^\dagger \phi)^2  $$

is by construction invariant under the gauge symmetry $SU(2)_L \times U(1)_Y$, where we take $Y = 1/2$ by convention and let $\phi$ transform in the fundamental of $SU(2)_L$. However, the Higgs potential is in fact invariant under a larger symmetry group. This is easiest to see by writing $\phi$ in terms of its real and imaginary parts:

$$ \phi = \begin{pmatrix} \phi_2 + i \phi_1 \\\ \phi_0 - i \phi_3 \end{pmatrix}  \ ,$$
so that
$$ \phi^\dagger \phi = \sum_i \phi_i^2  \ .$$
Then there is an obvious $O(4)$ symmetry. Ignoring discrete quotients, we have $O(4) = SU(2) \times SU(2)$. To see this decomposition explicitly in the case of the Higgs field, we can construct the matrix
$$ \Phi = \begin{pmatrix} \phi_0 + i \phi_3 &  \phi_2 + i \phi_1 \\\ - \phi_2 + i \phi_1 & \phi_0 - i \phi_3 \end{pmatrix} = \phi_0 I + i \sum_i \phi_i \sigma_i \ . $$
Note that $\Phi = |\phi| U$ where $U \in SU(2)$. Then we have
$$ \phi^\dagger \phi = \frac{1}{2}\mathrm{tr}(\Phi^\dagger \Phi) \ ,$$
which is invariant under the transformation
$$ \Phi \to U_L \Phi U_R^\dagger \ ,$$
where $U_{L,R} \in SU(2)$  (one can check that if $U_{L,R}$ are allowed to lie in $U(2)$ instead, they do not generally preserve the form of $\Phi$ as a real multiple of a special unitary matrix). The reader can check that the left action on $\Phi$ corresponds precisely to the action of $SU(2)_L$ on the original field $\phi$.

When the Higgs acquires a vacuum expectation value, so that $\Phi \propto I$, this symmetry group is spontaneously broken down to the diagonal subgroup, with $U_L = U_R$. This symmetry is known as **custodial symmetry**, $SU(2)_V$.

## Exactness --- The Yukawa Terms

Consider first a single generation of quarks. The Yukawa terms are
$$ \mathcal{L}\_y = -y_d \bar{Q}_L \phi d_R - y_u \epsilon\^{ab}\bar{Q}\_{La} \phi^*_b u_R  +\mathrm{h.c.}  $$
By construction this Lagrangian is invariant under $SU(2)_L$, but does not appear to be invariant under $SU(2)_R$ (defined to act on doublets of right-handed fermions analogously to $SU(2)_L$). However, in the case that $y_u = y_d = y$, one can write

$$ \mathcal{L}\_y = -y \bar{Q}_L \Phi Q_R + \mathrm{h.c.} $$

which is evidently invariant under $SU(2)_R$. With multiple generations, the complex numbers $y_u,y_d$ become complex matrices, which we will denote $Y_u,Y_d$. As above, $SU(2)_R$ will be a symmetry if $Y_u = Y_d$. However, since we can freely rotate the right-handed down-type quarks amongst themselves without disturbing any other term in the Lagrangian (and likewise for the right-handed up-type quarks), this requirement is a little too strict. In fact, $SU(2)_R$ will be a symmetry provided $Y_u$ and $Y_d$ are related by right-multiplication by a unitary matrix. In the case of a single generation, this just requires that $|y_u| = |y_d|$. 

Note that any square matrix $Y$ can be written as the product $HU$ where $H$ is Hermitian and positive semi-definite and $U$ is unitary. This is known as polar decomposition, and defines $H$ uniquely. We can hence use the freedom to rotate the right-handed fermions to ensure, without loss of generality, that the Yukawa matrices are Hermitian and positive semi-definite. With this convention, $SU(2)_R$ is a symmetry if and only if $Y_u = Y_d$ and $Y_e = Y\_\nu$. This condition does not hold in reality, however.

Since $SU(2)_L$ is always a symmetry of the Yukawa terms, the very same condition is necessary and sufficient for custodial $SU(2)_V$ to be exact.

> *Exercise:* Show that the above condition can be expressed in a convention-independent manner as
$$ Y_u^\dagger Y_u = Y_d^\dagger Y_d \quad \mathrm{and} \quad  Y_e^\dagger Y_e = Y\_\nu^\dagger Y\_\nu \ .$$

## Exactness --- Kinetic Terms and Hypercharge

If $SU(2)_L \times SU(2)_R$ is truly the full symmetry group of the Higgs potential, and the first factor is the familiar gauged $SU(2)_L$ group, then hypercharge must be a subgroup of the second factor. Indeed, it is not too difficult to show that hypercharge acts on the Higgs $\Phi$ as the $T^3_R$ generator of $SU(2)_R$. However, hypercharge does not act on the quarks and leptons in this way. In fact, the generator of hypercharge can be written
$$ Y = T^3_R + B/2 - L/2 \ ,$$
where $B$ and $L$ are the generators of baryon number and lepton number respectively. Since only some subgroup of $SU(2)_R$ is gauged, and not the entirety of it, $SU(2)_R$ is not an exact symmetry of the theory (unless we set $g' = 0$). To see this explicitly from the Lagrangian, we can consider the Higgs kinetic terms.

Without gauge couplings, the kinetic terms of the Higgs are invariant under the full $SU(2)\_L \times SU(2)\_R$ symmetry group, just as the potential is. When we gauge the $SU(2)\_L$ subgroup, the additional terms in the Lagrangian (coupling the Higgs to the gauge fields) are only invariant as a result of the global transformation properties of the gauge fields:
$$ W_\mu \to U W_\mu U^{-1} \ .$$
Thus, the problematic terms are those that involve the hypercharge gauge field $B_\mu$ (proportional to the matrix $T_R^3$), which does not transform under the action of the generators $T_R^1$ and $T_R^2$, nor commute with them:
$$ \begin{align} \mathrm{tr}(B^\mu \Phi^\dagger \Phi  B_\mu) \to \ &\mathrm{tr}(B^\mu (1 - i\alpha_iT_R^i)  \Phi^\dagger \Phi (1 + i\alpha_j T_R^j) B_\mu) \\\\
 \neq \ &\mathrm{tr}(B^\mu \Phi^\dagger \Phi  B_\mu) \ . \end{align}$$

> *Exercise:* Show that the kinetic terms for the fermions also break $SU(2)_R$ explicitly when $g' \neq 0$.

To summarise: both the Yukawa terms and the coupling to the hypercharge gauge boson explicitly break the full $SU(2)_L \times SU(2)_R$ symmetry, but they leave intact both $SU(2)_L$ and the $T^3_R$ generator of $SU(2)_R$.

## Fermion Symmetries and Anomalies

Having considered the Higgs sector in some detail, we should ask whether there are any additional symmetries that act only on the fermions. If the Yukawa matrices are general (as they are in reality), the only possible symmetries are $U(1)$ rephasings of fermion flavours and chiralities. In fact, as we will justify more fully in Part IV, the only such symmetries are the vectorial and flavour-blind symmetries $U(1)_B$ and $U(1)_L$.

Though exact, both of these symmetries suffer an electroweak anomaly:
$$ \partial_\mu J_B^\mu = \partial_\mu J_L^\mu = \frac{n_g}{64 \pi^2} \epsilon\^{\mu \nu \rho \sigma}\left( g^2 W^a_{\mu \nu} W^a_{\rho \sigma} - {g'}^2 B_{\mu \nu} B_{\rho \sigma}  \right) \ .$$

Since the divergences of the baryon number current and lepton number current are identical, we see that the combination of global symmetries $B - L$ is non-anomalous, and indeed is the only such exact global continuous symmetry in the Standard Model.

## Summary

| | Approximate |SSB | Anomalous | 
| ---------- | ---------- | ---------- | ---------- |
| $SU(2)_L \times SU(2)_R$ |$T_R^1$ and $T_R^2$ | Down to $SU(2)_V$ | No | 
| $SU(2)_V$ | $T^1$ and $T^2$ | No | No | 
| $U(1)_{B+L}$| No | No | Electroweak | 
| $U(1)_{B-L}$| No | No | No |

[//]: <> (Note that $SU(2)_L$ here is gauged, as is the hypercharge subgroup of $SU(2)_R \times U(1)\_{B-L}$.)
