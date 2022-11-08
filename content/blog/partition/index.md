---
title: Even Degree Graph Partition

# Summary for listings and search engines
summary: Is it possible to partition the vertices of a graph into two subsets, such that in each induced subgraph every vertex has even degree?

# Link this post with a project
projects: []

# Date published
date: "2021-10-01T00:00:00Z"

# Date updated
lastmod: "2021-10-01T00:00:00Z"

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
- Graph Theory
---

## The Problem

Given any finite graph $G$, can we partition the vertex set $V = V_1 \cup V_2$ such that in the induced subgraphs $G[V_1]$, $G[V_2]$ every vertex has even degree? If every degree in the original graph is even, we are done, since we can take $V_1 = V$, $V_2 = \varnothing$. We can suppose therefore that at least one vertex in $G$ has odd degree.

It is natural to attempt to prove this result by induction, on the number of vertices in $G$ perhaps. So suppose $|G| = n$ and that the result is true for graphs of order $n-1$. We can remove a vertex $v$ from $G$ and use the inductive hypothesis to partition the remaining vertices so that they all have even degree in their respective subgraphs.

The difficulty comes when we reintroduce $v$. Suppose we assign $v$ to the subset $V_1$. Then any neighbours of $v$ in $V_1$ will gain an extra edge, and hence have odd degree. We can therefore only preserve the even degree condition if one of the two subsets contains no neighbours of $v$. But there seems to be no way to arrange for this in general.

## An Idea

It may seem, at a glance, that an inductive argument is not appropriate in this case. However, we have not used the full might of the inductive hypothesis, which states that the result is true for *all* graphs of order $n-1$, not just $G - v$. We may thus hope to construct and then partition a different graph $G'$ of order $n-1$, such that when we reintroduce $v$ *and* pass back to the original set of edges, the degrees of the vertices are unchanged (modulo two, at least).

We first note that $v$ itself must have even degree in the subgraph it eventually belongs to. We can ensure this by choosing $v$ to be a vertex of odd degree in $G$ (as noted above, such a choice is possible without loss of generality). Then $v$ must have an even number of neighbours in either $V_1$ or $V_2$ --- let's say it's $V_1$ --- and we can hence choose to reintroduce $v$ to $V_1$.

Now, how can we contruct the graph $G'$ we speculated about above? Since reintroducing $v$ introduces an extra edge to each of its neighbours in $V_1$, we would like to construct a graph such that:

1. Any neighbour of $v$ in $V_1$ has a different degree modulo two in $(G-v)[V_1]$ and $G'[V_1]$.
2. Any neighbour of $v$ in $V_2$ has the same degree modulo two in $(G-v)[V_2]$ and $G'[V_2]$.

This looks a little tricky, since the partition $V_1 \cup V_2$ we take will depend on the graph $G'$ we construct. Denote the neighbours of $v$ by $\Gamma(v)$ and focus on the graph $G[\Gamma(v)]$. Restrict the partitions to these vertices: $W_i = V_i \cap \Gamma(v)$. We know that $|W_1|$ is even and $|W_2|$ is odd. Consider therefore that:

1. $w \in W_1$ has a different number of neighbours and non-neighbours (modulo two) in $G[W_1]$.
2. $w \in W_2$ has the same number of neighbours and non-neighbours (modulo two) in $G[W_2]$.

An idea now presents itself: delete every edge in $G[\Gamma(v)]$ and introduce an edge wherever there wasn't one. Such a construction is known as the **complement** of the graph $G[\Gamma(v)]$. By virtue of the above two facts, we have hereby changed the degree of every vertex in $G[W_1]$ and left unchanged the degree of every vertex in $G[W_2]$ (modulo two). This remains true when we reattach the rest of the graph $G-v$. But this is precisely what we wanted to achieve!

## A Proof

Let us put these ideas together. Given a graph $G$ of order $n$, choose a vertex $v$ of odd degree (if no such vertex exists, we are done). From $G-v$ construct the graph $G'$ by deleting edges between those elements $v_1, v_2$ of $\Gamma(v)$ with $v_1 v_2 \in E(G)$ and introducing edges between those elements $v_1, v_2$ of $\Gamma(v)$ with $v_1 v_2 \notin E(G)$.

Apply the inductive hypothesis to $G'$. Suppose that $v$ has an even number of neighbours in $V_1$ (if not, it has an even number of neighbours in $V_2$). Then the subsets $V_1 \cup \\{ v \\}$ and $V_2$ consitute a partition of $V$ such that every vertex in the induced subgraphs has even degree .

The proof is completed by noting that the result is clearly true for $n=1$.
