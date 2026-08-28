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
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_22.jpg" width="25000">  | <ul>Steps of the ORA (based on the differential gene expression analysis results as an example): <li>Define the groups of samples and perform the differential gene expression analysis</li><li>Rank genes that are significantly differentially expressed between chosen conditions by the differential statistic (e.g., LogFoldChange (LFC))</li><li>Choose the threshold to defind the list of genes to analyze with ORA. Usual thresholds for differential expression analysis e.g., LFC > +1 (**Upregulated**); LFC < -1 (**Downregulated**), |LFC| > 1.</li></ul>||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-6_27.jpg" width="25000">  | <ul>Steps of the ORA (based on the differential gene expression analysis results as an example, continuation): <li>Choose the sourse of the gene sets (e.g., GO Biological processes)</li><li>For each gene set, calculate how many genes from the list of interest overlap with a gene set</li><li>Perform a statistical **association test** to determine if this overlap is significant. In other words, if this overlap is higher than it will be expected by chance.</li><li>To perform an association test, also calculate the following numbers: how many genes that is not from the list of interest (**background**) overalp with a gene set, how many genes from the list of interest do not overlap with a gene set, and how many background genes do not overlap with a gene set.</li><li>After performing the association tests per gene set, correct the resulted p-values using any multiple test correction approaches</li></ul>||

## Gene set enrichment analysis (GSEA)

| Slide | Text | Additional material|
|----------------|-------------|-------------|
