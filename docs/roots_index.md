# Roots index

This document describes the root-vector files selected for the first curated release of this benchmark repository.

## Associated publication

The numerical root vectors included in this repository are associated with the benchmark study reported in:

Jiménez-Islas, H., Calderón-Ramírez, M., Martínez-González, G. M., Calderón-Álvarado, M. P., & Oliveros-Muñoz, J. M. (2019). Multiple solutions for steady differential equations via hyperspherical path-tracking of homotopy curves. *Computers and Mathematics with Applications*. https://doi.org/10.1016/j.camwa.2019.10.023

The associated publication presents a multiple-solution strategy for steady ordinary and partial differential equations. The methodology combines finite-difference discretization, homotopy continuation, and hyperspherical path-tracking to locate multiple roots of the nonlinear algebraic systems obtained after discretization.

## Scope of this release

The first curated release of this repository is restricted to raw root-vector files from the natural convection benchmark.

Only files following the naming pattern below are included:

```text
XRAIZ*.txt
```

These files are preserved as raw algebraic root vectors. They are intended to support reproducibility, verification, and comparison of nonlinear solvers applied to discretized steady differential equations with multiple solutions.

Postprocessed files, visualization files, and auxiliary output files are not included in the first curated release.

## Benchmark case

The selected root-vector files correspond to the natural convection benchmark described in the associated article.

| Field | Value |
|---|---|
| Benchmark problem | Steady natural convection in a two-dimensional square cavity |
| Mathematical formulation | Stream function-vorticity-temperature formulation |
| Numerical strategy | Finite differences and hyperspherical homotopy path-tracking |
| Rayleigh number | \(Ra = 1 \times 10^5\) |
| Mesh descriptor | 19 interior nodes |
| Data type | Raw algebraic root vectors |
| Number of selected files | 17 |

## Repository destination

The selected root-vector files should be placed in the following repository folder:

```text
data/raw/natural_convection/Ra_1e5/mesh_19_interior_nodes/roots/
```

The original file names are preserved to maintain traceability with the computational outputs.

## Selected files

The first curated release includes the following root-vector files:

```text
XRAIZ1.txt
XRAIZ2.txt
XRAIZ3.txt
XRAIZ4.txt
XRAIZ5.txt
XRAIZ6.txt
XRAIZ7.txt
XRAIZ8.txt
XRAIZ9.txt
XRAIZ10.txt
XRAIZ11.txt
XRAIZ12.txt
XRAIZ13.txt
XRAIZ14.txt
XRAIZ15.txt
XRAIZ16.txt
XRAIZ17.txt
```

## Interpretation of the files

Each `XRAIZ*.txt` file contains one numerical root vector of the nonlinear algebraic system obtained after discretizing the steady natural convection model.

The files are organized as nodal data. Each row corresponds to one node of the finite-difference mesh, and the columns are ordered as follows:

```text
x, y, stream-function, vorticity, temperature
```

where:

| Column | Variable | Description |
|---:|---|---|
| 1 | `x` | Dimensionless horizontal coordinate of the node. |
| 2 | `y` | Dimensionless vertical coordinate of the node. |
| 3 | `stream-function` | Dimensionless stream function, usually denoted as \(\psi\). |
| 4 | `vorticity` | Dimensionless vorticity, usually denoted as \(\omega\). |
| 5 | `temperature` | Dimensionless temperature, usually denoted as \(\theta\). |

The files are published as algebraic benchmark data. Therefore, they should not be interpreted automatically as physically admissible flow fields. In the associated article, the natural convection benchmark distinguishes between thermodynamically feasible solutions and non-conventional algebraic roots.

## Files excluded from this release

The first curated release does not include postprocessed, graphical, or auxiliary numerical-output files. In particular, the following file types are excluded:

```text
SOLN*.txt
Resultados*.txt
Resultados*.grd
*.srf
*.png
```

These files may be incorporated in future releases if a processed-data layer or visualization layer is added to the repository.

## Additional datasets reserved for future curation

Additional computational datasets are available but are reserved for subsequent curated releases. Their inclusion will require harmonization of metadata, standardized folder naming, and verification of their relation to the benchmark cases reported in the associated publication.

| Dataset | Curation status |
|---|---|
| `13 Nodos interiores` | Reserved for a subsequent release after harmonization of the associated numerical metadata. |
| `16 Nodos Interiores/Ra=5D5` | Reserved for a subsequent release focused on additional Rayleigh-number cases. |
| `22 Nodos Interiores` | Reserved for subsequent verification of available numerical outputs. |
| `29 Nodos Interiores` | Reserved for subsequent verification and possible inclusion as processed benchmark data. |

## Recommended citation

Users of these root-vector files should cite both the repository and the associated article.

Associated article:

Jiménez-Islas, H., Calderón-Ramírez, M., Martínez-González, G. M., Calderón-Álvarado, M. P., & Oliveros-Muñoz, J. M. (2019). Multiple solutions for steady differential equations via hyperspherical path-tracking of homotopy curves. *Computers and Mathematics with Applications*. https://doi.org/10.1016/j.camwa.2019.10.023

Repository citation:

Oliveros-Muñoz, J. M. (2026). *Hyperspherical path-tracking benchmark datasets*. GitHub repository. DOI to be added after archival release.
