---
id: lzel0xtqe117z2xkki5gi51
title: Perf
desc: ''
updated: 1666532513256
created: 1666531638110
---

### ensure cache-misses printed

`perf stat -B -e cache-references,cache-misses,cycles,instructions,branches,faults,migrations <program>`