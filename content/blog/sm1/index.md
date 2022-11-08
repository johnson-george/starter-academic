---
title: 'Symmetries of the Standard Model I: Overview'

# Summary for listings and search engines
summary: The structure of the Standard Model.

# Link this post with a project
projects: []

# Date published
date: "2021-09-21T00:00:00Z"

# Date updated
lastmod: "2021-09-21T00:00:00Z"

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

The Standard Model is a complicated quantum field theory. Understanding it in detail takes time, but understanding the symmetries of the theory provides a framework with which to understand these details.

Symmetries can be classified along many lines. They can be continuous or discrete, global or local, approximate or exact, anomalous, spontaneously broken, and so on. In this series, we will endeavour to discuss each and every symmetry of the Standard Model, and classify them according to each of the categories above.

In Part I, we will give a schematic overview of the structure of the Standard Model and its gauge symmetries. In Parts II and III we will consider global continuous symmetries, first from the perspective of the low-energy theory, and then from the perspective of the high-energy theory. In Part IV we will consider the discrete symmetries $C$, $P$, and $T$, and in Part V we will collect these results together and discuss how they are affected by some extensions to the theory.

## Gauge Symmetries

The starting point for the construction of the Standard Model is the gauge group

$$ SU(3)_C \times SU(2)_L \times U(1)_Y \ , $$

where the first factor represents the colour symmetry of **quantum chromodynamics (QCD)**, and the second two factors (known as weak isospin and hypercharge) represent the symmetry of the **electroweak** interactions.

## The Field Content

The Standard Model contains gauge bosons corresponding to each of the gauge groups described above, along with $n_g = 3$ generations of Weyl fermions in the following representations, as well as a single scalar field, the Higgs:

| | $SU(3)_C$ | $SU(2)_L$ | $U(1)_Y$ |
| ---------- | ---------- | ---------- | ---------- |
| $Q_L$ | Fundamental | Fundamental | $Y = 1/6$ |
| $u_R$ | Fundamental | Trivial | $Y = 2/3$ |
| $d_R$ | Fundamental| Trivial | $Y = -1/3$ |
| $L_L$ | Trivial | Fundamental | $Y = -1/2$ |
| $e_R$ | Trivial| Trivial | $Y = -1$ |
| $\nu_R$ | Trivial | Trivial | $Y = 0$ |
| $\phi$ | Trivial | Fundamental | $Y = 1/2$ |

## The Lagrangian

The most general renormalizable Lagrangian with the above gauge symmetry and field content is the Standard Model. We can group the terms in the Lagrangian into four classes:

1. Kinetic terms for the gauge fields.
2. Kinetic terms for the fermions, including coupling to the gauge fields.
3. Kinetic terms for the Higgs and Higgs self-interactions.
4. Yukawa couplings between the fermions and the Higgs.

Schematically, this Lagrangian is:

$$ \begin{align} \mathcal{L} = &-\frac{1}{4} F^a_{\mu \nu} F^{a\mu \nu} \\\ &+ \bar{\psi} i  \gamma^\mu D_\mu \psi \\\ &+ |D_\mu \phi|^2 - V(\phi) \\\ &- Y_d \bar{Q}_L \phi d_R - Y_u \bar{Q}\_{L} \phi^c u_R + \mathrm{h.c.} \\\ &- Y_e \bar{L}_L \phi e_R - Y_\nu \bar{L}\_{L} \phi^c \nu_R + \mathrm{h.c.} \end{align} $$

There is an additional class of term one can add to the Lagrangian whose effects are more subtle. These are the theta terms, one for each factor of the gauge group:

$$ \mathcal{L}\_\theta =  \frac{\theta g^2}{64 \pi^2} \epsilon^{\mu \nu \rho \sigma} F^a_{\mu \nu} F^a_{\rho \sigma} \ . $$

We will ignore these terms until Part IV.

## Exact Symmetries

The Lagrangian above has many approximate global symmetries which we will discuss in due course. The extent to which these symmetries are approximate is dictated by the various parameters of the theory. For general choices of these parameters (and in reality) the Standard Model has only two exact global continuous symmetries. These are **baryon number** and **lepton number**. They are not enforced upon the theory --- rather, it is simply not possible to write down renormalizable terms respecting the overall gauge symmetry which violate baryon or lepton number. We sometimes say such symmetries are **accidental**.

## Spontaneous Symmetry Breaking

A symmetry is spontaneously broken if it is respected by the Lagrangian but not by the vacuum of the theory. Spontaneous symmetry breaking is typically caused by fields acquiring a non-zero expectation value in the vacuum. In the Standard Model, there are two sources of spontaneous symmetry breaking.

1) The Higgs field $\phi$ acquires a non-zero VEV. This breaks the gauge symmetry thus:
$$ SU(3)_C \times SU(2)_L \times U(1)_Y \to SU(3)_C \times U(1)_Q \ .$$
It also breaks some approximate global symmetries. This is known as **electroweak symmetry breaking**. The unbroken $U(1)_Q$ symmetry is the symmetry of **quantum electrodynamics (QED)**. We will discuss this further in Part III.

2) At a lower energy scale, the quark bilinears $\bar{q}q$ acquire a non-zero VEV (equal in magnitude for each flavour). This breaks no further gauge symmetries, but does break some approximate global symmetries. This is known as **chiral symmetry breaking**. We will discuss this further in Part II.

## Anomalies

A symmetry is anomalous if it is respected by the Lagrangian but not by the path integral measure. For a symmetry $H$ with generators $t^a$ and a gauge symmetry $G$ with generators $T^a$, we say that $H$ suffers a $G$-anomaly if the **anomaly coefficient**

$$ \mathrm{tr}(\gamma^5 t^a \\{T^b, T^c\\}) $$

is non-zero. In principle it is possible for anomalies to arise from diagrams with three different currents, but this cannot happen in the Standard Model since such diagrams always involve exactly one generator of $SU(2)_L$ or $SU(3)_C$, which is traceless. It is a somewhat magical feature of the Standard Model, which one should check from the table of field representations above, that no gauge symmetry $H$ suffers a $G$-anomaly for any gauge symmetry $G$. Indeed, this is necessary for the theory to be consistent. Nevertheless, there are several global symmetries $H$ which suffer $G$-anomalies, as we shall see.

## Summary

| | Approximate | SSB | Anomalous |
| ---------- | ---------- | ---------- | ---------- |
| $SU(3)_C$ | No  | No | No |
| $SU(2)_L \times U(1)_Y$ | No  | Down to $U(1)_Q$ | No | 
| $U(1)_Q$ | No | No | No | 
