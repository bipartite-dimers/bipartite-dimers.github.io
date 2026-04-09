# Bipartite Dimers Project

Interactive tools for exploring dimer models on bipartite planar graphs, with a focus on lozenge tilings and random surfaces.

Live site: [bipartite-dimers.github.io](https://bipartite-dimers.github.io)

## Contents

- **[Lozenge Tiling Explorer](https://bipartite-dimers.github.io/lozenge.html)** — Draw regions on the triangular lattice and sample random lozenge tilings via Glauber dynamics. Includes Dinic's max-flow for the initial perfect matching, MCMC with q-volume bias, and a height-function view that renders each tiling as a 3D stepped surface of unit cubes.

- **[Lattice Creator](https://bipartite-dimers.github.io/lattice.html)** — Design your own periodic bipartite planar graph. Place black and white dots in a fundamental cell (up to 10 of each color); the tool auto-connects them into a non-crossing bipartite graph and tiles the lattice across the whole viewport. A draggable region shape (rectangle, circle, or free polygon) selects which dots form the finite graph. Supports manual edge editing with planarity warnings, balance checking, a "Show matching" feature that computes and displays one perfect matching of the induced subgraph, and PNG/JSON export.

## About

Lozenge tilings are perfect matchings of the triangular lattice, equivalently dimer coverings of the hexagonal lattice. Each tiling can be viewed as a 3D stepped surface (a pile of unit cubes seen in isometric projection), with the three lozenge orientations corresponding to the three visible cube faces.

More generally, every perfect matching of a bipartite planar graph carries a height function, which encodes the matching as a discrete surface. Sampling matchings uniformly at random — via algorithms like Glauber dynamics — produces random surfaces whose typical shape reveals deep results in combinatorics and statistical physics (limit shapes, frozen regions, fluctuations).

The two tools above sit at different stages of the same pipeline:

1. **Design the playing field** — `lattice.html` outputs a periodic bipartite planar graph.
2. **Sample a random surface on it** — `lozenge.html` runs the matching, MCMC, and rendering machinery (currently hardcoded to the triangular lattice; generalizing it to arbitrary user-designed lattices is the next step).

## Implementation

Pure HTML5 + vanilla JavaScript. Each tool is a single self-contained `.html` file with all CSS and JS inline.

The code is written to be self-contained and student-readable, with numbered sections and educational comments explaining the algorithms and the underlying mathematics.
