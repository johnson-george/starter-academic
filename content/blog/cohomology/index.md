---
title: Are Irrotational Vector Fields Conservative? An Excursion into Algebraic Topology

# Summary for listings and search engines
summary: A seemingly simple question in vector calculus and its suprisingly deep connections with topology.
# Link this post with a project
projects: []

# Date published
date: "2022-03-30T00:00:00Z"

# Date updated
lastmod: "2022-03-30T00:00:00Z"

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
- Geometry
- Topology
---

## Conservative and Irrotational Vector Fields

A smooth vector field $\mathbf{F}$ in $\mathbb{R}^3$ is known as **conservative** if it can be written as the gradient of a scalar field: $\mathbf{F} = \nabla f$. A vector field is termed **irrotational** if it has zero curl: $\nabla \times \mathbf{F} = \mathbf{0}$. It is not hard to check that all conservative vector fields are irrotational.

The converse also happens to be true: 

> *Theorem 1:* an irrotational vector field on $\mathbb{R}^3$ is conservative.

One consequence of this result is that the line integral of an irrotational field between any two points is independent of the path taken.

## An Exception

In electromagnetism, the magnetic field around a static current-carrying wire obeys Ampère's Law: $\nabla \times \mathbf{B} = \mathbf{0}$. We may thus hope to write the magnetic field in terms of a so-called magnetic scalar potential, $\mathbf{B} = \nabla \psi$. However, it is clear from the circulating nature of the solution,

$$ \mathbf{B}= \frac{\mu_0 I}{2 \pi r} \mathbf{e}_\phi  \ ,$$

that the integral of $\mathbf{B}$ along a circle enclosing the wire is non-zero. In fact an everywhere-defined scalar potential does not exist. This apparent conflict with Theorem 1 can be resolved in one of two ways: either we note that $\mathbf{B}$ fails to be irrotational inside the wire, where it obeys the equation $\nabla \times \mathbf{B} = \mu_0 \mathbf{J}$; or we consider the wire not to be part of our space, and treat our field as defined not on all of $\mathbb{R}^3$ (as required for the theorem to hold), but on $\mathbb{R}^3 \setminus \mathrm{line}$.

Taking this latter viewpoint, we are led to an interesting question: what features of a space permit or prevent us from expressing irrotational vector fields as the gradient of scalar fields? What is the pertinent difference between $\mathbb{R}^3$ and $\mathbb{R}^3 \setminus \mathrm{line}$ such that Theorem 1 holds for one but not the other? The answer to this question lies in the domain of topology.

## De Rham's Theorem

Given a space $M$, we can ask not just whether or not Theorem 1 holds on $M$, but indeed *to what extent* the theorem holds. To be precise, let us define an equivalence relation on the set of all vector fields on $M$ by identifying $\mathbf{F}$ and $\mathbf{G}$ if their difference is the gradient of a scalar field: $\mathbf{F} \sim \mathbf{G} \iff \mathbf{F} - \mathbf{G} = \nabla f$. This relation partitions the set of all irrotational vector fields on our space into classes. The space of all such classes is known as the **first de Rham cohomology group** $H^1(M)$. Thus, Theorem 1 above can be recast in this language as the statement that for $\mathbb{R}^3$ only one equivalence class exists, or $H^1(\mathbb{R}^3) = \\{0\\}$.

The central result of this analysis is de Rham's theorem, which relates this cohomology group to the topology of our space, as described by the **first homology group** $H_1(M)$. This is a measure of the number of loops in our space which do not form the boundary of any surface. For example, every loop in $\mathbb{R}^3$ can be thought of as the edge of some disc. However, a loop in $N = \mathbb{R}^3 \setminus \mathrm{line}$ that encircles the missing line bounds no surface (that lies entirely in the space). We thus say that $H_1(\mathbb{R}^3) = \\{0\\}$, whilst $H_1(N) = \mathbb{R}$.

As the names imply, there also exist higher homology and cohomology groups. Indeed (as we will discuss later) we can define $H_r(M)$ and $H^r(M)$ for $r$ up to the dimension of our space. De Rham's theorem makes a remarkably simple statement about them:

> *Theorem 2:* the $r^\mathrm{th}$ cohomology group and $r^\mathrm{th}$ homology group of a space $M$ are isomorphic: $ H^r(M) \cong H_r(M) $.

Thus, the trivial first homology of $\mathbb{R}^3$, in conjunction with de Rham's theorem, implies Theorem 1 above. Moreover, we also have that $H^1(N) = \mathbb{R}$, which means that any irrotational vector field on $N$ can be written in the form $\mathbf{F} = \mathbf{B}_I + \nabla f$, where $\mathbf{B}_I$ (with $I \in H^1(N) = \mathbb{R})$ is a one-parameter family of irrotational fields. The magnetic fields of the previous section serve as one such family.

## Real or Integer Homology?

The homology groups that appear in de Rham's theorem are defined with real coefficients, and may more explicitly be written $H_r(M;\mathbb{R})$. In other contexts, we more commonly work with the **integral homology groups** $H_r(M;\mathbb{Z})$, which are defined with integer coefficients.

The integral homology of a space is a somewhat 'finer' topological invariant, and indeed determines the real homology uniquely. In particular, where an integral homology group is a direct sum of $k$ copies of $\mathbb{Z}$ and a finite Abelian group, the corresponding real homology group will simply be $\mathbb{R}^k$. This extra finite group --- known as the torsion subgroup --- describes non-trivial loops that the real homology does not detect.

Consequently, it is possible for a space to have non-trivial first (integral) homology and yet nevertheless have the property that all irrotational vector fields are conservative. Perhaps the simplest example is the space $X = \mathbb{R}P^2 \times \mathbb{R}$. This is homotopy equivalent to the real projective plane $\mathbb{R}P^2$ and hence has first homology group $H_1(X;\mathbb{Z}) = \mathbb{Z}_2$. 

