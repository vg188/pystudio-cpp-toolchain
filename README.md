# PyStudio C/C++ Toolchain

Thin build-entry repository for PyStudio native C/C++ build packages.

This repository does not contain a Termux package tree. It calls the reusable
workflow in `vg188/pystudio-termux-builds`, which selects one of the managed
source forks:

- `primary`: `vg188/pystudio-termux-source-termux`
- `secondary`: `vg188/pystudio-termux-source-pacman`

Each run selects exactly one source. The package set provides the
compiler/sysroot and common build tools needed by native Python wheels, npm
native modules, and user C/C++ projects.
