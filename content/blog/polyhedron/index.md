---
title: Euler's Polyhedron Formula and the Gauss-Bonnet Theorem

# Summary for listings and search engines
summary: A beautiful theorem relating the average curvature of some surface to a property of polyhedra with the same topology.

# Link this post with a project
projects: []

# Date published
date: "2022-01-24T00:00:00Z"

# Date updated
lastmod: "2022-01-24T00:00:00Z"

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

## Euler's Polyhedron Formula

There is a wonderful theorem due to Euler (1752) which states that for a convex polyhedron with $V$ vertices, $E$ edges, and $F$ faces:

$$ V - E + F = 2 \ . $$

In this post we will sketch a proof of this result, and then extend it to non-convex polyhedra. Our starting point will be a result in the subject of spherical geometry.

## The Angle Defect Formula

For a triangle drawn on the plane, the sum of the interior angles is $\pi$. For a triangle drawn on the surface of a unit sphere, whose sides are arcs of great circles, the internal angles $\alpha,\beta,\gamma$ satisfy

$$ \alpha + \beta + \gamma - \pi = \text{area of triangle} \ . $$

To prove this, consider extending the sides of the triangle into three great circles. These divide the sphere into eight regions. By the symmetry of the figure under the exchange of antipodal points, our triangle and the three faces which neighbour it constitute exactly half the area of the sphere. The total area of these four regions is hence $2 \pi$.

Now our triangle together with any one of the three neighbouring regions form the surface of a spherical wedge. A wedge of angle $\theta$ has surface area $2 \theta$ (this gives an area $4 \pi$ when $\theta = 2 \pi$). If we consider the three possible wedges in turn, their total area is hence

$$ 2(\alpha + \beta + \gamma) \ . $$

Now, this total area can be written as the sum of the areas of those regions neighbouring our triangle, plus thrice the area of the triangle. Since we know that the four regions together have an area of $2 \pi$, we can rearrange for the area of our triangle, giving the angle defect formula quoted above.

## Back to Euler

With the angle defect formula to hand, we can embark on our proof of Euler's formula. Given any convex polyhedron, choose a point in its interior as the origin and form the projection onto the surface of the unit sphere. Deform the edges so that they form the arcs of great circles (that this is always possible is plausible, though we will not prove it).

For any face with four or more vertices, consider inserting a new edge. This adds precisely one face and one edge, and hence leaves unchanged the quantity $\chi = V - E + F$. We can hence, without loss of generality, take our polyhedron to be constructed from triangular faces.

For such a polyhedron, each face has three edges, and each edge is shared by two faces. Thus we can relate

$$ E = \frac{3}{2} F  \ .$$

For each triangular face, we can apply the angle defect formula. Summing over all faces, we find

$$ \sum_F (\alpha + \beta + \gamma - \pi) = \text{area of sphere} = 4 \pi  \ . $$

This sum over all faces of all internal angles of each face can be reorganised as a sum over all vertices of all angles at each vertex. But the angles at a vertex sum to $2 \pi$, and hence the above formula reads

$$ 2 \pi V - \pi F = 4 \pi \ . $$

Taken together, the results above can be combined to give Euler's formula:

$$ V - E + F = 2  \ .$$ 

## Generalising the Angle Defect Formula

For those familiar with Riemannian geometry, the notion of an angle defect may appear connected with the notion of parallel transport. Indeed, the failure of a vector to return to itself upon parallel transport around some small rectangle seems to correspond to the failure of the interior angles to sum to $2 \pi$. But this failure can also be quantified by the Riemann tensor, a measure of the curvature of the space.

We may thus hope to generalise the angle defect formula to arbitrary curved surfaces thus. Let $K$ be an appropriate scalar curvature, which takes the value $1$ for the unit sphere. Let $\alpha,\beta,\gamma$ be the internal angles of a triangle $\triangle$ on this surface, whose edges are geodesics. Then we postulate:

$$ \alpha + \beta + \gamma - \pi = \int_{\triangle} K \ \mathrm{d}A \ .$$

This formula turns out to be true --- it is called the local Gauss-Bonnet theorem, and holds with $K$ the Gauss curvature of the surface.

## The Gauss-Bonnet Theorem

With this new formula to hand, we can repeat the previous steps for any polyhedron, not necessarily a convex one. First map the polyhedron to some smooth surface, topologically equivalent to it. Deform the edges so that they are geodesics on this surface, and insert new edges so that all faces are triangular. We then have $E = 3F/2$ as before, but now

$$ \sum_F (\alpha + \beta + \gamma - \pi) = \int K \ \mathrm{d}A \ .$$

Reorganising the sum over faces as a sum over vertices, this gives

$$ 2 \pi V - \pi F = \int K \ \mathrm{d}A  \ , $$

and altogether we have the global Gauss-Bonnet theorem:

$$ V - E + F = \frac{1}{2 \pi} \int K \ \mathrm{d}A  \ . $$

## Musings

At once this theorem tells us two pretty facts about polyhedra and curved surfaces. Firstly, it implies that for any two polyhedra which are topologically equivalent, the quantity $\chi = V - E + F$ --- known as the Euler characteristic --- must take the same value, since both can be mapped to the same surface with fixed integrated curvature.

Secondly, it implies that for any two smooth surfaces which are topologically equivalent, the integrated curvature must take the same value, since both surfaces can be triangulated with the same polyhedron.

Said more succinctly, the integrated curvature and the Euler characteristic are both **topological invariants** of closed surfaces, equal to one another by the Gauss-Bonnet theorem.
