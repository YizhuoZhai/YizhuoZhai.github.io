---
title: 'Bug Analysis: Type Confusion in Syzbot'
date: 2022-02-09
permalink: /posts/2022/02/TypeConfusionBug/
tags:
  - Bug Analysis, Type Confusion
---

Syzbot Report: https://syzkaller.appspot.com/bug?id=8393c021d960cd9b36203efd312343a26d011997

```c
 pppol2tp_connect-> l2tp_tunnel_create ->setup_udp_tunnel_sock

 udp_sk(sk)->encap_type = cfg->encap_type //struct udp_sock{__u8 encap_type;}

 socket_create 
```

