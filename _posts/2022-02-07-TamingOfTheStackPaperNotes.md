---
title: 'Paper Notes:  The Taming of the Stack: Isolating Stack Data from Memory Errors (NDSS'22)'
date: 2020-03-25
permalink: /posts/2022/02/TamingOfTheStackPaperNotes/
tags:
  - Paper Notes, Static Analysis
---

## Background:
Clang's safe stack: SafeStack is an instrumentation pass that protects programs against attacks based on stack buffer overflows, without introducing any measurable performance overhead. It works by separating the program stack into two distinct regions: the safe stack and the unsafe stack. The safe stack stores return addresses, register spills, and local variables that are always accessed in a safe way, while the unsafe stack stores everything else. This separation ensures that buffer overflows on the unsafe stack cannot be used to overwrite anything on the safe stack. Ref: [LLVM SafeStack](https://clang.llvm.org/docs/SafeStack.html)

## Summary:
This paper proposes a DATAGUARD tool which ensures the spatial, type and temporal memory errors for all the stack variables. 
Only if a stack object is proven safe from these three types of memory errors can it be placed on an isolated stack.

## Motivation: 
Current defenses are too limited / expensive.
**Shadow Stack/Stack Canaries:** Protect the return address on the stack.
**Safe Stack** Protect code pointers only while the protetction is too conservative which means protect some safe pointers.

## Novelty:
Extend the protection to all the stack variables instead of the pointers.
Combine the static analysis and symbolic execution to figure out more safe variables in the stack and further reduce the overhead for run time.
