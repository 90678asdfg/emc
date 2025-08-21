TOPIC OF THE ASSIGNMENT : write a program to determine the co-cells in a N cluster cell geometry 

## Overview

- The file defines a class `CellularGeometryCluster` for analyzing **cellular network geometry** using hexagonal grid models – common in studying mobile/cellular networks.
- Key features include:
  - Calculation and visualization of **co-channel cells** (cells sharing the same frequency).
  - Calculation of **reuse distance** and **reuse ratio** for particular cluster parameters.
  - Visualization of cell clusters and co-channel patterns using `matplotlib`.

## How It Works

### Parameters
- The two primary parameters for a cluster:
  - **i, j**: integers defining cluster (and thus frequency reuse) patterns.
  - The cluster size  N  is calculated as:  N = i^2 + j^2 + i. j.

### Main Methods
- `find_co_channel_cells()`: Locates the positions of the co-channel cells relative to a reference cell.
- `calculate_reuse_distance()`: Computes geometric distance from center to co-channel cell, "reuse ratio" (distance divided by cell radius), and the theoretical reuse ratio ($$ Q = \sqrt{3N} $$).
- `plot_cluster_diagram()`: Plots the hexagonal cellular grid, highlights center and co-channel cells, displays lines connecting them, and annotates distances.

### Example Usage
A typical workflow:
```python
cluster = CellularGeometryCluster(i=2, j=1)
cluster.plot_cluster_diagram()
plt.show()
```
This creates a cluster with  i=2, j=1 , plots it, and displays information such as:
- Cluster parameters,
- Number and positions of co-channel cells,
- Reuse distance and ratio.

## Visualization

The notebook generates a diagram:
- **Red hexagon:** Center cell.
- **Colored hexagons:** Co-channel cells (each with a different color).
- **Dashed lines:** Connections from center to co-channel cells, annotated with the calculated reuse distance.
- **Text block:** Key parameters and calculated values.

This plot helps **visualize frequency reuse and cluster geometry**, useful for cellular planning and radio resource management.

## Customization

- You can change `i` and `j` for different cluster sizes or reuse patterns.
- Grid size and visualization options are customizable.

***




