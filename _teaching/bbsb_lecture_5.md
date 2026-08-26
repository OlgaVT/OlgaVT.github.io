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
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-5_page-0010.jpg" width="25000">| The difference between **low-** and **high-throughput methods** concerns the number of samples to be measured. <ul>Low-throuput gene expression measuring methods:<li>**Nothern blot** detects known RNA molecules</li><li>qPCR quintifies known RNA molecules (e.g., COVID19 test)</li><li>**mRNA fluorescence in situ hybridization/mRNA FISH** visualizes known mRNA molecules</li></ul><ul>High-throughput methods:<li>**Microarray** quantifies the expression of thousands of genes based on the known DNA sequences (**probes**). Cheaper, almost obsolete (have specific applications). </li><li>**RNA-Sequencing** quantifies mRNA molecules (**poly(A) RNA-Seq**) or all RNA molecules (**Total RNA-Seq**)</li></ul>|[Nothern blot](https://youtu.be/11NHYntRV4Q?si=zobrJ7W3ucd2b43F) [qPCR for COVID test](https://youtu.be/ThG_02miq-4?si=g7DXZ-QeFOxiSNgp) [Microarray](https://youtu.be/xoxUWGl8WFs?si=RXzNU-7S8JQ7Sanv) [DNA Sequencing library preparation](https://youtu.be/VEgeqcHkljc?si=0xsYEN4fHdS5QbyS) [RNA Sequencing library preparation](https://youtu.be/xKzzmhJQjUE?si=VN1GsDUYLZ4zyn-Z)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-5_page-0011.jpg" width="25000">| Sequencing technologies: <ul><li>First generation - Maxam-Gilber sequencing and Sanger sequencing</li><li>Second generation - high-throughput and parallel e.g., Illumina</li><li>Third generation - Single-cell and long reads resolution e.g., ONT Nanopore, PacBio</li></ul>| [Sanger sequencing](https://www.youtube.com/watch?v=e2G5zx-OJIw) [Illumina](https://www.youtube.com/watch?v=fCd6B5HRaZ8&t=179s) [PacBio](https://www.youtube.com/watch?v=_lD8JyAbwEo) [Nanopore](https://www.youtube.com/watch?v=RcP85JHLmnI) |

## Computational analysis of bulk RNA-Sequencing data

### Raw data
| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-5_page-0014.jpg" width="25000">|**FASTQ** files represent raw data for RNA-sequencing (and all other sequencing) analysis. FASTQ format consists of: 1) The name/identifier of a sequence; 2) A sequence; 3) A delimiter; 4) Quality scores. A sequence represents a short RNA gragment and is called **read**. **FASTA** format (often used in the sequence databases) consists of: 1) The name/identifier of a sequence; 2) A sequence. ||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-5_page-0015.jpg" width="25000">|**Quality scores** symbols encode the probability of a nucleotide to be called erroneously. Quality scores calculation is a part of a base calling algorithm inside the sequencing instrument|[Manuscript](https://genome.cshlp.org/content/8/3/175?implicit-login=true%26263)|

### Quality control
| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-5_page-0016.jpg" width="25000">| The first step is always the **Quality Control** step. **'Garbage in, Garbage out' principle**: flawed, biased or poor quality (garbage) information or input produces a result or output of similar ("garbage") quality. The most used programs are FastQC (one report per one sample) and MultiQC (one report per multiple samples). Quality control programs take FASTQ files as input and generate the quality plots based on the quality scores and other sequencing results parameters (e.g., GC content, read length, duplicate level, etc). |[FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) [MultiQC](https://github.com/multiqc/multiqc) [QC Fail](https://sequencing.qcfail.com/)|

### Mapping and quantification
| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-5_page-0021.jpg" width="25000">|The second step is to find the origin of a read sequence. Here the two main approaches are to assemble the reads de novo (**Transcriptome assembly**) and to map them to a template (**Reference genome/transcriptome mapping**). ||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-5_page-0021.jpg" width="25000">|The **reference genome** is DNA sequences representing the DNA material of an organism. There are huge databases that collect all sequenced genomes - GenBank (NCBI, USA), Ensembl (EMBL, Europe), DDBJ (BI-DDBJ, Japan). Also, the model organisms (e.g., human, mouse, arabidopsis) have the dedicated, separate consortiums and databases. |[GeneBank](https://www.ncbi.nlm.nih.gov/genbank/) [Ensembl](https://www.ensembl.org/) [DDBJ](https://www.ddbj.nig.ac.jp/index-e.html)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-5_page-0024.jpg" width="25000">| The mapping process usually consists of two steps. The first step is the **genome indexing**: making a vocabulary of all small words (**k-mers**) in the genome and their coordinates. Storing structures examples: hashes, suffix trees or arrays, Burrow-Wheeler transform. The second step is **read mapping**: the process of aligning and detecting the coordinates of a read. |[Ben Langmead on Suffix trees and arrays ]([link](https://www.youtube.com/watch?v=odyGCviFmXA&list=PL2mpR0RYFQsDFNyRsTNcWkFTHTkxWREeb)) [Manuscript with an overview of mapping tools](https://link.springer.com/article/10.1186/s13059-021-02443-7)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-5_page-0029.jpg" width="25000">|<ul>Counting reads quantifies how many reads have been mapped to a genomics feature (e.g., gene) to measure gene expression level. <li>Computational tools: HTSeq (usually genes), featureCounts (usually genes), kallisto (usually transcripts), Salmon (usually transcripts), RSEM (both) </li><li>Result: a raw gene/transcript count table</li></ul>|[HTSeq](https://htseq.readthedocs.io/en/latest/) [featureCounts](https://subread.sourceforge.net/featureCounts.html) [kallisto](https://pachterlab.github.io/kallisto/about) [Salmon](https://combine-lab.github.io/salmon/) [RSEM](https://github.com/deweylab/RSEM)|

Computational analysis of bulk RNA-Sequencing data: differential gene expression
======

| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| |[](link)   [](link)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">| |[](link)   [](link)|

Heading 3
======
