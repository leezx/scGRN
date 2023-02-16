# scGRN
A tool for gene regulatory network (GRN) construction and visualization

# Basic assumptions
1. TF existence and activity. (we usually use TF expression to estimate this, however, we still need western blot to confirm the protein expression. What's more we need more expriments to confirm the TF-DNA activity as a complex, see that Nature paper.)
2. TF DNA Motif Occurrence in open chromatin region. 
3. Correlation between chromatin open and target gene expression.
4. Co-accessibility peak and co-expression gene modules/topics (this is scGRN)

# Basic logic
Individual data
- single cell or sample with paired RNA-seq and ATAC-seq is enough to build a GRN.

Population data
- However, population cells or samples is powerful to link peak and gene with correlation.
- Also, celltype specific-GRN and modules can be identified.
- Finally, by compared case to control, we can see what GRN is disturbed and what GRN is generated.
- **So, a scGRN is defined by co-accessibility peak and co-expression gene modules/topics with enriched TF (DNA motif)**

# ggplot visulization of scGRN
1. expression of TF (absolute expression)
2. TF DNA motif and opening chromatin peak (proximal 10kb and distal 500kb in maximun, zoom in form chromasome to gene/peak to DNA base)
3. peak and gene correlation (negative and positive) 
4. Volcano plot of a TF target GRN
5. Volcano plot of a gene module, enrich for TF
6. Functional annotation of a novel GRN

# Other fancy plot
1. circle plot for genomoe-wide visualization, target gene distribution
2. add protein-protein interaction in circle plot
3. gene UMAP plot to show different modules


# Tools
- ggcoverage - Visualize and annotate genome coverage with ggplot2
- ggtranscript: an R package for the visualization and interpretation of transcript isoforms using ggplot2
- https://github.com/dzhang32/ggtranscript
- https://github.com/YuLab-SMU/ggmsa
- http://bioconductor.org/packages/release/bioc/html/ggbio.html
- https://github.com/omarwagih/ggseqlogo
- https://github.com/bradyajohnston/plasmapr/
- https://github.com/jhkorhonen/MOODS [MOODS: Motif Occurrence Detection Suite]

TF protein structure
- https://bioconductor.org/packages/devel/bioc/vignettes/drawProteins/inst/doc/drawProteins_BiocStyle.html
- https://cran.r-project.org/web/packages/protti/vignettes/protein_structure_workflow.html

# References
- Recent studies using 3C-based techniques have provided initial maps of distal enhancer–promoter contacts. Active promoters were found, on average, to contact 4–5 enhancer-like elements. The majority of these elements are located within 500 kb from the interacting promoter, with an estimated median distance of ~125 kb [17,18]. Interestingly, active enhancers were found to contact approximately two promoters on average, suggesting that enhancers might commonly regulate multiple genes. Moreover, only a fraction of looping distal elements contact the nearest promoter (reported as 27% in [18] and 60% in [19]), whereas the others skip one or more genes. These data indicate that it is often incorrect to assume that an enhancer interacts only with its nearest promoter. [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4252644]
- The genes range in size from 994 to 41.8 kb for mouse (average length = 7902 bp, S.D. = 6391) and from 1148 to 37.7 kb for human (average length = 8446 bp,S.D. = 7124). The number of exons range from 1 to 41 per/gene (average = 8.4, S.D. = 6.9). [https://genome.cshlp.org/content/9/9/815.full]
