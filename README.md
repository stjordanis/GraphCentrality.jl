# Centrality

[![Build Status](https://travis-ci.org/sbromberger/Centrality.jl.svg?branch=master)](https://travis-ci.org/sbromberger/Centrality.jl)

Performant centrality measures on Graphs.jl graphs.

```
julia> g = Centrality.readgraph("$(Pkg.dir("Centrality"))/test/testdata/graph-500-50000.csv")
Directed Graph (500 vertices, 50000 edges)

julia> @time z = betweenness_centrality(g, normalized=false);
elapsed time: 4.32613941 seconds (1258181320 bytes allocated, 16.05% gc time)
```

vs NetworkX:

```
In [244]: %time z = nx.betweenness_centrality(g,normalized=False)CPU times: user 9.07 s, sys: 109 ms, total: 9.17 s
Wall time: 9.11 s
```

##TODO
- [X] Finish betweenness_centrality with dijkstra
- [X] Optimize code
- [ ] TESTS!
- [ ] New centrality measures:
 - [ ] Closeness
 - [ ] Load
 - [ ] Eigenvector
 - [ ] Current flow betweenness?
 - [ ] Current flow closeness?