## Homology or Homotopy?

It is sometimes said that irrotational vector fields are conservative when the domain of the fields is **simply connected**. To be simply connected is to have trivial **first homotopy group**, $\pi_1$. Like the first homology group, the first homotopy group in some sense measures the number of the non-trivial loops in our space.

However, the first homology and first homotopy groups are in general different. A relation between them is provided by the Hurewicz theorem, which states that the first (integral) homology group is the Abelianisation of the first homotopy group --- that is, the quotient of $\pi_1$ under the equivalence relation $xy \sim yx$.

Thus, if our space is simply connected, then it also has trivial first homology group, and irrotational vector fields are conservative, as is claimed. However, the above discussion shows that simple connectedness isn't a necessary condition for this to hold. Indeed, any space whose first homotopy group has trivial Abelianisation will have this property. Such groups as known as **perfect groups**, and are in some sense maximally non-Abelian. The smallest non-trivial example is the alternating group $A_5$.

An important example of a space with perfect fundamental group is the **Poincaré homology sphere**. This is obtained as the quotient of $SO(3)$ --- the rotational symmetries of 3D space --- by the icosahedral group $I \cong A_5$ --- the rotational symmetries of the icosahedron. This quotient can hence be thought of as the space of all geometrically distinguishable orientations of the icosahedron. Passing to the double cover of both groups, we can also write this as the quotient $Y = S^3 / 2I$, where $2I$ is the binary icosahedral group (a perfect group also). This space has $\pi_1(Y) = 2I$.

There is a great deal of interesting mathematics concerning such 'spheres' with perfect $\pi_1$. However, if we seek a space which is not simply connected but on which irrotational vector fields are conservative, a more straightforward example would simply exploit the difference between real and integral homology. For example, the space $X = \mathbb{R}P^2 \times \mathbb{R}$ considered in the previous section has $\pi_1(X) = H_1(X;\mathbb{Z}) = \mathbb{Z}_2$, and yet the first de Rham cohomology group of this space is trivial.

## Generalising: Higher Cohomology

Just as the curl of the gradient of any scalar field is zero, so the divergence of the curl of any vector field is zero. So, just as above, we can ask: to what extent can a **solenoidal vector field** (one with zero divergence) be written as the curl of another vector field? The answer to this question depends on the space $M$ our fields live on<sup>1</sup>, and is quantified by the second de Rham cohomology group, $H^2(M)$.

We can also define higher homology groups. Where the first homology group quantifies the number of non-trivial loops in our space, the second homology group $H_2(M)$ quantifies the non-trivial closed surfaces (or more precisely, those surfaces which are not the boundaries of some volume). All closed surfaces in $\mathbb{R}^3$ bound their interior, and so $H_2(\mathbb{R}^3) = \\{0\\}$. However, remove a point from $\mathbb{R}^3$ and this is no longer the case --- surfaces which enclose this point are not the boundaries of any volume. We hence have $H_2(\mathbb{R}^3 \setminus \mathrm{point}) = \mathbb{R}$. 

As we noted above, de Rham's theorem states that the $r^\mathrm{th}$ homology and $r^\mathrm{th}$ cohomology groups of a space are isomorphic. Thus, there exist solenoidal fields on $\mathbb{R}^3 \setminus \mathrm{point}$ which cannot be written as the curl of another vector field. The magnetic field around a magnetic monopole is an example of such a field. This fact (after some explication) leads to a famous observation of Dirac, that the existence of a magnetic monopole in our universe would necessitate the quantisation of electric charge.

There is no relation between higher homology and homotopy groups in general (although the Hurewicz theorem provides a condition under which they are isomorphic). Thus, one should not make the mistake of invoking the second homotopy group $\pi_2$ to conclude that a vector potential must exist, as the following example illustrates.

Let $Z = T^2 \times \mathbb{R}$, where $T^2$ is the 2-torus. Then $H_2(Z) = \mathbb{R}$ but $\pi_2(Z) = \\{0\\}$. Despite having trivial second homotopy group, there exist solenoidal fields on $Z$ which cannot be written as the curl of another vector field. The simplest example of such a field is $\mathbf{B} = B \mathbf{e}_3$, corresponding to a constant vector field pointing along the $\mathbb{R}$ direction. Integrating this field over the torus at some fixed $z \in \mathbb{R}$ gives a positive number, yet the integral of any curl over such a surface must be zero by Stokes' theorem.

There is a final chapter to this story which is rarely discussed. The third homology group of a space describes the number of 'non-trivial volumes'. The third de Rham cohomlogy group describes the extent to which a scalar field can be written as the divergence of a vector field. This decomposition is always possible on $\mathbb{R}^3$ --- for example, the field $f = c$ can be written as the divergence of $\mathbf{F} = c x \mathbf{e}_1$. On topologically less trivial spaces, such as the 3-sphere, no such vector field exists.

<sup>1</sup><sub>In order to cast the discussion of this section into the familiar language of vector calculus, we shall need to assume that our space $M$ is orientable. This technical requirement allows us to define the Hodge star operator.</sub>

## Final Words

The discussion above has repeatedly featured the curl of a vector field, and so has been inherently three-dimensional. Nevertheless, there is a simple generalisation of the above ideas to higher dimensions. The curl is replaced by a more general operator, the **exterior derivative**. The cohomology groups of a given space capture the extent to which certain fields (namely, differential forms) can be expressed as the exterior derivative of others. As in three dimensions, these groups are isomorphic to the corresponding homology groups, which describe the number and nature of the holes in our space.
