---
title: "Basics on Bioinformatics and Systems Biology: Lecture 5"
collection: teaching
type: "Lecture"
permalink: /teaching/bbsb_lecture_5
venue: "VU"
date: 2026-01-10
location: "Amsterdam, the Netherlands"
---

Here you will find the basic concepts for the Lecture 2 and links to the additional/support materials

# Transcriptomics

## How do we measure gene expression

| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| How can we measure gene expression? Depends in the purpose. If you need to detect or measure one or several known RNA molecules, there are low-throughput methods. We will not cover them in the course but it is important to know that they exist. Nothern blot detects the presence of known RNA molecule(s). qPCR quantifies the amount of also known RNA molecules. That's why qPCR has an application in virology - to detect virus molecules, e.g., COVID-19. mRNA FISH is used to detect and visualize RNA molecules within a cell based on fluorescently labeled probes|[Nothern blot](link)   [qPCR](link) [mRNA FISH](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| However, if we need to measure (almost) all genes in a sample, we use microarray or RNA-Sequencing. Microarray is almost obsolete though it is still have some applications, it is cheaper, and there are microarray datasets that is still widely used e.g., METABRIC that consists of about 2500 breast cancer samples. However, microarray uses the predefined set of probes to detect and quantify RNA, thus we can not detect and quantify novel transcripts. That's why RNA-Sequenicng is the most popular technology for measuring gene expression|[Microarray](link)   [METABRIC](link)  |
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| Sequencing technologies (covered in Lecture 4): <ul><li>First generation - Maxam-Gilber sequencing and Sanger sequencing</li><li>Second generation - high-throughput and parallel e.g., Illumina</li><li>Third generation - Single-cell and long reads resolution e.g., ONT Nanopore, PacBio</li></ul> |[Illumina](link)   [Sanger sequencing](link) [Nanopore](link) [PacBio](link) |

Computational analysis of bulk RNA-Sequencing data: from raw files to biological interpretation (next lecture)
======
| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|FASTQ files represent raw data for RNA-sequencing (and all other sequencing) analysis. FASTQ format consists of: 1) The name/identifier of a sequence; 2) A sequence; 3) A delimiter; 4) Quality scores. FASTA format (often used in the sequencing databases) consists of: 1) The name/identifier of a sequence; 2) A sequence. |[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|Quality scores symbols encode the probability of a nucleotide to be called erroneously. Quality scores calculation is a part of a base calling algorithm inside the sequencing instrument|[Manuscript](https://genome.cshlp.org/content/8/3/175?implicit-login=true%26263)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|The first step is always the Qulity Control step. The most used programs are FastQC (one report per one sample) and MultiQC (one report per multiple samples). Quality control programs take FASTQ files as input and generate the quality plots based on the quality scores and other sequencing results parameters (e.g., GC content, lenth, duplicate level, etc). Why is the step important? Because RNA-Sequencing (and any analysis) follows the principle 'Garbage in, Garbage out' |[FastQC](link)   [MultiQC](link) [QC Fail](https://sequencing.qcfail.com/)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|The second step is to find the origin of a read sequence. Here the two main approaches are to assemble the reads de novo (the assembly algorithms were covered on Lecture 4) and to map them to a template - reference genome or transcriptome. |[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|The reference genome is DNA sequences representing the DNA material of an organism. There are huge databases that collect all genomes - GenBank (NCBI, USA) and Ensembl (EMBL, Europe). Also, the model organisms usually have the dedicate, separate consortiums and databases. |[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| The mapping process usually consists of two steps. The first step is the genome indexing - making a vocabulary of all small words in the genome and their coordinates. To store this vocabulary, different tools use all possible structures like hashes, suffix trees or arrays, Burrow-Wheeler transform. The idea is to have a structure which you can use to look for the word of interest as fast as possible. The second step is mapping ...|[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| |[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| |[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| |[](link)   [](link)|

Heading 3
======
