# TCGA Breast Cancer Gene Expression Analysis

## Overview
This project looks at RNA-seq gene expression data from TCGA breast cancer samples to see how tumor and normal tissue differ at the transcript level. I created and used a Python script to run differential expression analysis and then visualized the results with PCA and clustering to get a better sense of the overall structure in the data.

---
## Objectives
- Identify genes that are differentially expressed between tumor and normal samples  
- Visualize overall gene expression patterns using PCA  
- Explore how genes and samples cluster using a heatmap
  
---
## Methods
- Performed differential expression analysis using t-tests  
- Applied multiple testing correction using FDR (Benjamini–Hochberg)  
- Used PCA for dimensionality reduction  
- Generated a clustered heatmap to visualize gene expression patterns
  
---
## Results
### Differential Expression
The volcano plot shows a clear set of genes that are significantly up- or downregulated in tumor samples. Even with a simple statistical approach, there’s a noticeable shift in expression for certain genes, suggesting real biological differences between conditions.
### PCA
PCA shows partial separation between tumor and normal samples. It’s not perfectly clean which is expected with biological data, but there is a trend of the structure—tumor samples tending to group together with each other more than with the normal samples.
### Heatmap
The heatmap of the top differentially expressed genes shows clear clustering. Samples tend to group by condition, and genes with similar expression patterns cluster together, which points to coordinated regulation.

--
## Figures
### Volcano Plot
![Volcano Plot](figures/volcano.png)
### PCA Plot
![PCA Plot](figures/pca.png)
### Heatmap
![Heatmap](figures/heatmap.png)

---
## Technologies Used
- Python  
- pandas, numpy  
- matplotlib, seaborn  
- scikit-learn  
- statsmodels  
---
## Data Source
The gene expression data used in this project was obtained from the UCSC Xena Browser, using the TCGA Breast Invasive Carcinoma (BRCA) cohort. This dataset contains RNA-seq–based gene expression measurements across a large number of breast tumor samples, along with a smaller set of normal tissue samples for comparison. The values represent normalized gene-level expression (RSEM, log2-transformed), making them suitable for downstream analysis such as differential expression and clustering.

The dataset used in this project is publicly available through the UCSC Xena Browser (TCGA BRCA cohort). Due to file size, the raw data is not included in this repository.
To reproduce the analysis, download the gene expression dataset from UCSC Xena and place it in the project directory before running the notebook.

---
## Key Takeaways
- A relatively small subset of genes accounts for most of the observed differences between tumor and normal tissue  
- Tumor samples exhibit more consistent expression patterns compared to normal samples, which may reflect shared oncogenic processes  
- Unsupervised methods (PCA and hierarchical clustering) independently capture separation between biological conditions  
- Gene clustering patterns suggest coordinated regulation, potentially reflecting underlying biological pathways involved in cancer progression
  
---
## Notes
This project uses a simplified differential expression approach (t-tests) rather than specialized RNA-seq tools. The goal was to build an intuitive and reproducible pipeline in Python while still capturing meaningful biological patterns.
