---
title: "Basics on Bioinformatics and Systems Biology: Lecture 3"
collection: teaching
type: "Lecture"
permalink: /teaching/bbsb_lecture_3
venue: "VU"
date: 2026-01-10
location: "Amsterdam, the Netherlands"
---

The basic concepts (not the full lecture!) for the Lecture 3: Introduction and links to the additional/support material

# DNA sequencing

## Introduction

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_2.png" width="25000">  |**Sequencing** is the process of determining the order of letters. In DNA sequencing, we determine the order of nucleotides.||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_3.png" width="25000">|The first sequenced genome was a genome of bacteria Haemophilus influenza and it was in a magnitute of megabases. The current state of DNA sequencing technology allows to sequence in the magnitude of gigabases.||

## DNA structure
| Slide | Text | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_11.png" width="25000">|**DNA** stands for **Deoxyribonucleic acid**. **Ribo** reflects that DNA contains the sugar **ribose** with 5 carbon atoms (5-C sugar). The **acid** stands because DNA has three **phosphate** groups. **Deoxy** reflects that the ribose sugar lacks one oxygen atom. The final part is the **nitrogenous base**: Adenine (A), Thymine (T), Guanine (G), Cytosine (C).||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_12.png" width="25000">|In a **DNA** molecule, nucleotides are paired based on the **complimentarity**: A with T and G with C. Nucleotides are connected to each other via **phosphodiester bonds** between the 3'-hydroxyl group and the 5'-alpha-phosphate. Each new nucleotide is added to the 3'-hydroxil group. This synthesis direction is called **5'-3' sense**. If the oxygen atom is missing at the 3'-end, a new nucleotide can not be added, and the DNA synthesis stops. In other words, it leads to **chain termination**. The nucleotides without the oxygen atom at the 3'-end that lead to chain termination are the essential part of **Sanger sequencing**.||

## Sanger sequencing
| Slide | Text | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_15.png" width="25000">|Sanger sequencing is the chain termination sequencing method. It presents the 1st generation sequencing technology. The steps of Sanger sequencing: 1) The synthesis of a **primer**: a short nucleotide chain that complimentarily binds to a single-stranded DNA and serves as a start of a DNA synthesis. 2) The DNA synthesis: during the DNA sequencing we add modified nucleotides that lack the oxygen at the 3'-end and lead to chain termination (dideoxyribonucleotides (ddNTPs)). We set four DNA synthesis reactions, each with only a single type of ddNTP (ddATP, ddTTP, ddGTP, and ddCTP) mixed in. In an automatic Sanger sequencing, ddNTPs are fluorescently labelled with different colors. As a result, for a single type of ddNTP, we have all DNA fragments that end with this type of nucleotide. 3) We separate the fragments by size via capillary gel electrophoresis. **Electrophoresis**: technique to separate molecules in a gel based on different sizes and electric charge. Smaller molecules will move faster than larger molecules. 4) We analyze the gel to read the sequence of a DNA.||


## Illumina and Oxford Nanopore (ONT) sequencing
| Slide | Text | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_17.png" width="25000">|Illumina sequencing presents the 2nd generation sequencing technology.|[Illumina](https://www.youtube.com/watch?v=fCd6B5HRaZ8)|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_18.png" width="25000">|Oxford Nanopore (ONT) sequencing presents the 3rd generation sequencing technology based on long reads|[ONT](https://www.youtube.com/watch?v=E9-Rm5AoZGw)|

## Sequencing output
| Slide | Text | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_19.png" width="25000">|**Sequencing reads** are output of a sequencing machine that represents the sequence of letters in a molecule. For DNA sequencing, reads represent the sequence of nucleotides as a DNA fragment.||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_20.png" width="25000">|Output of sequencing is stored in a text-based **FASTQ** format. Each read has four features: 1) an identifier that starts with @; 2) a sequence; 3) a separator +; 4) a quality score||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_21.png" width="25000">|**Sequencing depth** is a number of times a specific nucleotide base is read (present in a read). **Sequencing coverage** is how much of the total original sequence has been read.||

## Genome assembly
| Slide | Text | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_25.png" width="25000">|**Genome assembly** is the computational process of reconstructing a genome sequence from the DNA reads produced by sequencing machines. Reads can be presented as graphs. Each unique distinct element of a read can be presented as a **node** (or a **vertex**). The nodes are connected with **edges** with have directions (**directed graph**). The task is to find a **Eulerian path**: a trail in a finite graph that visits every edge exactly once, allowing for revisiting nodes).||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_26.png" width="25000">|Genome assembly algorithms use the representation of reads as graphs and are based on the **Universal string problem** formulated by Nicolaas de Bruijn. **Universal string problem**: Given a set of strings, find a circular string that contains each of them exactly once. Steps: 1) Define k-mers, substrings of length k (e.g., 000, 001, etc). 2) Split each k-mer into left and right (k-1)-mers with overlap (e.g., 000 will be splitted into 00 and 00). 3) Define the unique elements from all (k-1)-mers (e.g., 00 will be the unique element for 000 k-mer). These unique elements will serve as nodes. 4) Connect nodes of unique elements with directed edges if there is an overlap between these unique elements. The result will be the **de Brujin graph**. 5) To solve the universal string problem, find the Eulerian path: a trail in a finite graph that visits every edge exactly once, allowing for revisiting nodes||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_29.png" width="25000">|The steps of the de Bruijn algorithm for the genome assembly are similar: 1) Split the sequence/the reads into k-mers. k could be of any value, e.g., 3, 5, or 7. 2) Split k-mers into left and right (k-1)-mers. 3) Find unique elements. 4) Construct the de Bruijn graph: unique (k-1)-mers are nodes and overlaps are edges. 5) find a Eulerian path.|[Paper: Why are de Bruijn graphs useful for genome assembly?](https://pmc.ncbi.nlm.nih.gov/articles/PMC5531759/) [Paper: How to apply de Bruijn graphs to genome assembly](https://www.nature.com/articles/nbt.2023)|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_32.png" width="25000">|Repeats in the original sequence lead to loops in the de Bruijn graphs, and to ambiguity in choosing the Eulerian paths and errors during the genome assembly. Repeats challenge the genome assembly because the genomes usually have many repetitive elements.||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/not_published/images/BBSB_3_33.png" width="25000">|High sequencing depth will help to identify and resolve sequencing errors. Keeping the track of the sequencing coverage will help to track back the most covered Eulerian path in the graph.||

