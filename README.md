# PAAD_Analysis

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/vaniisgh/PAAD_Analysis/e77110445e8662043199fc72e6c12e4d88fa4230)

This repository contains a small analysis on a RNA seq dataset. The aim of this exploratory analysis was to develop an understanding of gene expression datasets and and the relation of the same with Pancreatic Adenocarcinoma (PAAD). To preview this work use the binder link or toggle to the Analysis ipython notebook in the repository. To view this on your own jupyter environment :

```
git clone https://github.com/vaniisgh/PAAD_Analysis PAAD_Analysis
cd PAAD_Analysis
jupyter notebook
```
and open the Analysis notebook
_note_: the requirements file will be updated shortly.

## Data files

All data files generated during the analysis or for the analysis can be found in the ```\data``` folder. 
This includes the main GCT file i.e. a Gene Cluster Text file format. The GCT file format is a tab-delimited text-based format, pairing matrix expression values with row and column metadata, allowing comparison of both transcriptional and contextual differences across samples. To parse the GCT file I use the python package [cmapPy]. This ensures the row and column metadata as well as data matrix is parsed and stored correctly.
This allows us to have a the data matrix, matrix with row metadata, column metadata as well as multi indexed matrix which allows for a different way to select data.

## Pancreatic Adenocarcinoma (PAAD) 

Pancreatic Adenocarcinoma is the most common type of pancreatic cancer.These adenocarcinomas (when the neoplasm is of the epithelial tissue of glandular origin) start within the part of the pancreas which makes digestive enzymes.  
Inferons are a group of signalling proteins used by the cell to signal the immune system in presence of pathogenic presence say that of virus, bacteria, parasites as well as in the presence of tumour cells. This probably triggers the immune system to take note of these "imposters" among the hosts own cells and interact with their specific receptors to activate signal transducer and activator of transcription (STAT) complexes to regulate the expression of immune system genes. More specifically they can be 
  
  - Administration of Type I IFN has been shown experimentally to inhibit tumour growth in animals
  - Interferon action—destroys RNA within the cells to further reduce protein synthesis of both viral and host genes. Inhibited protein synthesis impairs both virus replication and infected host cells.
  - Interferons can also suppress angiogenesis by down regulation of angiogenic stimuli deriving from tumour cells. They also suppress the proliferation of endothelial cells. Such suppression causes a decrease in tumour angiogenesis, a decrease in its vascularization and subsequent growth inhibition. Interferons, such as interferon gamma, directly activate other immune cells, such as macrophages and natural killer cells.
  
Hence you will notice a file ```\data\type1_IFN.txt```, this contains a list of genes related to these type 1 inferons. Hence we try to study their expression in Pancreatic Adenocarcinoma samples.

### Gene Set Variation Analysis

Gene Set Variation Analysis (GSVA) is a non-parametric, unsupervised method for estimating variation of gene set enrichment through the samples of a expression data set. GSVA performs a change in coordinate systems, transforming the data from a gene by sample matrix to a gene-set by sample matrix, thereby allowing the evaluation of pathway enrichment for each sample. This new matrix of GSVA enrichment scores facilitates applying standard analytical methods like functional enrichment, survival analysis, clustering, CNV-pathway analysis or cross-tissue pathway analysis, in a pathway-centric manner. 



[cmapPy]: https://github.com/cmap/cmapPy
