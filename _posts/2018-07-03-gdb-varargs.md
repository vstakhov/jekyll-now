---
layout: post
title: "GDB + varargs"
---

Current position:

```
p *(char **)(((char *)args[0].reg_save_area)+args[0].gp_offset)
```

Previous pointer (64 bit):

```
p *(char **)(((char *)args[0].reg_save_area)+args[0].gp_offset - 8)
```

Next pointer:

```
p *(char **)(((char *)args[0].reg_save_area)+args[0].gp_offset + 8)
```
