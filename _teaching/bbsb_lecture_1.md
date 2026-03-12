---
title: "Basics on Bioinformatics and Systems Biology: Lecture 1"
collection: teaching
type: "Lecture"
permalink: /teaching/bbsb_lecture_1
venue: "VU"
date: 2026-01-10
location: "Amsterdam, the Netherlands"
---

Here you will find the basic concepts for the Lecture 1: Introduction and link to the additional/support material

# Molecular Biology

## Central dogma of molecular biology

| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Central_dogma.png" width="25000">  | Central dogma of molecular biology describes the information flow from DNA via RNA to proteins. First, it was stated by Francis Crick in 1957 and publishd in 1958. Briefly, DNA contains all the information about the cell. Which genes will be used (expressed), which proteins, etc. The information is passed to RNA. And finally, to proteins, the functional units of the cell. The slide illustrates the extended version of Central dogma. The most important processes are from DNA to RNA, called transcription. And from RNA to proteins, called translation|[About DNA replication, transcription, and translation](https://www.youtube.com/watch?v=6gUY5NoX1Lk)   |
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Measurements.png" width="25000">  |  And we can measure each level to learn about the biological processes in the cell. Each layer comes with its own set of experimental techniques and downstream bioinformtics analysis. Some techniques measure one or several molecules. We can call them low-throughput. In opposite, there are methods that try to measure all moleculs of a type of interest. We can call them high-throughput.  |[About biomolecules](https://www.youtube.com/watch?v=1Dx7LDwINLU)|

## DNA level

| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Genomics.png" width="25000">  |DNA level is referred to as Genomics. Genomics studies whole genomes of organisms. It uses a combination of recombinant DNA, DNA sequencing methods, and bioinformatics to sequence, assemble, and analyse the structure and function of genomes. The main difference between genomics and genetics is that genetics scrutinizes the functioning and composition of the single gene (or several genes) where as genomics addresses all genes and their inter relationships in order to identify their combined influence on the growth and development of the organism.|[About DNA](youtube.com/watch?si=NF9aF05YWWBrv5s0&v=AmOO4j0E408&feature=youtu.be)|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Development_genomics.png" width="25000">  |The main technique to study genomes is sequencing. Sequencing refers to getting access to the sequence or primary structure of any biopolymer. (DNA, mRNA, miRNA, methylation pattern). The sequencing have been rapidly developing from low-throughput methods like Sanger sequencing, which is still remains the 'gold standard' to Illumina sequencing that can sequence millions of fragments in parallel or aims to sequence the whole DNA (long-sequencning by PacBio/ONT Nanopore).|[Sanger sequencing](https://www.youtube.com/watch?v=e2G5zx-OJIw) [Illumina](https://www.youtube.com/watch?v=fCd6B5HRaZ8&t=179s) [PacBio](https://www.youtube.com/watch?v=_lD8JyAbwEo) [Nanopore](https://www.youtube.com/watch?v=RcP85JHLmnI)|
|||[About mutations](https://www.youtube.com/watch?v=vl6Vlf2thvI)|


## RNA level
| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/RNA_measurements.png" width="25000">  |On the level of RNA, in the transcriptomics, we measure and analyze the level of RNA. Two main techniques here are microarray (which is becoming obsolete but still used) and RNA sequencning (RNA-Seq). In microarray, we can detect the presence of pre-defined sequences (probes) that hybridize with the sequences in the sample and trigger flouresence. The fluoresecne intensity allows to assess the level of a probe. RNA sequencning (RNA-seq) allows to detect all RNA transcripts within a sample. We can have only mRNAs, so-called poly-A enriched RNA-Seq. Or we can have total RNA-Seq, and also detect non-coding RNAs|[About RNA](https://www.youtube.com/watch?v=jUUJSOM1ihU)|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">  |Now, as we briefly mentioned RNA level, we can answer the followng questions. Each cell in an organism contains the same DNA. What makes all cells look and function differently. And one answer is difference in gene expression.||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">  |Here is the scheme of a prokaryotic gene. You see the coding parts, that can be transcribed into mRNAs and translated into proteins. Gene A, Gene B, etc. In prokaryotes, related genes, e.g., genes that encode parts of a protein complex or encode for enzymes that function together, often are located close to each other and transcribed together. This is called operon. Then, there should be a signal for RNA polymerase where to start a transcription. This region is called promoter. And between promoter and genes there is a region, called operator. ||
||Operator is a region where a protein can bind and either physically block binding of RNA polymerase (thus, repress the gene expression) or attract it (thus, activates). The special protein is called transcriptional factor.||
||The structure of a eukariotic gene is a bit more complicated. Within the gene there are coding regions - exons, and non-coding regions - introns. After transcription, or actually during transcription (so called, co-transcriptionally), introns are removed, and exons are joind together. The process is called splicing. So in other words, introns are spliced out, and exons are spliced in. However, eukaryotic genes have the same regulatory regions: promotes to start transcription and operator to bind transcriptional factor|[About gene expression regulation](https://www.youtube.com/watch?v=ebIpkw3XapE)|
||There is one more, very intriguing type of regulation that is very remote. A very distant region, enhancer, that can bind and impact the gene expression||
||Coming back to the eukariotic gene structure, we now see one more mechanism how the same DNA can manisfest into different cell types. Introns and exons can be seen as building blocks that can be combined in different ways. This process is called alternative splcing. And the estimation is that 95% of multiexonic genes undergo alternative splicing||
||During alternative splcing, exons can be skipped, extended, or shortened. Also introns might be kept in the resulting mRNA. And there are also special proteins - splicing factors - that regulate this process. The resulting mRNA are translated into proteins that might be similar but might be very different in function and structre.||

## Epigenetics
| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
||The cells diverity might be not only dictated on the level of RNA but already on the level of DNA. Here we talk about epigenetics. “Epi” in Greek meaning “on” or “above”. C.H. Waddington used the phrase in the 1940’s to describe how environmental influences on developmental event can affect the phenotype. The present definition describe 'epigenetics' as alteration of gene (expression) without changes in DNA sequence itself, which may lead to functional changes. This includes chemical modifications of the DNA or the histones. Why is this important||
||Let's have a look into the organization of a genome. How long is a DNA molecule. It is around 3 meters. And cell nucleus (if we talk about eukaryotic cells, for example), is micrometers. How to put inside such a long molecule. You need to pack it quite tightly||

## Proteins



Biomarkers
======

