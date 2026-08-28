---
title: "Basics on Bioinformatics and Systems Biology: Lecture 6"
collection: teaching
type: "Lecture"
permalink: /teaching/bbsb_lecture_6
venue: "VU"
date: 2026-01-10
location: "Amsterdam, the Netherlands"
---

Here you will find the basic concepts for the Lecture 1 and link to the additional/support material

# Functional enrichment

## Gene sets

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_6.jpg" width="25000">  | Cellular functions can be represented as gene sets. **A gene set** is a list of genes that share a common biological function, pathway, or localization.||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_11.jpg" width="25000">  | Gene sets are defined based on **ontology**: a collection of terms, with their definitions and relationship.||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_12.jpg" width="25000"> | The Gene Ontology (GO) is a major bioinformatics initiative that provides standardized framework to describe the functions of genes and gene products. <ul>GO privides three main ontologies:<li>Cellular compnent - a cellular localization of a gene/gene product</li><li>Molecular function - the gene or gene product activity</li><li>Biological process - a gene function</li></ul>|[Gene Ontology](https://geneontology.org/)|

## Enrichment analysis

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_19.jpg" width="25000">  | <ul>Main steps of enrichment analysis: <li>Define the list of genes your are interested to analyze (e.g., differentially expressed genes between case in control from RNA-Seq experiment)</li><li>Choose the source of the gene sets (e.g., Gene Ontology Biological processes)</li><li>Choose the enrichment test. Different anrichment analysis computational tools use different tests and approaches. **Enrichment test** determines the gene sets significantly over- or under-represented among the genes that you are interested to analyze. The description of gene sets (e.g., gene functions, localizations, etc) points towards the cellular functions associated with the condition or phenotype of interest.</li></ul><ul>Main representatives of enrichment analysis approaches: <li>**Overrepresentation analysis (ORA)** </li><li> **Gene set enrichment analysis (GSEA)** </li></ul>||

## Overrepresentatopn analysis (ORA)

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_22.jpg" width="25000">  | <ul>Steps of the ORA (based on the differential gene expression analysis results as an example): <li>Define the groups of samples and perform the differential gene expression analysis</li><li>Rank genes that are significantly differentially expressed between chosen conditions by the differential statistic (e.g., LogFoldChange (LFC))</li><li>Choose the threshold to defind the list of genes to analyze with ORA. Usual thresholds for differential expression analysis e.g., LFC > +1 (**Upregulated**); LFC < -1 (**Downregulated**), abs(LFC) > 1.</li></ul>||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_27.jpg" width="25000">  | <ul>Steps of the ORA (based on the differential gene expression analysis results as an example, continuation): <li>Choose the sourse of the gene sets (e.g., GO Biological processes)</li><li>For each gene set, calculate how many genes to analyze overlap with a gene set</li><li>Perform a statistical **association test** to determine if this overlap is significant. In other words, if this overlap is higher than it will be expected by chance.</li><li>To perform an association test, also calculate the following numbers: how many genes that is not from the list to analyze (**background**) overalp with a gene set, how many genes to analyze do not overlap with a gene set, and how many background genes do not overlap with a gene set.</li><li>After performing the association tests per gene set, correct the resulted p-values using any multiple test correction approaches</li></ul>||

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_30.jpg" width="25000">  | Most common association tests on bioinformatics: **Chi-squared test** (is used for bigger datasets) and **Fisher's exact test** (is used for smaller datasets). One-sided Fisher's exact test is called hypergeometric test. ORA analysis tools use one of these tests|[Fisher's exact test](https://www.pathwaycommons.org/guide/primers/statistics/fishers_exact_test/)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_36.jpg" width="25000">  | **Chi-squared test** tests if the difference between the values that are **expected** to be distributed across the groups in a situation that all the features occur independently from each other (or not accociated with each other) differs significantly from the **observed** values. **Observed** values are obtained from the experiment. The table with the values are called **contingency table**. This contingency table has a degree of freedom 1. The formula for a degree of freedom: (number of rows - 1)*(number of columns - 1). For the table of 2 by 2: (2 - 1) * (2 - 1) = 1. <ul>**Expected** values will be calculated as following (example Event 1 - gene is upregulated (UP) and belongs to a gene set (GS)):<li>The probability to be upregulated is the number of upregulated genes (21 + 27) divided to the whole amount of samples (21 + 27 + 0 + 18 = 66)</li><li>The probability to be in a gene set is the number of genes in a gene set (21 + 0) divided to the whole amount of samples (21 + 27 + 0 + 18 = 66)</li><li>If these two features - to be upregulated and to belong to a gene set - are independent, then the probability of being both upregulated and in the gene set for independent events is the multiplication of both probabilities: 48/66 * 21/66</li><li>To calculate the amount of genes, we need to multiply this probability on the amount of samples: 48/66 * 21/66 * 66, which will be about 15.26</li><li>The same procedure is repeated for all pairs of features - to be upregulated and not in a gene set, not to be upregulated and to be in a gene set, and not to be unpregulated and not to be in a gene set. The results is a contingency table of expected values.</li></ul>||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_41.jpg" width="25000">  | <ul>The next steps of Chi-squared test:<li>Calculate the statistic score - chi-squared - using the formula</li><li>Check a p-value for a resulted value based on the distribution of chi-squared values (chi-squared distribution), what is the probability to observe the same or more extreme value. P-values for each chi-squared value is pre-calculated and can be obtained from the corresponding tables or online calculators. For the chi-squared value calculated in the example, a p-value is 0.00068 for degree of freedom of 1.</li> <li>Interpretation: With a significance threshold of 0.05, the null hypothesis that there is no association between a gene set and upregulated genes, can be rejected.</li></ul> |[Chi-squared distribution](https://www.scribbr.com/statistics/chi-square-distributions/) [Chi-squared test calculator](https://stattrek.com/online-calculator/chi-square)|


