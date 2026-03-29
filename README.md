# Bipartite Dimers Project

Interactive tools for exploring dimer models on bipartite planar graphs, with a focus on lozenge tilings of the triangular lattice.

Live site: [bipartite-dimers.github.io](https://bipartite-dimers.github.io)

## Contents

- **[Lozenge Tiling Explorer](https://bipartite-dimers.github.io/lozenge.html)** -- Draw regions on the triangular lattice and sample random lozenge tilings via Glauber dynamics. Pure JavaScript, no dependencies. Includes Dinic's max-flow for initial matching, MCMC with q-volume bias, and height function visualization.

## About

Lozenge tilings are perfect matchings of the triangular lattice, equivalently dimer coverings of the hexagonal lattice. Each tiling can be viewed as a 3D stepped surface (a pile of unit cubes seen in isometric projection), with the three lozenge orientations corresponding to the three visible cube faces.

The code is written to be self-contained and student-readable, with educational comments explaining the algorithms and the underlying mathematics.
