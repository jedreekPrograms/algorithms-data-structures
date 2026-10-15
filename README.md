# Algorithms & Data Structures — C/C++ Labs

Coursework from **Algorithms and Data Structures** at Wrocław University of Science and Technology. The repository combines implementations of fundamental algorithms with experiments on operation counts, runtime and input-dependent behavior.

**Scope:** a collection of independent C/C++ exercises and experiment artifacts. It is not one application with a single root build.

## Laboratory map

| Directory | Topics | Example work |
| --- | --- | --- |
| [lista1](lista1/) | Basic data structures | Stack, queue, singly and doubly circular linked lists |
| [lista2](lista2/) | Sorting and structured search | Insertion/quick/hybrid sorting, merge-based sorting and matrix search |
| [lista3](lista3/) | Selection and search | Randomized selection, median of medians, group-size comparisons and binary-search comparisons |
| [lista4](lista4/) | Trees and graphs | BST, splay trees, Prim/Kruskal minimum spanning trees and information propagation |

The laboratory directories also contain assignment notes, benchmark output, reports, plotting scripts and figures. Folder and source names retain the coursework's original Polish terminology.

## Engineering focus

- Implementing data structures and their operations directly.
- Measuring comparisons, swaps, pointer operations and tree height.
- Comparing randomized and ordered input scenarios.
- Separating theoretical complexity from observed experimental behavior.
- Generating figures from collected results.

## Build individual exercises

Use a C11 compiler for the C exercises and a C++17 compiler for the C++ examples. Some directories provide their own CMake or Makefile configuration.

For the stack/queue demonstration, from the repository root:

```shell
cc -std=c11 lista1/zadanie1/main.c lista1/zadanie1/queue.c lista1/zadanie1/stack.c -o stack-queue
./stack-queue
```

For the standalone BST demonstration:

```shell
c++ -std=c++17 lista4/zadanie1/main.cpp -o bst-demo
./bst-demo
```

On Windows, use the corresponding executable filename produced by your compiler. The examples above show compilation from source rather than relying on historical binaries included with the coursework.

Each task has its own input and execution conventions. Inspect its `main` function, local build file or experiment script before running a larger benchmark; there is no shared root command that runs every exercise.

## Reports and experiments

- [Selection reports](lista3/sprawozdania/) discuss the selection and search experiments.
- [BST experiments](lista4/zadanie2/) and [splay-tree experiments](lista4/zadanie4/) include result tables and figures.
- [Minimum spanning tree project](lista4/zadanie5/) includes its own source, Makefile and plotting code.

Python is used for the plotting scripts, not as the primary implementation language of the algorithms.

## Repository status

This repository preserves academic implementations and their associated experiment artifacts. It does not currently provide a unified automated test/CI pipeline. Reported results should be read together with the relevant input, script and experiment configuration.
