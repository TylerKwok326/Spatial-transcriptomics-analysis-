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

- Successfully identified 8 distinct cell populations
- Spatial organization reveals tissue architecture
- ~21.8% unassigned transcripts in negative probe analysis
- Clear separation of epithelial and stromal regions based on PanCK staining
- Distinct CD45+ immune cell infiltrates

