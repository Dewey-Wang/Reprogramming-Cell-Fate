# Script

## Repository Structure

### Notebooks Overview
This repository contains six Jupyter notebooks, each addressing a critical step in the analysis pipeline:

1. **integration and clustering.ipynb**
   - Data integration across experiments and clustering analysis.
   - Includes robustness analysis for determining optimal resolution and neighbors (`k`) parameters for clustering.

2. **identify interest cluster.ipynb**
   - Identification of key clusters using UMAP and PCA projections.
   - Integration with **CIARA** to pinpoint the cluster of rare cell type markers.
   - Find the highly variable genes (HVGs) and highly localized genes (HLGs) within the CIARA clustering result.

3. **Map DPT.ipynb**
   - Calculation of diffusion pseudotime (DPT) using `Seurat` and `destiny`.
   - Focuses on global trajectories and developmental topology.

4. **Select genes for expression vs DPT.ipynb**
   - Selection of HVGs and their expression trends across pseudotime.
   - Employs `SCTransform` for normalization and noise reduction.

5. **plot the expression vs dpt.ipynb**
   - Visualizations of gene expression trajectories across pseudotime.

6. **GO analysis.ipynb**
   - Functional enrichment analysis of identified gene clusters.

---

## Contact

For technical queries related to the analysis, please contact:  
**Ding-Yang Wang**  
Email: [deweywang2000@gmail.com](mailto:deweywang2000@gmail.com)
