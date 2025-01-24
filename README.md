# Spatial-transcriptomics-analysis-

This repository contains code for analyzing spatial transcriptomics data from NanoString's CosMx platform, focusing on lung tissue samples.

## Analysis Pipeline

1. **Data Loading and QC**
- Import raw data from Lung5_Rep1 dataset
- Calculate QC metrics using negative probe controls (NegPrb)
- Filter cells (min_counts=100) and genes (min_cells=500)

2. **Data Processing**
- Normalize counts per cell
- Log transformation
- PCA dimensionality reduction
- UMAP embedding
- Leiden clustering (resolution=0.3)

3. **Visualization**
- UMAP plots showing cell clusters
- Expression maps for key markers:
  - Epithelial: KRT17, EPCAM, DCN
  - Immune: CD45, CD52, CD79A
  - Other: PECAM1, RGS5, ACTA2
- Pan-cytokeratin (PanCK) spatial distribution
- Cell segmentation overlays

## Key Findings

- Identified 8 cell populations with distinct molecular signatures and spatial organization
- Quality control shows 0.22% unassigned transcripts in negative probe analysis
- Mean transcript count ~500-1000 per cell with high cell-to-cell variation
- Strong spatial segregation between epithelial (EPCAM+) and stromal (DCN+) regions
- Immune populations (CD45+, CD52+, CD79A+) show localized clustering patterns
- Vascular markers (PECAM1, RGS5, ACTA2) highlight distinct vessel architecture
