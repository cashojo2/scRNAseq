# scRNAseq Trajectory Analysis

This repository demonstrates the use of Scanpy and scVelo to perform trajectory analysis on single-cell gene expression data from 10x Genomics, specifically focusing on neutrophils. The dataset comprises 8,000 cells, over 36,000 genes, and more than 187 million UMIs/ total reads.

The analysis begins with FASTQ files uploaded from the 10x platform, where RNA reads were assessed for quality control. We enforced the inclusion of 8,000 barcodes due to the low UMI counts per barcode associated with neutrophils. Additionally, introns were mapped to account for the high intron retention rate in neutrophils. Data correction involved applying a minimum mean threshold of 7.5 features to eliminate low gene expression background and capping mitochondrial reads at 15% to remove dying cells. This approach removed 98% of background barcodes not included in the original clusters and 38% of the originally classified neutrophils.

The Loupe Browser was utilized to cluster cell populations and isolate neutrophils. In this Jupyter Notebook, the Scanpy and scVelo packages were employed to conduct trajectory analysis of the data. Visualizations created include:

UMAP embeddings of neutrophil velocities
UMAP plots with latent time
Heatmaps of differentially expressed genes
Violin plots of clusters differentially expressed during neutrophil maturation

credit to 10x Genomics
