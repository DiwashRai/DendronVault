
### ensure cache-misses printed

`perf stat -B -e cache-references,cache-misses,cycles,instructions,branches,faults,migrations <program>`