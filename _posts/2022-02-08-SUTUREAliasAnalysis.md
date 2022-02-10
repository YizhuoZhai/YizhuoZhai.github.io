---
title: 'Paper Notes: Statically Discovering High-Order Taint Style Vulnerabilities in OS Kernels (CCS 2021)'
date: 2022-02-08
permalink: /posts/2022/02/SUTUREAliasAnalysis/
tags:
  - Static Analysis
---

## Novelty: 
SUTURE employs a novel summary-based high-order taint flow construction approach to efficiently enumerate the cross-entry taint flows, while incorporating multiple innovative en- hancements on analysis precision that are unseen in existing tools, resulting in a highly precise inter-procedural flow-, context-, field-, index-, and opportunistically path-sensitive static taint analysis.  

## Notes: 
The main focus is how to decide the alias relations/taint rules across the system call. In this paper they treat the object which has the same access path and the same type. The access path means from the same instance, following the same dereference offset.

