---
title: 'Symmetries of the Standard Model V: Summary and Extensions'

# Summary for listings and search engines
summary: Summary of all symmetries of the Standard Model, with brief discussion of how they are modified by common extensions to the theory.

# Link this post with a project
projects: []

# Date published
date: "2021-09-30T00:00:00Z"

# Date updated
lastmod: "2021-09-30T00:00:00Z"

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

## Extensions

In this series we have discussed the symmetries of the Standard Model in its 'standard' form. Some aspects of the theory, such as the Higgs sector and the neutrino mass terms, have not been definitively established, and it is quite possible that nature behave somewhat differently from the present model. For example, electroweak symmetry could be broken by an extended sector, containing the Higgs boson alongside other scalar fields. Likewise, the neutrino masses may receive contributions (solely or partially) from Majorana terms. The current model is merely the simplest one consistent with current experimental constraints, but future experiments may demand that we extend our model. 

In fact, even at present there are several theoretical and experimental motivations for such extensions. Attempts to understand why the gauge group takes the form it does, why there are three generations, and why each generation has the structure it does, lead naturally to grand unified theories, with a single simple gauge group. On the other hand, the existence of dark matter and the apparent non-existence of the QCD theta term motivate the addition of further fields to the theory. In this final part of the series we will look at some natural extensions of the Standard Model, and how they impact its symmetries.

## Majorana Neutrinos

There is in fact one term we have neglected to add to the Lagrangian throughout this series, consistent with both renormalizability and the gauge symmetry of the theory. This is the Majorana mass term for the right-handed neutrinos:

$$ \mathcal{L}\_m = -m \epsilon^{ab} \nu^a_R \nu^b_R + \mathrm{h.c.}$$

Here $m$ is a matrix in flavour space. Such a term exists only for the right-handed neutrinos since they are the only fields in the theory which transform as singlets under each factor of the gauge group. 

The Majorana mass term violates lepton number (and also breaks explicitly the $T^3_R$ subgroup of $SU(2)_R$). Thus, with the inclusion of this term the theory possesses no non-anomalous exact global symmetries ($B-L$ being the only such symmetry previously). The only exact anomalous symmetry of our new Lagrangian is baryon number.

The diagonalisation of the mass terms is slightly more complicated in this case, though it is straightforward to sketch the effect on the discrete symmetries. We note that $\mathcal{L}\_m$ above is not invariant under neutrino rephasings, unlike the diagonalised Yukawa mass terms. Thus, after diagonalisation, the mass terms possess only a $U(1)^3$ flavour symmetry (corresponding to charged lepton rephasings), and this allows us to remove only three phases from the PMNS matrix. There are thus three $CP$-violating phases in the lepton sector in this case.

## Two Higgs Doublets

Though it is possible to give all fermions mass *and* break electroweak symmetry with just a single complex scalar doublet, there is an (only marginally more complicated) alternative involving two such doublets. Experimental constraints on the Higgs sector are weak, and such a scenario is consistent with current data.  Moreover, in theories such as those involving supersymmetry or axions, it is often natural or even necessary for two Higgs doublets to exist.

In the simplest of such models, the quark Yukawa terms and Higgs potential are replaced by the Lagrangian:

$$\mathcal{L}\_{2HD} = V(\phi_1,\phi_2) - Y_d \bar{Q}\_L \phi_1 d_R - Y_u \bar{Q}\_L \phi_2^c u_R + \mathrm{h.c.}$$

For the leptons, we can freely choose to couple each Yukawa term to either of the two Higgs fields.

The maximum possible symmetry of the potential is $U(2)_1 \times U(2)_2$, which we can write as $SU(2)_1 \times U(1)_1 \times SU(2)_2 \times U(1)_2$ up to discrete quotients. However, the couplings to $Q_L$ prevent us from performing independent $SU(2)$ rotations of the two Higgs doublets, and so in fact the maximum symmetry of our Lagrangian is $SU(2) \times U(1)_1 \times U(1)_2$. The two $U(1)$ factors (corresponding to independent rephasings of the two Higgs fields) can equally be written as the product of a 'vectorial' $U(1)$ (rephasing both fields by the same amount) and an 'axial' $U(1)$ (rephasing both fields by opposite amounts).

The quarks and leptons must be charged under these two $U(1)$ symmetries if the Yukawa terms are to be invariant. Indeed, the required charges under the vectorial symmetry are precisely the hypercharges $Y$ of the Standard Model. Under axial rephasings, which we shall denote $U(1)_X$, we can take all right-handed quarks to have charge $-1/2$ and all left-handed quarks charge zero. The exact lepton charges will depend on the binary choices made in that sector. The maximal symmetry group of our Lagrangian can hence be written $SU(2)_L \times U(1)_Y \times U(1)_X$ --- that is, as the product of the electroweak symmetry group with a single new global symmetry.

