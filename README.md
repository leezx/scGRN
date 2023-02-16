# scGRN
A tool for gene regulatory network (GRN) construction

# Basic assumptions
1. TF existence and activity. (we usually use TF expression to estimate this, however, we still need western blot to confirm the protein expression. What's more we need more expriments to confirm the TF-DNA activity as a complex, see that Nature paper.)
2. TF DNA motif occurence in open chromatin region. 
3. Correlation between chromatin open and target gene expression.
4. Co-accessibility peak and co-expression gene modules/topics

# ggplot visulization of scGRN
1. expression of TF (absolute expression)
2. TF DNA motif and opening chromatin peak
3. peak and gene correlation (negative and positive)
4. Volcano plot of a TF target GRN
5. Volcano plot of a gene module, enrich for TF
6. Functional annotation of a novel GRN

# other fancy plot
1. circle plot for genomoe-wide visualization, target gene distribution
2. 
