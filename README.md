# Science-Fair-2018
## Investigating Epigenetic Factors in CTLA-4 and PD-1 Immune Checkpoint Blockade Therapy
## Chinmay Lalgudi, Lynbrook High School
### Purpose:
Immune system is a complex system of cells, cytokines(chemical messengers) and checks & balances.
Step 1: Dendritic Cells (Antigen Presenting Cells) present peptides in MHC molecules to T-cell receptor.
Step 2: DC increase T cell activation by co-stimulatory molecules, or lower T cell responses by co-inhibitory molecules.
Cancer cells escape immune surveillance by presenting inhibitory signals to immune system, specifically in CTLA4(cytotoxic T lymphocyte antigen 4) during priming phase, and in PD-1(Programmed cell Death) in effector phase. In Immune Checkpoint Blockade, immunotherapy with monoclonal Antibodies(mAb) block inhibitory signal and increase T-cell activation. Issue with immunotherapy is only some patients see clinical benefits. Epigenetic drugs such as DNA methyltransferase can change expression of immune-related genes. We need epigenetic biomarkers, based on methylation of immune genes, to assess combined epigenetic therapy with immunotherapy.

### Hypothesis:
Epigenetic factors such as methylation are correlated with specific genes involved in CTLA-4 and PD1 immune checkpoint blockade immunotherapy. Identifying the methylation patterns allows predicting when epigenetic therapy can be used to potentially improve immunotherapy outcomes.

### Procedures, methods:
Use TCGA datasets on Skin Cutaneous Melanoma for the immune-related genes, to generate mRNA expression, methylation, mutual exclusion and coexpression data. Genes are: Cytolytic markers (Granzymes:GZMA, GZMB, Perforin:PRF1, Granulysin:GNLY); HLA molecules (human leukocyte antigen: HLA-A, HLA-B, HLA-C, HLA-E, HLA-F, HLA-G, HLA-H, HLA-DMA, HLADMB, HLA-DOA, HLA-DOB, HLA-DPA1, HLA-DPB1, HLADQA1, HLA-DQA2, HLA-DQB1, HLA-DRA, and HLA-DRB1); Interferon pathway related genes (IFNG, IFNGR1, IFNGR2, IRF1, STAT1, PSMB9, PTPN6); Chemokines (CCR5, CCL3, CCL4, CCL5, CXCL9, CXCL10, and CXCL11); Adhesion molecules (ICAM1, ICAM2, ICAM3, ICAM4, ICAM5, and VCAM1).

### IGEM(Immune Gene Epigenetic Model):
Single Gene methylation mRNA(SGMM): Identify genes, whose methylation affects its mRNA expression.
Pair Gene methylation mRNA(PGMM): identify genes whose methylation affects other genes' mRNA expression.
In SGMM, genes which show significant direct(>0.5) or inverse(<0.5) in Spearman and Pearson correlation are ranked based on correlation. In PGMM, sort/ranking based on how many other genes' mRNA expression is affected by this gene's methylation.

### Results:
IGEM identified the following Epigenetic biomarkers for immune-related genes, which may be used for personalized epigenetic treatment. Details: 478 samples, 42 genes, 187 gene pairs significantly co-expressed.
SGMM: 13 significant genes identified (PTPN6 IRF1 STAT1 PSMB9 ICAM2 ICAM3 HLA-B HLA-C HLA-E HLA-F HLADMA HLA-DMB HLA-DPA1)
PGMM: 10 significant genes (PTPN6 IRF1 PSMB9 ICAM3 PRF1 ICAM2 GZMA HLA-G HLA-C HLA-B)

### Conclusions:
Methylation of PTPN6 or SHP-1 (Chr12) shows significant changes in mRNA expression of multiple genes. SHP-1 is inhibitory to T-regulatory cells. Lowering SHP-1 can improve immunotherapy outcomes. PSMB9 methylation affects significant number of other genes. This melanoma result is consistent with Ovarian Epithelial cancer in previous research.
IRF-1(Interferon Regulatory Factor) is key in development and activation of immune cells. However past studies have not identified methylation of IRF-1.
MHC genes involved in antigen presentation are located in Chromosome 6, which may explain methylation of one gene causing change in mRNA expression of other genes.
Model is implemented in python, which is reusable for other cancer types (e.g. NSCLC, ovarian) and any new genes that show significance in melanoma.
