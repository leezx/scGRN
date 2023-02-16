# scGRN
A tool for gene regulatory network (GRN) construction and visualization

# Basic assumptions
1. TF existence and activity. (we usually use TF expression to estimate this, however, we still need western blot to confirm the protein expression. What's more we need more expriments to confirm the TF-DNA activity as a complex, see that Nature paper.)
2. TF DNA motif occurence in open chromatin region. 
3. Correlation between chromatin open and target gene expression.
4. Co-accessibility peak and co-expression gene modules/topics (this is scGRN)

# logic
Individual data
- single cell or sample with paired RNA-seq and ATAC-seq is enough to build a GRN.
Population data
- However, population cells or samples is powerful to link peak and gene with correlation.
- Also, celltype specific-GRN and modules can be identified.
- Finally, by compared case to control, we can see what GRN is disturbed and what GRN is generated.
- So, a scGRN is defined by co-accessibility peak and co-expression gene modules/topics

# ggplot visulization of scGRN
1. expression of TF (absolute expression)
2. TF DNA motif and opening chromatin peak (proximal and distal, zoom in form chromasome to gene/peak to DNA base)
3. peak and gene correlation (negative and positive) 
4. Volcano plot of a TF target GRN
5. Volcano plot of a gene module, enrich for TF
6. Functional annotation of a novel GRN

# other fancy plot
1. circle plot for genomoe-wide visualization, target gene distribution
2. add protein-protein interaction in circle plot


# reference
- ggcoverage - Visualize and annotate genome coverage with ggplot2
- ggtranscript: an R package for the visualization and interpretation of transcript isoforms using ggplot2
- https://github.com/dzhang32/ggtranscript
- https://github.com/YuLab-SMU/ggmsa
- http://bioconductor.org/packages/release/bioc/html/ggbio.html
- https://github.com/omarwagih/ggseqlogo
- https://github.com/bradyajohnston/plasmapr/

TF protein structure
- https://bioconductor.org/packages/devel/bioc/vignettes/drawProteins/inst/doc/drawProteins_BiocStyle.html
- https://cran.r-project.org/web/packages/protti/vignettes/protein_structure_workflow.html


