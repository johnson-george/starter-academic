---
title: 'Symmetries of the Standard Model II: The Quark Sector'

# Summary for listings and search engines
summary: Global symmetries of the low-energy theory, with gauge group $SU(3)_C \times U(1)_Q$ and Dirac mass terms for the fermions.

# Link this post with a project
projects: []

# Date published
date: "2021-09-22T00:00:00Z"

# Date updated
lastmod: "2021-09-22T00:00:00Z"

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

At low energies, the Standard Model has unbroken gauge group $SU(3)_C \times U(1)_Q$. The heavy Higgs and massive gauge bosons can be ignored, leaving a theory of massless gauge bosons and several flavours of Dirac fermion. We will discuss the continuous global symmetries of this theory, focusing on the quark sector.

## Flavour Symmetries

With $n_f$ flavours of quark, the largest possible global symmetry group consists of independent unitary rotations of the left-handed quarks and the right-handed quarks, that is, $U(n\_f)\_L \times U(n\_f)\_R $. Such symmetries are sometimes called **flavour symmetries**. Ignoring discrete symmetry quotients, this can be written
$$ SU(n\_f)\_L \times SU(n\_f)\_R \times U(1)\_L \times U(1)\_R  \ .$$
It is sometimes useful to rewrite left- and right-handed rotations in terms of rotations of both chiralities by the same amount and by opposite amounts. Such symmetries are called **vector symmetries** and **axial symmetries** respectively. Thus we are tempted to write the above symmetry group as
$$ SU(n\_f)\_V \times SU(n\_f)\_A \times U(1)\_V \times U(1)\_A  \ .$$
In fact there is a small subtlety here. It is not the case that axial special unitary transformations form a group (they are not closed under composition). More precisely, we should think of $SU(n\_f)\_A$ as the coset $SU(n\_f)\_L \times SU(n\_f)\_R  / SU(n\_f)\_V$.

## Exact Symmetries

Such a symmetry is exact when all the quarks are massless. If the quarks are not massless but all have the same mass, the vector symmetry is exact but none of the axial symmetries are. In the case that all the quark masses are different and non-zero, as in reality, the exact symmetry group is $U(1)\_V^{n\_f}$, corresponding to number conservation of each quark flavour.

>*Exercise:* show that if there are $n_0$ massless quarks and $n_i$ quarks of mass $m_i > 0$, then the exact symmetry group is
>$$  U(n\_0)_R \times U(n\_0)\_L \times \prod_i U(n\_i)\_V  \ .$$

In the Standard Model, the lightest three quarks (the up, down, and strange) have sufficiently small masses that for $n_f = 3$ we can consider $U(n_f) \times U(n_f)$ to be a good approximate symmetry. It is an even better approximate symmetry for $n_f = 2$.

## Spontaneous Symmetry Breaking

All axial symmetries are broken by the vacuum due to the non-zero VEV of the quark bilinears $\bar{q}q$. Note that the broken gauge symmetry $SU(2)_L \times U(1)_Y$, acting on quarks, is in fact a subgroup of $U(n_f)_L \times U(n_f)_R$, provided we take $n_f = 6$. And indeed, spontaneous breaking of the axial symmetries translates into spontaneous breaking of the gauge symmetry down to $U(1)_Q$. One might wonder, therefore, whether the chiral condensate alone could be responsible for this pattern of symmetry breaking. However, this will naturally give the gauge bosons masses of order the QCD scale (around $100\ \mathrm{MeV})$ rather than the observed scale of $100\ \mathrm{GeV}$. Furthermore, the Higgs serves a second purpose in the Standard Model (in addition to breaking electroweak symmetry), which is to give masses to the quarks and leptons. Without the Higgs, the gauge symmetry can only be exact if all the quarks and leptons are massless, which is not the case.

## Anomalies

As well as being inexact and spontaneously broken by the vacuum, the axial symmetries are also anomalous. In particular, axial $U(1)_A$ suffers both a QCD anomaly and a QED anomaly. There is also one generator of axial $SU(n_f)_A$ which suffers a QED anomaly --- for $n_f = 3$ this is $\lambda_8 + \sqrt{3} \lambda_3$. The aforementioned QCD anomaly is the supposed explanation for the lack of a fourth ($n_f = 2$) or ninth ($n_f = 3$) light meson. 

One might suspect that the QED anomaly suffered by $SU(n\_f)\_A$ would also raise the masses of some of the other light mesons. This is a rather complicated story which we will briefly discuss in Part IV. For the present moment we note that if we neglect electric charge ($e = 0$), the only anomalous symmetry is axial $U(1)\_A$:
$$ \partial_\mu J_5^\mu = -\frac{n_f g_s^2}{32 \pi^2} \epsilon\^{\mu \nu \rho \sigma}F^a_{\mu \nu} F^a_{\rho \sigma} \ .$$ 

## The Lepton Sector

In principle a similar study is warranted of the global continuous symmetries of the lepton sector. However, this is vastly more simple. Firstly, without the strong dynamics of QCD, there is no chiral condensate, so no spontaneous symmetry breaking. Secondly, the lepton masses are sufficiently different that no flavour symmetry can fairly be called approximate. We note, however, that to the extent that any $U(n_f)_L \times U(n_f)_R$ flavour symmetry *could* be considered approximate, the axial symmetries would suffer a QED anomaly as in the quark case.

>*Exercise:* As we stated in Part I, a generator $T$ of $SU(n\_f)\_A$ suffers a QED anomaly if $\mathrm{tr}(TQ^2) \neq 0$, where $Q$ is the generator of electric charge. Show that in general there is one such anomalous generator, but that if we consider a flavour symmetry amongst only the charged leptons, or only the neutrinos, then there is no QED anomaly.

## Summary

| | Approximate | SSB | Anomalous |
| ---------- | ---------- | ---------- | ---------- |
| $SU(3)_V$ |  Yes* |No | No |
| $SU(3)_A$ | Yes |Yes | QED ($\lambda_8 + \sqrt{3} \lambda_3$) | 
| $U(1)_V$ |  No |No | No |
| $U(1)_A$ | Yes |Yes | QCD and QED | 

*Note that the two diagonal generators of $SU(3)_V$ are exact symmetries. One of these can be identified with electric charge $Q$. Together with $U(1)_V$ they form the $U(1)^3_V$ symmetry group corresponding to conservation of each quark flavour.

