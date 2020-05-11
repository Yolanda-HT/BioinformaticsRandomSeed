**[Back to main page](https://yolanda-ht.github.io/BioinformaticsRandomSeed/)**

# Dimensionality Reduction
*Curse of dimensinality*

## Concept
- Dimensionality reduction is a process of reducing the number of random varialbes under consideration by obtaining a set of principle variables.
- Approaches can be divided into feature selection and feature extraction.

## Common methods of dimensionality reduction
1. Principal component analysis (PCA)
  - Linear dimensionality reduction
  - Extract "principal components" that are uncorrelated with each other to represent the variance in the data
  - Generate ranked list of "principal components" that explain high to low fraction of variance
  - Typically works in Euclidean space (linear), not suitable for data on a non-euclidean space (non-linear) or contain fine structures
2. Kernel PCA
  - Employ kernel trick to PCA to increase capacity of nonlinear mapping
3. Linear Disriminant Analysis (LDA)
4. T-distributed Stochastic Neighboring Embedding (t-SNE)
  - Non-linear dimensionality reduction
  - Model each high-dimensional object by a 2 / 3 dimensional point in way that similar objects are modeled by nearby points and dissimilar objectes are modeled by distant points
  - Based on neighboring map
  - Developed from Stochastic Neighbor Embedding (SNE)
5. Uniform Manifold Approximation and Projection (UMAP)
  - Non-linear dimensionality reduction
  - Based on neighboring map & topological data analysis method

## Benchmarks
- [Scikit-learn Manifold Learning](https://scikit-learn.org/stable/modules/manifold.html)
![Minifold Learning with 1000 points, 10 neighbors](https://scikit-learn.org/stable/_images/sphx_glr_plot_compare_methods_001.png)
- [t-SNE v.s. PCA handwritten digits](https://towardsdatascience.com/visualising-high-dimensional-datasets-using-pca-and-t-sne-in-python-8ef87e7915b)
![PCA v.s. t-SNE](https://miro.medium.com/max/1400/1*izt3rfV_itenuD32DEr1Vw.png)
- [Becht, Etienne, et al. "Dimensionality reduction for visualizing single-cell data using UMAP." Nature biotechnology 37.1 (2019): 38.](https://www.nature.com/articles/nbt.4314)
![t-SNE v.s. UMAP](https://media.springernature.com/lw685/springer-static/image/art%3A10.1038%2Fnbt.4314/MediaObjects/41587_2019_Article_BFnbt4314_Fig1_HTML.jpg?as=webp)


## Reference
1. [Dimensionality reduction algorithms: strengths and weaknesses](https://elitedatascience.com/dimensionality-reduction-algorithms)
2. [Gunasekaran, Mr Ramkumar, and Mr Tamilarasan Kasirajan. "Principal Component Analysis (PCA) for Beginners." (1901).](http://ijasrm.com/wp-content/uploads/2017/09/IJASRM_V2S9_333_44_46.pdf)
3. [Hinton, Geoffrey E., and Sam T. Roweis. "Stochastic neighbor embedding." Advances in neural information processing systems. 2003.](http://papers.nips.cc/paper/2276-stochastic-neighbor-embedding.pdf)
4. [Maaten, Laurens van der, and Geoffrey Hinton. "Visualizing data using t-SNE." Journal of machine learning research 9.Nov (2008): 2579-2605.](http://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf)
5. [McInnes, Leland, John Healy, and James Melville. "Umap: Uniform manifold approximation and projection for dimension reduction." arXiv preprint arXiv:1802.03426 (2018).](https://arxiv.org/abs/1802.03426)
