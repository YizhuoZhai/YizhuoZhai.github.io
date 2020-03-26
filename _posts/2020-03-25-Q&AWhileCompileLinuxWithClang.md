---
title: 'Paper Reading '
date: 2020-03-20
permalink: /posts/2020/03/Q&AWhileCompileLinuxWithClang/
tags:
  - Clang 
---
This posts collects some Q & A while compiling Linux by Clang

1. 'variable length array in structure' extension will never be supported
Error fs/exofs/ore.c:153:28: error: fields must have a constant size: 'variable length array in structure' extension will never be supported
Solution: Patch: https://lore.kernel.org/kernel-hardening/20180418163546.GA45794@beast/
2. Unknown argument: '-mpreferred-stack-boundary=4'
Error: 
clang-10: error: unknown argument: '-mpreferred-stack-boundary=4'
scripts/Makefile.build:316: recipe for target 'drivers/gpu/drm/amd/amdgpu/../display/dc/calcsdd/dcn_calcdcs.o' failed
Solution: Change the Makefile of 'drivers/gpu/drm/amd/amdgpu/../display/dc/calcs/’ flag "-mpreferred-stack-boundary=4" to "-mstack-alignment=4"