The most general potential invariant under this group is:

$$\begin{align}
V(\phi_1,\phi_2) = &\lambda_1 (\phi_1^\dagger \phi_1)^2 - \mu_1^2 \phi_1^\dagger \phi_1  + \lambda_2 (\phi_2^\dagger \phi_2)^2 - \mu_2^2 \phi_2^\dagger \phi_2 \\\\ &+\lambda_3 (\phi_1^\dagger \phi_1)(\phi_2^\dagger \phi_2) +  \lambda_4 (\phi_1^\dagger \phi_2)(\phi_2^\dagger \phi_1) \ .
\end{align}$$

If the potential is such that both fields acquire a vacuum expectation value, then in general there will be no unbroken symmetry. Thus, we must restrict the form of the potential further to reproduce the correct pattern of symmetry breaking.

> *Exercise:* An unbroken generator $T$ satisfies $T \phi_1^0 = T \phi_2^0  = 0$, where $\phi_{1,2}^0$ are the vacuum expectation values of the Higgs fields. Working with the convention that $\phi_1^0 = (0,v)$, show that all five of the above symmetries are broken unless $\phi_1^0$ and $\phi_2^0$ are parallel or perpendicular. Show that in either case there is only one unbroken symmetry, and that it is (respectively) $T^3 + Y$ or $T^3 + X$.

## Axions

We mentioned in Part IV that in principle the Standard Model should contain a QCD theta term, but that no effects of this term have yet been discovered. This is not for lack of trying, however. Indeed, current experiments constrain the constant $\theta\_{QCD}$ to be less than about $10^{-10}$. Why this parameter should be so unnaturally small is known as the **strong CP problem**.

We also claimed that the QCD theta term would be unphysical if there existed a symmetry (such as the chiral rotation of a single quark flavour) which was respected by the Lagrangian but which suffered a QCD anomaly. With general Yukawa matrices (as in reality), no such symmetry exists. We may attempt to rephase $u_R$ only, for example, but the structure of the Yukawa terms requires that we also rephase the Higgs and, in turn, the other right-handed fermions, in order to maintain invariance. Such a symmetry is necessarily some combination of $B-L$ and hypercharge $Y$, and is non-anomalous.

The Peccei-Quinn solution to the strong CP problem invokes a second Higgs doublet to bypass the above obstruction. Indeed, the symmetry $U(1)\_X$ of the previous section is both respected by the Lagrangian (by construction) and suffers a QCD anomaly (by virtue of acting equally on only right-handed quarks). In this context we call $U(1)\_X$ the Peccei-Quinn symmetry.

As the exercise in the previous section illustrates, $U(1)\_{PQ}$ must be spontaneously broken by any potential which does not break $Q = T^3 + Y$. Hence, our theory must contain a Nambu-Goldstone boson associated with the Peccei-Quinn symmetry. This boson is known as the **axion**. The axion is not exactly massless on account of the anomaly, but is nevertheless light. The existence of a new light scalar particle would appear to have observable consequences, and indeed the axion we have described here has been ruled out experimentally. Nevertheless, the Peccei-Quinn theory forms the basis for more complicated axion models which are compatible with current observations.

## Summary

Here are the summary tables from the previous parts of the series.

| | Approximate | SSB | Anomalous |
| ---------- | ---------- | ---------- | ---------- |
| $SU(3)_C$ | No  | No | No |
| $SU(2)_L \times U(1)_Y$ | No  | Down to $U(1)_Q$ | No | 
| $U(1)_Q$ | No | No | No | 
| $SU(3)_V$ |  Yes |No | No |
| $SU(3)_A$ | Yes |Yes | QED ($\lambda_8 + \sqrt{3} \lambda_3$) | 
| $U(1)_V$ |  No |No | No |
| $U(1)_A$ | Yes |Yes | QCD and QED | 
| $SU(2)_L \times SU(2)_R$ |$T_R^1$ and $T_R^2$ | Down to $SU(2)_V$ | No | 
| $SU(2)_V$ | $T^1$ and $T^2$ | No | No | 
| $U(1)_{B+L}$| No | No | Electroweak | 
| $U(1)_{B-L}$| No | No | No |

| | QCD | Electroweak | QED |
| ---------- | ---------- | ---------- | ---------- |
|$C$| Yes | No | Yes |
|$P$| If $\theta_{QCD} = 0$ | No | Yes |
|$T$ or $CP$ | If $\theta_{QCD} = 0$  | If $\theta_{CKM} = \theta_{PMNS} = 0$ | Yes |

