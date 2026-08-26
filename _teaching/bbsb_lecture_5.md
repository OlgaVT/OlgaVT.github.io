---
title: "Basics on Bioinformatics and Systems Biology: Lecture 5"
collection: teaching
type: "Lecture"
permalink: /teaching/bbsb_lecture_5
venue: "VU"
date: 2026-01-10
location: "Amsterdam, the Netherlands"
---
Here you will find the basic concepts for the Lecture 2 and links to the additional/support materials.

# Transcriptomics

## How do we measure gene expression

| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-5_page-0010.jpg" width="25000">| The difference between **low-** and **high-throughput methods** concerns the number of samples to be measured. <ul>Low-throuput gene expression measuring methods:<li>**Nothern blot** detects known RNA molecules</li><li>qPCR quintifies known RNA molecules (e.g., COVID19 test)</li><li>**mRNA fluorescence in situ hybridization/mRNA FISH** visualizes known mRNA molecules</li></ul><ul>High-throughput methods:<li>**Microarray** quantifies the expression of thousands of genes based on the known DNA sequences (**probes**). Cheaper, almost obsolete (have specific applications). </li><li>**RNA-Sequencing** quantifies mRNA molecules (**poly(A) RNA-Seq**) or all RNA molecules (**Total RNA-Seq**)</li></ul>|[Nothern blot](https://youtu.be/11NHYntRV4Q?si=zobrJ7W3ucd2b43F) [qPCR for COVID test](https://youtu.be/ThG_02miq-4?si=g7DXZ-QeFOxiSNgp) [Microarray](https://youtu.be/xoxUWGl8WFs?si=RXzNU-7S8JQ7Sanv)|

| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| Sequencing technologies: <ul><li>First generation - Maxam-Gilber sequencing and Sanger sequencing</li><li>Second generation - high-throughput and parallel e.g., Illumina</li><li>Third generation - Single-cell and long reads resolution e.g., ONT Nanopore, PacBio</li></ul> |[Sanger sequencing](https://www.youtube.com/watch?v=e2G5zx-OJIw) [Illumina](https://www.youtube.com/watch?v=fCd6B5HRaZ8&t=179s) [PacBio](https://www.youtube.com/watch?v=_lD8JyAbwEo) [Nanopore](https://www.youtube.com/watch?v=RcP85JHLmnI) |

Computational analysis of bulk RNA-Sequencing data: from raw files to a gene counts table
======
| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|FASTQ files represent raw data for RNA-sequencing (and all other sequencing) analysis. FASTQ format consists of: 1) The name/identifier of a sequence; 2) A sequence; 3) A delimiter; 4) Quality scores. FASTA format (often used in the sequencing databases) consists of: 1) The name/identifier of a sequence; 2) A sequence. |[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|Quality scores symbols encode the probability of a nucleotide to be called erroneously. Quality scores calculation is a part of a base calling algorithm inside the sequencing instrument|[Manuscript](https://genome.cshlp.org/content/8/3/175?implicit-login=true%26263)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|The first step is always the Qulity Control step. The most used programs are FastQC (one report per one sample) and MultiQC (one report per multiple samples). Quality control programs take FASTQ files as input and generate the quality plots based on the quality scores and other sequencing results parameters (e.g., GC content, lenth, duplicate level, etc). Why is the step important? Because RNA-Sequencing (and any analysis) follows the principle 'Garbage in, Garbage out' |[FastQC](link)   [MultiQC](link) [QC Fail](https://sequencing.qcfail.com/)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|The second step is to find the origin of a read sequence. Here the two main approaches are to assemble the reads de novo (the assembly algorithms were covered on Lecture 4) and to map them to a template - reference genome or transcriptome. |[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|The reference genome is DNA sequences representing the DNA material of an organism. There are huge databases that collect all genomes - GenBank (NCBI, USA) and Ensembl (EMBL, Europe). Also, the model organisms usually have the dedicate, separate consortiums and databases. |[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| The mapping process usually consists of two steps. The first step is the genome indexing - making a vocabulary of all small words in the genome and their coordinates. To store this vocabulary, different tools use all possible structures like hashes, suffix trees or arrays, Burrow-Wheeler transform. The idea is to have a structure which you can use to look for the word of interest as fast as possible. The second step is mapping ...|[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| After you mapped all the sequences (reads) from the FASTQ raw file, you can count how many reads you have per a genome region e.g., per gene. The result is a count table. Each cell represents the amount of gene present in the sample, or in other words, the gene expression. One of the most common questions to ask is which genes have different level of expression between samples.|[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| |[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| |[](link)   [](link)|

Computational analysis of bulk RNA-Sequencing data: differential gene expression
======

Heading 3
======