## Gene set enrichment analysis (GSEA)

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_44.jpg" width="25000">  | The limitation of ORA: ORA-based methods require an arbitrary threshold to define the list of genes to analyze. However: there is no natural level for a threshold, different thresholds lead to different results, thresholding also leads to the information loss because it treats all significant results similarly despite their stremgth and neglects weak signals. Whole-distribution methods have been shown to be more stable and statistically powerful. They have to be used whenever is possible. **Gene set enrichment analysis (GSEA)** is an example of the whole distribution methods for enrichment analysis.||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_45.jpg" width="25000">  |The idea of GSEA approach: Given genes in a gene set list (s) and a ranked list of genes to analyze, the question is whether S is distributed randomly (as the examplary gene set B) or tends towards upper or lower part of the ranked list (as the examplary gene set A). For differentially expression analysis, ranking can be done by LFC or by adjusted p-values|[GSEA paper](https://www.pnas.org/doi/10.1073/pnas.0506580102)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_47.jpg" width="25000">  |<ul>GSEA method calculates ES score as following. <li>Starting from the first gene in the ramked gene list, calculate the fraction of genes that belong to S (“hits”) present up to this first position in L weighted by their rank (Phit).</li> <li>Calculate the same for misses: the fraction of genes that are not in S (“misses”) that are present up to this first given position in L (Pmiss).</li> <li>Calculated the difference between Phit and Pmiss.</li><li>Repeat for the second position, the third, and so on till the end of the ranked list of genes.<li></ul>|[GSEA paper](https://www.pnas.org/doi/10.1073/pnas.0506580102)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_51.jpg" width="25000">  |The result will be the distribution of the differences across all genes in the ranked list. ES score is the largest observed difference between Phit and Pmiss. The question is whether this ES score high enough||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_51.jpg" width="25000">  |A statistical thinking approach: to compare the observed ES score with the background distribution - the distribution of ES score that could be obtained by chance. The problem: the distribution of ES scores is unknown. The approach: to estimate the background ES score distirbution by randomizing the data for each gene set. In other words, which ES score could be obtained if the S is randomly distributed in the L. <li>First, S is randomly shuffled many times among L (the more, the more accurate estimates will be obtained).</li><li> The resulting ES scores present the distribution of ES scores that can be obtained by chance.</li><li> The observed ES score is compared with this distribution, and the probability (p-value) of observing the same ES score or more extreme is calculated for this distribution. This p-value obtained from an estimated distribution is called **empirical p-value**</li>||





