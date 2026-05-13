# Hyperspherical path-tracking benchmark

This repository contains benchmark datasets associated with the article:

Jiménez-Islas, H., Calderón-Ramírez, M., Martínez-González, G. M., Calderón-Álvarado, M. P., & Oliveros-Muñoz, J. M. (2019). Multiple solutions for steady differential equations via hyperspherical path-tracking of homotopy curves. *Computers and Mathematics with Applications*. https://doi.org/10.1016/j.camwa.2019.10.023

## Purpose

The purpose of this repository is to provide reusable numerical benchmark data for testing, validating, and comparing nonlinear algebraic solvers, homotopy continuation methods, and numerical methods for steady differential equations with multiple solutions.

## Scope of the first curated release

The first curated release of this repository includes raw algebraic root-vector files associated with the natural convection benchmark reported in the associated publication.

The selected dataset corresponds to:

```text
Ra = 1 x 10^5
19 interior nodes
```

The root-vector files are documented in:

```text
docs/roots_index.md
```

## Data structure

The selected files are stored as nodal data. Each row corresponds to one node of the finite-difference mesh, and the columns are ordered as follows:

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

## Repository organization

The selected root-vector files are stored in:

```text
data/raw/natural_convection/Ra_1e5/mesh_19_interior_nodes/roots/
```

The documentation files are stored in:

```text
docs/
```

## Interpretation note

The files are published as algebraic benchmark data. They should not be interpreted automatically as physically admissible flow fields. In the associated article, the natural convection benchmark distinguishes between thermodynamically feasible solutions and non-conventional algebraic roots.

## Suggested citation

If you use these data, please cite both the associated article and this repository.

Associated article:

Jiménez-Islas, H., Calderón-Ramírez, M., Martínez-González, G. M., Calderón-Álvarado, M. P., & Oliveros-Muñoz, J. M. (2019). *Multiple solutions for steady differential equations via hyperspherical path-tracking of homotopy curves*. Computers and Mathematics with Applications. https://doi.org/10.1016/j.camwa.2019.10.023

Repository citation:

Oliveros-Muñoz, J. M. (2026). *Hyperspherical path-tracking benchmark datasets*. GitHub repository. DOI to be added after archival release.

## License

The data are released under the Creative Commons Attribution 4.0 International License.
