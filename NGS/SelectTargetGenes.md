**[Back to main page](https://yolanda-ht.github.io/BioinformaticsRandomSeed/)**

# Approaches for Selecting Target Genes
> Last update: 10/29/2020 <br>
> By: Huitian (Yolanda) Diao

#### 1. Without using reference (limited to RNA-seq dataset in question):
  - Select genes based on p-val / log2fc / expression value
  - Select genes based on PCA principal component contribution (on the PC that is most meaningful biologically), this can also be referred to as feature extraction
  - Classify genes to reduce the amount of variable to consider (e.g. k-means clustering based on pattern of gene expression in samples)
  - Regression methods to select the gene that is the best predictor for differences between conditions you want to consider
#### 2. With public data as reference
  - Use GSEA to extract genes in the signature set that you are interested in
  - Use GO term to extract genes in the term that you are interested in
  - Use other published dataset (perform differential / other kind of analysis) to select intersection of genes that contribute to phenotype you are interested in (see also meta analysis)
#### 3. For specific experimental procedure
  - For flow cytometry follow up: select only surface markers
  - For general protein related experiment: use expressed protein list to filter (some of the genes that are expressed are not well translated)
  - Etc..
#### 4. Meta analysis with other dataset
  - For transcription & DNA binding related research: use ChIP-seq to to identify potential transcription factor controlled genes. This can also be achieved in some level with ATAC-seq & motif scanning
  - For protein intereaction research: use protein interaction database to further classify your target genes into functional clusters
