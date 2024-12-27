# Reprogramming-Cell-Fate

This repository contains analyses and data from the research project titled "Reprogramming Cell Fate", conducted under the supervision of Dr. Antonio Scialdone. The primary aim is to investigate whether regional boundaries of blastula cells change after endoderm nuclei transfer (NT), specifically focusing on the animal cap of Xenopus laevis blastula cells.



## Background

This study builds on insights from two foundational papers published by our lab:
1. **Characterisation of the transcriptional dynamics underpinning the function, fate, and migration of the mouse Anterior Visceral Endoderm.**  
   Shifaan Thowfeequ, Jonathan Fiorentino, Di Hu, Maria Solovey, Sharon Ruane, Maria Whitehead, Bart Vanhaesebroeck, Antonio Scialdone, Shankar Srinivas  
   DOI: [https://doi.org/10.1101/2021.06.25.449902](https://doi.org/10.1101/2021.06.25.449902)
2. **CIARA: a cluster-independent algorithm for the identification of markers of rare cell types from single-cell RNA seq data.**  
   Gabriele Lubatti, Marco Stock, Ane Iturbide, Mayra L. Ruiz Tejada Segura, Richard Tyser, Fabian J. Theis, Shankar Srinivas, Maria-Elena Torres-Padilla, Antonio Scialdone  
   DOI: [https://doi.org/10.1101/2022.08.01.501965](https://doi.org/10.1101/2022.08.01.501965)

Key insights include:
- Embryo cells exhibit gene expression dynamics along the diffusion pseudotime, reflecting developmental progression along the spatial axis.
- NT-induced changes in blastula cells prompt questions about boundary shifts between ectoderm, mesoderm, and endoderm regions.

### Experiment
The experiments and RNA-seq analysis were conducted using *Xenopus laevis* blastula cells:
- **IVF and NT groups**: Cells were isolated from the animal cap.
- **Goal**: Determine how NT affects ectoderm boundaries and regional gene expression.
- **Key finding**: NT introduces mixed expression of ectoderm and endoderm markers, suggesting potential shifts in cellular boundaries.

### Collaborators
- **Wet-lab work**: Gaurav Agarwal and Chris Penfold (University of Cambridge).
- **Computational work**: Marco Stock, Jonathan Fiorentino, and Ding-Yang Wang (current study).

---

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

## Experimental Details

### Key Objectives
- **Question**: Do regional boundaries of blastula cells change after endoderm nuclei transfer?
- **Data**: scRNA-seq of animal cap cells (ectoderm region).
- **Approach**:
  - Integration of IVF and NT datasets.
  - Identification of HVGs and highly localized genes.
  - Robust pseudotime mapping using DPT.

### Results and Conclusions
1. **Cluster-Specific Insights**:
   - **Cluster 9**: Exhibited potential mesodermal and endodermal interactions.
   - **Cluster 3 (CIARA)**: Identified as a rare cell marker region overlapping Cluster 9.
2. **Gene Trajectories**:
   - **foxi1.L**: High expression towards ectodermal recovery.
   - **wnt11b.L**: Initially suppressed but resurges during mesodermal specification.
3. **Boundary Dynamics**:
   - NT induces fixed boundaries, later reverting to normal developmental patterns.
 
### Summary
- **Key findings**: NT alters gene expression within the animal cap, introducing mixed markers of ectoderm and endoderm. Over pseudotime, NT-induced changes are initially evident but tend to diminish as normal boundaries are restored during development.
- **Significant genes**: *Vegt.S*, *Wnt11b.L*, *Foxi1.L*, and *Foxi1.S* were pivotal in highlighting shifts in boundaries and developmental changes.

---

## Contact

**Dr. Antonio Scialdone**  
Computational Biology Laboratory, Helmholtz Zentrum München  
Email: [Antonio.Scialdone@helmholtz-munich.de](mailto:Antonio.Scialdone@helmholtz-munich.de)  

For technical queries related to the analysis, please contact:  
**Ding-Yang Wang**  
Email: [deweywang2000@gmail.com](mailto:deweywang2000@gmail.com)
