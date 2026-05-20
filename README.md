# msekit

A Python toolkit for physically grounded materials science modeling, connecting atomistic simulations, local mechanics, and educational workflows.

## Purpose

`msekit` is a materials science and engineering toolkit developed as part of Project Koios.

The package focuses on transparent, inspectable modeling tools for connecting atomistic simulations with continuum mechanics and materials science education.

The initial emphasis is on:

- atomic geometry
- neighbor-based deformation analysis
- local deformation gradients
- local strain tensors
- coarse-grained stress fields
- basic structure utilities
- bridges to MD and DFT workflows

The goal is not to hide the physics behind black-box routines. The goal is to expose the computational structure clearly enough that students, researchers, and instructors can inspect the method, modify it, and connect it to the underlying theory.

## Current Status

`msekit` is in early development.

The first development target is local strain analysis from atomistic configurations.  For each atom $a$, the local deformation gradient $\mathbf{F}_a$ is computed by comparing reference neighbor vectors with deformed neighbor vectors

## Planned Package Structure

```text
msekit/
├── src/
│   └── msekit/
│       ├── __init__.py
│       ├── lattices/
│       │   ├── __init__.py
│       │   └── bravais.py
│       ├── md/
│       │   ├── __init__.py
│       │   ├── mechanics/
│       │   │   ├── __init__.py
│       │   │   ├── deformation.py
│       │   │   ├── strain.py
│       │   │   └── stress.py
│       │   └── io/
│       │       ├── __init__.py
│       │       └── lammps.py
│       ├── dft/
│       │   ├── __init__.py
│       │   └── structure.py
│       └── io/
│           ├── __init__.py
│           ├── xyz.py
│           └── cif.py
├── notebooks/
│   └── dev/
│       └── md/
│           └── 01_local_strain_from_neighbors.ipynb
├── tests/
│   └── md/
│       └── mechanics/
│           ├── test_deformation.py
│           └── test_strain.py
├── docs/
├── LICENSE
├── LICENSE-docs
└── README.md
```

