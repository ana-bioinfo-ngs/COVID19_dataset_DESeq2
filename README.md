# COVID19_dataset_DESeq2

DATASET - [GSE150392](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE150392)

This study explores the effect of COVID19 on human induced pluripotent stem cell-derived cardiomyocytes (hiPSC-CMs). The raw count files were derived from Galaxy EU platform where the raw samples were passed through steps like FastQC, trimmomatic, RNASTAR and HTSeq.

Objectives:
1. To analyze RNA-seq count data of SARS-CoV-2 Infected and control hiPSC-CMs samples.
2. To perform DESeq2 and identify significantly upregulated and downregulated genes
3. To visualize expression patterns of the DE genes using volcano plots

Workflow:
1. Load the count files and create a combined raw count matrix file.
2. Clean the data and combine this with metadata file.
3. Perform DESeq2
4. Annotate the deseq result by mapping the gene ids to their respective human gene symbols.
5. Remove the low expression genes
6. Generate a volcano plot
7. Seperate the upregulated and downregulated genes from the DE gene data by setting cutoff for logfc and padj values.

Python code for all the steps is [HERE](https://github.com/ana-bioinfo-ngs/COVID19_dataset_DESeq2/blob/main/COVID19_DESeq2_%26_Volcano_Plot.ipynb)

Further steps involve, finding COVID19 associated host genes from various gene databases and intersecting them with our upregulated and downregulated gene list to identify key genes associated with COVID19 in our samples. Functional enrichment analysis will reveal further information on biological processes and pathways associated with these genes.
