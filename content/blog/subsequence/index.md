---
title: Longest Increasing Subsequence

# Summary for listings and search engines
summary: Given a finite sequence of real numbers, how can one find the longest strictly increasing subsequence?

# Link this post with a project
projects: []

# Date published
date: "2021-04-28T00:00:00Z"

# Date updated
lastmod: "2021-04-28T00:00:00Z"

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
- Algorithms
---

## The Problem

Given a finite sequence $(a_1, a_2, \ldots, a_k)$ of real numbers, how can one find the longest subsequence satisfying $a_{n(i+1)} > a_{n(i)}$ for all $i$? A sequence of length $k$ has $2^k$ subsequences and checking each case may not be feasible.

## A Solution

Suppose our sequence begins $(1,10,11,12,2,3,\ldots)$. If we begin our subsequence with $a_1 = 1$, we are left with the decision whether to next take $a_2 = 10$, thus committing to the exclusion of $a_5$ and $a_6$, or whether perhaps to skip the second to fourth elements in the hope of finding more elements less than $a_2$ further down the line. Which decision is better could depend on elements all the way to the end of the sequence.

Thus, one is tempted to start thinking from the other end. Suppose we begin with $a_k$. Clearly there is nowhere else to go, and our longest subsequence will have length one. Now suppose we begin with $a_{k-1}$. We have hardly more choice in this case: we include $a_k$ if it is greater than $a_{k-1}$, and not otherwise.

Now suppose we begin with $a_{k-2}$. We have already determined the longest subsequence beginning with $a_i$ for each $i > k-2$. Thus, we need only check which such $a_i$ satisfy $a_i > a_{k-2}$, and of those, prepend $a_{k-2}$ to the longest corresponding subsequence. This will generate the longest subsequence beginning with $a_{k-2}$.

It's clear we can continue this process, tracking backwards through the sequence to determine the longest ascending subsequence beginning with each element, and once this is complete we can choose the longest among them as our solution.

## An Implementation

One way to implement this idea uses Python dictionaries:

```python
a = [1,10,11,12,2,3,4,13,14,15,5,6,7,8]
k = len(a)

# prepend a small number a_0 so that the longest subsequence necessarily begins with a_0
a = [min(a)-1] + a
# create a dictionary of the longest subsequences starting from a_i
longsubseq = {k : [a[-1]]}

for i in reversed(range(k)):
    # restrict the dictionary to those j with a_j > a_i
    lss = {j: longsubseq[j] for j in range(i, k+1) if a[j] > a[i]}
    # from these choose m such that a_m begins the longest subsequence
    m = max(lss, key = lambda j: len(lss[j]), default = 0)
    # append this subsequence to a_i
    if m == 0: subseq = [a[i]]
    else: subseq = [a[i]] + longsubseq[m]
    longsubseq[i] = subseq

solution = longsubseq[0][1:] 
```

I don't know that dictionaries are necessarily the fastest way to implement this idea, but they are conceptually clean at least.
