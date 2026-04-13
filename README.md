# IGA B-Spline Basis Function Visualizer

An interactive browser-based tool for visualizing B-spline basis functions, built to support learning isogeometric analysis (IGA). Generated with [Claude](https://claude.ai) by Anthropic.

## Live demo

[https://ekimekiz.github.io/iga-basis-vis/](https://ekimekiz.github.io/iga-basis-vis/)

## Features

- Two knot vector input modes: uniform and manual
- Degree selector (p = 1–5) with open/clamped toggle
- Adjustable interior knot multiplicities with live continuity feedback
- Basis function plot with Greville abscissae and knot line overlays
- PNG and CSV export

## Implementation

Basis functions are evaluated via the Cox–de Boor recursion formula (Cox 1971, de Boor 1972). No external math libraries are used. The chart is rendered with [Chart.js](https://www.chartjs.org/) and [chartjs-plugin-annotation](https://www.chartjs.org/chartjs-plugin-annotation/).

## Usage

The tool runs entirely in the browser with no build step or dependencies to install. To use locally, just open `index.html` in any modern browser.

## Background

This tool was built as a learning aid for isogeometric analysis, specifically to build intuition about:

- How knot vector structure determines basis function shape and continuity
- The effect of knot multiplicity on continuity ($C^{p-k}$ at a knot with multiplicity $k$)
- The relationship between knot spans (elements), basis function support, and active DOFs
- Greville abscissae as natural interpolation sites for control point placement

## Author

Ekim Ekiz — [ekiz@utexas.edu](mailto:ekiz@utexas.edu)  
Department of Aerospace Engineering & Engineering Mechanics, The University of Texas at Austin

## License

MIT
