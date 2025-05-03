# Gene Selection and Network Analysis

I have merged two datasets *GSE18842* and *GSE19804* to make the results more reliable.

To find important genes, I used a step-by-step approach:

**Variance Filtering:** First, I kept only genes with high variability (variance > 0.04) since they are more likely to be biologically relevant. There are 43 genes.
<img src="images\GSE18842 and GSE19804__Variance_Line_Diagram.png" alt="Variance_Line_Diagram.png" width=100%>

**Simulated Annealing:** Next, I used an optimization method to select the best 40 genes.
<img src="images\GSE18842 and GSE19804__Simulated Annealing.png" alt="Simulated Annealing.png" width=100%>

**Volcano Plot:** Then, I looked for genes with significant changes in expression (-log10 p-value > 10 and |logFC| > 1). There are 130 genes.
<img src="images\GSE18842 and GSE19804__Volcano_Plot_Final.png" alt="Volcano_Plot_Final.png" width=100%>

**Final Gene List:** Combining all three steps gave me 11 key genes:
**['MMP12', 'WIF1', 'AGER', 'GREM1', 'GJB2', 'CPB2', 'TMEM100', 'MT1M', 'MMP1', 'GKN2', 'CLDN18']**
<img src="images\GSE18842 and GSE19804__Venn of SA Var and Vol.png" alt="Venn of SA Var and Vol.png" width=100%>

Finally I create the Correlation Gene Regulatory Network for Healthy and Disease state:

<div>
<img src="images\GSE18842 and GSE19804__GRN Healthy.png" alt="GRN Healthy" width=100%>

<img src="images\GSE18842 and GSE19804__GRN Disease.png" alt="GRN Disease" width=100%>
</div>
